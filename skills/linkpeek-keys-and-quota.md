---
name: Manage LinkPeek keys and quota
description: >-
  Discover what the live service actually exposes, read your remaining quota, and obtain a trial
  or Pro key — including what the provider does and does not guarantee.
api: openapi/linkpeek-openapi-original.yml
base_url: https://147.15.103.217.sslip.io
operations:
  - 'GET /api/status'
  - 'GET /api/health'
  - 'GET /api/health/json'
  - 'GET /api/key'
  - 'GET /api/subscribe'
generated: '2026-08-09'
method: generated
source: openapi/linkpeek-openapi-original.yml
note: >-
  The published spec declares no operationIds; steps cite the verbatim method + path. Names in
  parentheses are the ids proposed in overlays/linkpeek-openapi-overlay.yaml.
---

# Manage keys and quota

## Discover the real surface before anything else

`GET /api/status` (`getServiceStatus`) is unmetered and returns the running `version`, `ok`,
`uptime_seconds`, `free_daily_limit`, `pro_daily_limit`, and a `RouteInfo[]` array of **every
registered route with its allowed methods**. This is the authoritative surface — the published
OpenAPI documents only a subset of it. Start here whenever you need an endpoint that is not in
the spec.

`GET /api/health` (`getHealth`) and `GET /api/health/json` (`getHealthJson`) are the liveness
checks; `health/json` has a fixed structure and is the one to poll from code.

## Read your quota

Metered responses embed `quota`: `plan`, `limit`, `used`, `remaining`, `reset_iso`. There are no
rate-limit headers on any response, so parse the body. Budget against `remaining` and schedule
retries against `reset_iso`.

## Get a key (only if you need more than 100/day)

1. **Trial** — `GET /api/key?email=<address>` (`issueTrialKey`) mints a 14-day key with the
   50,000/day ceiling. No card required; it auto-expires back to Free.
2. **Pro** — `GET /api/subscribe?email=<address>` (`subscribePro`) mints a non-expiring key and
   returns a self-serve PayPal payment link ($1/month), along with `api_key`, `pay_url`,
   `pay_method`, `price_usd` and `instructions`.
3. Both return `400` on a missing or invalid email.
4. Use the key by appending `?key=<key>` (or `&key=`) to any metered endpoint.

## What an agent must know before automating this

- **These are `GET` requests that create state.** Issuing a key and starting a subscription are
  both side-effecting operations behind `GET`, with no idempotency key and no de-duplication
  contract. A retry, a prefetch, or a crawler can mint keys. Never place these calls on a
  retry path, and never let a generic "GET is safe" heuristic reach them.
- **Entitlement precedes payment.** The provider documents that a Pro key works immediately and
  that payment reconciliation is manual. Do not read a working key as proof of a completed
  payment.
- **The key travels in the URL.** It will appear in proxy logs, browser history and referrer
  headers. Treat it as low-sensitivity, rotate by re-issuing, and never log full request URLs.
- **There is no 401/403 contract.** The spec documents no response for an invalid or expired key,
  so handle an unexpected status defensively rather than matching on a documented one.
- **There is no SLA and no status page.** `/api/status` and `/api/health` are served by the API
  itself and go down with it. See `lifecycle/linkpeek-lifecycle.yml`.
