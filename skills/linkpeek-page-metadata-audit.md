---
name: Audit a page's metadata with LinkPeek
description: >-
  Pick the right depth of extraction — card, crawl, or full meta dump — and inspect a page's meta
  tags, link tags, favicons and response headers without writing a scraper.
api: openapi/linkpeek-openapi-original.yml
base_url: https://147.15.103.217.sslip.io
operations:
  - 'GET /api/extract'
  - 'GET /api/metadata-full'
  - 'GET /api/meta-tag-parser'
  - 'GET /api/favicon-extractor'
  - 'GET /api/headers'
generated: '2026-08-09'
method: generated
source: openapi/linkpeek-openapi-original.yml
note: >-
  The published spec declares no operationIds; steps cite the verbatim method + path. Names in
  parentheses are the ids proposed in overlays/linkpeek-openapi-overlay.yaml.
---

# Audit a page's metadata

## Pick the depth first — each level costs a separate metered call

There is no `fields` or `expand` parameter. Depth is chosen by endpoint, so choose once and do
not chain calls you do not need.

| Need | Endpoint | Returns |
|---|---|---|
| A social card | `GET /api/preview?url=` (`getLinkPreview`) | title, description, image, site_name, favicon |
| Card + structure | `GET /api/extract?url=` (`extractPage`) | raw meta plus headings and links |
| Every meta tag | `GET /api/metadata-full?url=` (`getMetadataFull`) | full metadata dump |
| Meta **and** `<link>` tags | `GET /api/meta-tag-parser?url=` (`parseMetaTags`) | `MetaTag[]` and `LinkTag[]` |
| Icons only | `GET /api/favicon-extractor?url=` (`extractFavicons`) | every declared favicon as `Icon[]` |
| Transport only | `GET /api/headers?url=` (`getResponseHeaders`) | the target's HTTP response headers, no body |

## Steps

1. URL-encode the target and call exactly one endpoint from the table.
2. `GET /api/headers?url=` is the cheapest way to answer "is this URL alive, and what does it
   claim to serve?" without pulling or parsing the body.
3. For an icon set, `extractFavicons` gives you every declared icon with its metadata; use
   `GET /api/favicons?url=` only when you want the raw bytes proxied.
4. All five endpoints are metered and share the same 100/day (free) or 50,000/day (keyed)
   allowance. Read `quota.remaining` off any metered response before you loop over a URL list.

## Handling failures

- `400` — the `url` parameter was missing or unparseable. Send an absolute, encoded http(s) URL.
- `502` — the upstream page could not be fetched. Retry once with backoff; a private, loopback or
  cloud-metadata target is blocked by the provider's SSRF blocklist and will never resolve.
- `429` — quota exhausted. No `Retry-After` header is sent; use `quota.reset_iso` from an earlier
  successful response.

## Undocumented neighbours — probe before you automate

The live route index (`GET /api/status`) lists ~107 routes while the published OpenAPI documents
16. Adjacent extractors — `/api/opengraph`, `/api/og-extract`, `/api/structured-data`,
`/api/readability`, `/api/links`, `/api/headings`, `/api/word-count`, `/api/tech-stack` — are
real and callable but carry **no published parameters or response schema**. Treat their shapes as
unverified: probe once and pin what you observe rather than assuming.
