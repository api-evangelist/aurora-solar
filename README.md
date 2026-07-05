# Aurora Solar (aurora-solar)

Aurora Solar is a cloud platform for solar sales and design. It provides remote shading analysis, LIDAR and satellite-based roof modeling, PV system design, performance simulation, financing, and proposal generation so installers can design and sell solar projects without a site visit. The Aurora API (v2024.05) is a tenant-scoped REST API secured with API-key bearer tokens that lets integrations manage projects, request and retrieve designs, generate proposals, pull consumption profiles, manage users and webhooks, and push financings and agreements.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/aurora-solar/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/aurora-solar/refs/heads/main/apis.yml)

## Tags

- Solar
- Solar Design
- PV
- Proposals
- CleanTech
- Energy
- Sales Software

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## Authentication & Base URL

- **Production base URL:** `https://api.aurorasolar.com`
- **Sandbox base URL:** `https://api-sandbox.aurorasolar.com`
- **Auth:** API-key bearer token, `Authorization: Bearer <token>`. Standard keys are prefixed `sk_`, Restricted keys `rk_`; `sand_`/`prod_` denote the environment. Keys are managed on the tenant's API Tokens screen (`v2.aurorasolar.com/settings/api/tokens`).
- **Versioning:** current version `v2024.05` (selected via the `Aurora-Version` header).
- Every resource is scoped to a tenant under `/tenants/{tenant_id}`.

## APIs

### Aurora Solar Projects API

Create, retrieve, update, list, and delete projects - the customer/site records that anchor every design and proposal in Aurora. Includes project assets and the authority-having-jurisdiction (AHJ) lookup. Scoped to a tenant at `/tenants/{tenant_id}/projects`.

- **Human URL:** [https://docs.aurorasolar.com/reference/listprojects](https://docs.aurorasolar.com/reference/listprojects)
- **Base URL:** `https://api.aurorasolar.com`

#### Tags

- Projects
- Customers
- Sites

#### Properties

- [Documentation](https://docs.aurorasolar.com/reference/aurora-solar-api)
- [API Reference](https://docs.aurorasolar.com/reference/listprojects)
- [OpenAPI](openapi/aurora-solar-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/aurora-solar.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/aurora-solar.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Aurora Solar Designs API

Submit design requests (including AutoDesigner and EagleView flows), accept them, then create and retrieve full PV designs with racking arrays, roof and system-loss summaries, bill-of-materials, and performance-simulation outputs.

- **Human URL:** [https://docs.aurorasolar.com/reference/createdesignrequest](https://docs.aurorasolar.com/reference/createdesignrequest)
- **Base URL:** `https://api.aurorasolar.com`

#### Tags

- Designs
- Design Requests
- Simulation

#### Properties

- [Documentation](https://docs.aurorasolar.com/reference/aurora-solar-api)
- [API Reference](https://docs.aurorasolar.com/reference/createdesignrequest)
- [OpenAPI](openapi/aurora-solar-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/aurora-solar.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/aurora-solar.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Aurora Solar Proposals API

Create, retrieve, and delete customer-facing proposals, list and retrieve proposal templates, generate a hosted web proposal URL from a design, and run/retrieve proposal PDF generation.

- **Human URL:** [https://docs.aurorasolar.com/reference/aurora-solar-api](https://docs.aurorasolar.com/reference/aurora-solar-api)
- **Base URL:** `https://api.aurorasolar.com`

#### Tags

- Proposals
- Sales
- Web Proposal

#### Properties

- [Documentation](https://docs.aurorasolar.com/reference/aurora-solar-api)
- [OpenAPI](openapi/aurora-solar-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/aurora-solar.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/aurora-solar.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Aurora Solar Consumption Profiles API

Retrieve and update a project's energy consumption profile, and manage the utility bills that drive it - list and retrieve bills plus run and check utility-bill upload (OCR) status.

- **Human URL:** [https://docs.aurorasolar.com/reference/aurora-solar-api](https://docs.aurorasolar.com/reference/aurora-solar-api)
- **Base URL:** `https://api.aurorasolar.com`

#### Tags

- Consumption
- Energy Usage
- Utility Bills

#### Properties

- [Documentation](https://docs.aurorasolar.com/reference/aurora-solar-api)
- [OpenAPI](openapi/aurora-solar-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/aurora-solar.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/aurora-solar.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Aurora Solar Users & Tenants API

Retrieve the tenant, manage users (create, invite, retrieve, update, activate, deactivate), list roles and teams, and configure SSO providers for a tenant.

- **Human URL:** [https://docs.aurorasolar.com/reference/aurora-solar-api](https://docs.aurorasolar.com/reference/aurora-solar-api)
- **Base URL:** `https://api.aurorasolar.com`

#### Tags

- Users
- Tenants
- Teams
- SSO

#### Properties

- [Documentation](https://docs.aurorasolar.com/reference/aurora-solar-api)
- [OpenAPI](openapi/aurora-solar-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/aurora-solar.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/aurora-solar.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Aurora Solar Webhooks API

Create, list, retrieve, update, and delete webhooks so Aurora can push event notifications (project, design, and async job lifecycle events) to your endpoints instead of you polling.

- **Human URL:** [https://docs.aurorasolar.com/reference/createwebhook](https://docs.aurorasolar.com/reference/createwebhook)
- **Base URL:** `https://api.aurorasolar.com`

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [Documentation](https://docs.aurorasolar.com/reference/aurora-solar-api)
- [API Reference](https://docs.aurorasolar.com/reference/createwebhook)
- [OpenAPI](openapi/aurora-solar-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/aurora-solar.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/aurora-solar.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Aurora Solar Financings API

List and retrieve financings, push a financing to a financier, and share a financing milestone - integrating Aurora deals with lending partners.

- **Human URL:** [https://docs.aurorasolar.com/reference/aurora-solar-api](https://docs.aurorasolar.com/reference/aurora-solar-api)
- **Base URL:** `https://api.aurorasolar.com`

#### Tags

- Financings
- Financiers
- Milestones

#### Properties

- [Documentation](https://docs.aurorasolar.com/reference/aurora-solar-api)
- [OpenAPI](openapi/aurora-solar-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/aurora-solar.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/aurora-solar.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Aurora Solar Agreements API

List and retrieve customer agreements, get a hosted agreement link, and run/retrieve generation of a signed-agreement download URL.

- **Human URL:** [https://docs.aurorasolar.com/reference/aurora-solar-api](https://docs.aurorasolar.com/reference/aurora-solar-api)
- **Base URL:** `https://api.aurorasolar.com`

#### Tags

- Agreements
- Contracts
- E-Signature

#### Properties

- [Documentation](https://docs.aurorasolar.com/reference/aurora-solar-api)
- [OpenAPI](openapi/aurora-solar-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/aurora-solar.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/aurora-solar.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/aurorasolar)
- [LinkedIn](https://www.linkedin.com/company/aurorasolar)
- [Website](https://aurorasolar.com)
- [Documentation](https://docs.aurorasolar.com)
- [Plans](plans/aurora-solar-plans-pricing.yml)
- [Rate Limits](rate-limits/aurora-solar-rate-limits.yml)
- [Fin Ops](finops/aurora-solar-finops.yml)
- [Blog](https://aurorasolar.com/blog/)

## Review

- **Question:** Does Aurora Solar expose a documented public WebSocket API?
- **Answer:** No. The Aurora API is request/response REST over HTTPS. Real-time delivery is via outbound webhooks, and long-running design work uses asynchronous submit-then-poll endpoints. No WebSocket (ws/wss) or SSE surface is documented. See [review.yml](review.yml).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
