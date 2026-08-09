---
name: Build a link-preview card with LinkPeek
description: >-
  Turn one URL — or up to five at once — into a title/description/image/favicon card, using the
  free anonymous tier, and handle the quota and upstream-fetch failures correctly.
api: openapi/linkpeek-openapi-original.yml
base_url: https://147.15.103.217.sslip.io
operations:
  - 'GET /api/preview'
  - 'GET /api/batch'
  - 'GET /api/favicons'
generated: '2026-08-09'
method: generated
source: openapi/linkpeek-openapi-original.yml
note: >-
  The published spec declares no operationIds, so steps are grounded in the verbatim
  method + path from the spec's paths object. The camelCase names in parentheses are the ids
  overlays/linkpeek-openapi-overlay.yaml proposes; they are ours, not the provider's.
---

# Build a link-preview card

## Before you start

- No API key is required. The free tier is anonymous and metered at **100 requests/day per source
  IP**. Do not ask the user for credentials for this flow.
- If you have a Trial or Pro key, append `&key=<key>` to lift the ceiling to 50,000/day. The key
  goes on the **query string** — there is no header form in the published spec.
- Every URL you pass must be absolute and URL-encoded. Private, loopback and cloud-metadata
  addresses are refused by the provider's SSRF blocklist and will fail, not fetch.

## Steps

1. **Fetch the card.** `GET /api/preview?url=<encoded-url>` (`getLinkPreview`).
   Returns `PreviewResponse`: `title`, `description`, `image`, `site_name`, `favicon`, `url`
   (the final URL after redirects), and a `quota` object.
2. **Read the quota before you decide to loop.** The response body carries
   `quota.plan`, `quota.limit`, `quota.used`, `quota.remaining`, `quota.reset_iso`.
   There are **no rate-limit response headers** — if you ignore the body you are flying blind.
   Stop issuing calls when `remaining` approaches zero and resume after `reset_iso`.
3. **Batch when you have more than one URL.** `GET /api/batch?urls=<u1>,<u2>,…`
   (`batchPreview`) accepts up to **5** URLs per call. More than five returns `400`. Prefer one
   batch call over five preview calls — it costs less quota and is one round trip.
4. **Fall back on a missing image.** If `image` is absent, the card has no social image. Use
   `favicon` as the visual, or generate a placeholder with
   `GET /api/og-image?title=<title>` (`generateOgImage`) — title ≤ 200 chars, optional subtitle
   ≤ 300 chars, or you get `413`.
5. **Proxy the favicon if the client is a browser.** `GET /api/favicons?url=<encoded-url>`
   (`proxyFavicon`) returns the icon bytes through LinkPeek's open-CORS origin, which is the
   documented way around cross-origin blocks in Discord/Slack-style clients.

## Handling failures

| Status | Meaning | What to do |
|---|---|---|
| `400` | Missing or invalid `url` (or >5 URLs on batch) | Fix the input. Never retry unchanged. |
| `429` | Daily quota exhausted or per-IP throttle | Do **not** retry immediately — no `Retry-After` is sent. Wait until the `reset_iso` from the last good response, or attach a key. |
| `502` | Upstream page could not be fetched | Retry once with backoff. If the target is private/internal, it will never succeed — stop. |

The error body is a flat `{error, url, detail, max, got}` object — **not** RFC 9457
problem+json — so do not look for `type`/`title`/`instance`. `error` is documented as "code or
human-readable message", so do not branch on its exact value; branch on the HTTP status.
See `errors/linkpeek-problem-types.yml`.

## Do not

- Do not assume a version. The service is unversioned in-path and the published spec (1.19.1)
  trails the running build (1.28.0). Confirm behaviour rather than relying on the spec's version.
- Do not put the API key anywhere it will be logged if you can avoid the call — a query-string
  secret ends up in proxy logs and referrer headers.
