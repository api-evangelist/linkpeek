# LinkPeek (linkpeek)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
