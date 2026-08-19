# LinkPeek (linkpeek)

A developer utility REST API bundling ~92 JSON endpoints for URL intelligence (link preview, metadata, OpenGraph), QR generation, DNS/WHOIS/SSL security checks, and data-conversion dev tools. Includes an OpenAI-compatible chat/completions surface. Hobby-grade service hosted on Oracle Cloud Free Tier via a raw-IP sslip.io hostname.

**APIs.json:** [https://linkpeek.apievangelist.com/apis.yml](https://linkpeek.apievangelist.com/apis.yml)

## Tags

- screenshots
- webpage-capture
- website-thumbnails
- image-generation
- rendering
- web-scraping-adjacent
- developer-tools
- saas
- rest-image-api
- Developer Tools
- Utility API
- URL Metadata
- Link Preview
- OpenGraph
- QR Code Generation
- DNS
- WHOIS
- SSL
- Web Security Scanning
- IP Geolocation
- Data Conversion
- LLM-Compatible API
- api-utilities
- url-metadata
- link-preview
- qr-code-generation
- dns-whois
- web-security-scanning
- data-conversion
- openai-compatible-llm

## Timestamps

- **Created:** 2026-08-09
- **Modified:** 2026-08-09

## APIs

### LinkPeek Screenshot API

HTTP/REST-style image API: request a target URL with parameters (e.g. size=original, viewport flags) and receive a webpage screenshot image. API-key authenticated; paid plans from $20/month.

- **Human URL:** [https://linkpeek.com/docs](https://linkpeek.com/docs)
- **Base URL:** `https://linkpeek.com/api/v1`

#### Tags

- screenshots
- webpage-capture
- website-thumbnails
- image-generation
- rendering
- web-scraping-adjacent
- developer-tools
- saas
- rest-image-api

#### Properties

- [Documentation](https://linkpeek.com/docs)
- [API Reference](https://linkpeek.com/docs/request-options)
- [Developer Portal](https://linkpeek.com/)
- [Pricing](https://linkpeek.com/how-much-does-linkpeek-cost)
- [Login](https://linkpeek.com/login)
- [Support](https://linkpeek.com/contact)
- [Blog](https://linkpeek.com/blog)
- [Postman Collection](collections/linkpeek-favicon-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkpeek-favicon-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/linkpeek-meta-tags-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkpeek-meta-tags-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/linkpeek-qr-code-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkpeek-qr-code-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/linkpeek-system-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkpeek-system-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### LinkPeek Favicon API

Favicon discovery and extraction

- **Human URL:** [https://linkpeek.com/docs](https://linkpeek.com/docs)
- **Base URL:** `https://linkpeek.com/api/v1`

#### Tags

- Favicon

#### Properties

- [OpenAPI](openapi/linkpeek-favicon-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/linkpeek-favicon-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkpeek-favicon-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://github.com/dcn13l/hermes-autonomia/blob/main/linkpeek-postman.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://147.15.103.217.sslip.io)
- [Documentation](https://147.15.103.217.sslip.io/api/status)
- [API Reference](https://147.15.103.217.sslip.io/api/status)
- [Developer Portal](https://147.15.103.217.sslip.io)
- [Getting Started](https://github.com/dcn13l/hermes-autonomia#quickstart-no-signup)
- [Source Code](https://github.com/dcn13l/hermes-autonomia)

### LinkPeek Link Preview API

URL metadata and link-card extraction

- **Human URL:** [https://linkpeek.com/docs](https://linkpeek.com/docs)
- **Base URL:** `https://linkpeek.com/api/v1`

#### Tags

- Link Preview

#### Properties

- [OpenAPI](openapi/linkpeek-link-preview-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](https://github.com/dcn13l/hermes-autonomia/blob/main/linkpeek-postman.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://147.15.103.217.sslip.io)
- [Documentation](https://147.15.103.217.sslip.io/api/status)
- [API Reference](https://147.15.103.217.sslip.io/api/status)
- [Developer Portal](https://147.15.103.217.sslip.io)
- [Getting Started](https://github.com/dcn13l/hermes-autonomia#quickstart-no-signup)
- [Source Code](https://github.com/dcn13l/hermes-autonomia)

### LinkPeek Meta Tags API

HTML head meta and link tag parsing

- **Human URL:** [https://linkpeek.com/docs](https://linkpeek.com/docs)
- **Base URL:** `https://linkpeek.com/api/v1`

#### Tags

- Meta Tags

#### Properties

- [OpenAPI](openapi/linkpeek-meta-tags-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/linkpeek-meta-tags-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkpeek-meta-tags-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://github.com/dcn13l/hermes-autonomia/blob/main/linkpeek-postman.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://147.15.103.217.sslip.io)
- [Documentation](https://147.15.103.217.sslip.io/api/status)
- [API Reference](https://147.15.103.217.sslip.io/api/status)
- [Developer Portal](https://147.15.103.217.sslip.io)
- [Getting Started](https://github.com/dcn13l/hermes-autonomia#quickstart-no-signup)
- [Source Code](https://github.com/dcn13l/hermes-autonomia)

### LinkPeek QR Code API

QR code generation (PNG and base64 JSON)

- **Human URL:** [https://linkpeek.com/docs](https://linkpeek.com/docs)
- **Base URL:** `https://linkpeek.com/api/v1`

#### Tags

- QR Code

#### Properties

- [OpenAPI](openapi/linkpeek-qr-code-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/linkpeek-qr-code-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkpeek-qr-code-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://github.com/dcn13l/hermes-autonomia/blob/main/linkpeek-postman.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://147.15.103.217.sslip.io)
- [Documentation](https://147.15.103.217.sslip.io/api/status)
- [API Reference](https://147.15.103.217.sslip.io/api/status)
- [Developer Portal](https://147.15.103.217.sslip.io)
- [Getting Started](https://github.com/dcn13l/hermes-autonomia#quickstart-no-signup)
- [Source Code](https://github.com/dcn13l/hermes-autonomia)

### LinkPeek System API

Service health, status, and discovery

- **Human URL:** [https://linkpeek.com/docs](https://linkpeek.com/docs)
- **Base URL:** `https://linkpeek.com/api/v1`

#### Tags

- System

#### Properties

- [OpenAPI](openapi/linkpeek-system-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/linkpeek-system-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkpeek-system-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://github.com/dcn13l/hermes-autonomia/blob/main/linkpeek-postman.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://147.15.103.217.sslip.io)
- [Documentation](https://147.15.103.217.sslip.io/api/status)
- [API Reference](https://147.15.103.217.sslip.io/api/status)
- [Developer Portal](https://147.15.103.217.sslip.io)
- [Getting Started](https://github.com/dcn13l/hermes-autonomia#quickstart-no-signup)
- [Source Code](https://github.com/dcn13l/hermes-autonomia)

## Common Properties

- [M C P Server](mcp/linkpeek-mcp.yml)
- [Overlay](overlays/linkpeek-openapi-overlay.yaml)
- [Agentic Access](agentic-access/linkpeek-agentic-access.yml)
- [Domain Security](security/linkpeek-domain-security.yml)
- [Authentication](authentication/linkpeek-authentication.yml)
- [Packages](packages/linkpeek-packages.yml)
- [S D Ks](packages/linkpeek-packages.yml)
- [L L Ms Txt](llms/linkpeek-llms.txt)
- [Conventions](conventions/linkpeek-conventions.yml)
- [Error Catalog](errors/linkpeek-problem-types.yml)
- [Lifecycle](lifecycle/linkpeek-lifecycle.yml)
- [Conformance](conformance/linkpeek-conformance.yml)
- [Data Model](data-model/linkpeek-data-model.yml)
- [Rate Limits](rate-limits/linkpeek-rate-limits.yml)
- [Plans](plans/linkpeek-plans.yml)
- [Changelog](changelog/linkpeek-changelog.yml)
- [Changelog](https://github.com/dcn13l/hermes-autonomia/releases)
- [Agent Skill](skills/_index.yml)
- [Vulnerability Disclosure](security/linkpeek-vulnerability-disclosure.yml)
- [Security](https://github.com/dcn13l/hermes-autonomia/security)
- [GitHub Organization](https://github.com/dcn13l)
- [Support](https://github.com/dcn13l/hermes-autonomia/discussions)
- [Pricing](https://147.15.103.217.sslip.io/api/pricing)
- [Sign Up](https://147.15.103.217.sslip.io/api/key)

## Maintainers

**FN:** Russell Ballestrini
**URL:** https://linkpeek.com
**FN:** dcn13l
**URL:** https://github.com/dcn13l/hermes-autonomia
