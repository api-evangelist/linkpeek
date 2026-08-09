---
name: Generate a QR code with LinkPeek
description: >-
  Produce a QR code from arbitrary text or a URL as either a PNG image or base64 JSON, and respect
  the 2000-character payload ceiling.
api: openapi/linkpeek-openapi-original.yml
base_url: https://147.15.103.217.sslip.io
operations:
  - 'GET /api/qr'
  - 'GET /api/qrcode'
generated: '2026-08-09'
method: generated
source: openapi/linkpeek-openapi-original.yml
note: >-
  The published spec declares no operationIds; steps cite the verbatim method + path. Names in
  parentheses are the ids proposed in overlays/linkpeek-openapi-overlay.yaml.
---

# Generate a QR code

## Choose the right endpoint

Both endpoints encode the same payload; they differ only in what comes back, and content
negotiation does **not** switch between them — pick by path.

- `GET /api/qr?text=<payload>` (`generateQrPng`) → `image/png` bytes. Use when you are writing a
  file or setting an `<img src>`.
- `GET /api/qrcode?text=<payload>` (`generateQrJson`) → JSON with the image base64-encoded. Use
  when you need to embed the image in a JSON response or a data URI without a second fetch.

## Steps

1. URL-encode the payload and call one of the two endpoints above.
2. Keep `text` at **2000 characters or fewer**. Over that you get `413`, and the error body tells
   you exactly what happened: `max` is the ceiling, `got` is what you sent.
3. If you sent nothing, you get `400` — `text` is required.
4. No key is needed on the free tier (100 requests/day per IP). Append `&key=<key>` for
   50,000/day.

## Handling failures

| Status | Meaning | What to do |
|---|---|---|
| `400` | Missing `?text=` | Supply a payload. |
| `413` | Payload over 2000 chars | Read `max`/`got` from the body and shorten. For a long URL, shorten it first with the provider's own `GET /api/shortlink?url=` (live route; not in the published spec, so treat its response shape as unverified). |
| `429` | Daily quota exhausted | Wait for the reset time from a prior response's `quota.reset_iso`; no `Retry-After` is sent. |

## Notes

- The QR endpoints are metered like the rest of the API — a page that renders many QR codes will
  burn the 100/day free allowance fast. Cache the PNG on your side.
- `GET /api/qr-with-logo` and `GET /api/qr-analytics` exist on the live route index but are not in
  the published OpenAPI, so their parameters and responses are undocumented — do not call them
  from an automated flow without probing first.
