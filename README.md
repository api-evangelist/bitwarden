# Bitwarden (bitwarden)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Bitwarden is an open-source password and secret management platform. The Bitwarden Public API exposes organization-level resources - members, groups, collections, policies, and event logs - plus a separate Vault Management API for personal vault items, an Identity (OAuth2) endpoint for token issuance, a SCIM endpoint for directory-based provisioning, and the Secrets Manager API for application secrets.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/apis.yml)

## Tags

- Security
- Password Manager
- Open Source
- Vault
- Identity
- SCIM

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-19

## APIs

### Bitwarden Public API - Members

Manages members of an organization (invite, list, retrieve, update permissions, reinvite, remove). Members are the user-side identity that owns vault items and collection grants within an organization.

- **Human URL:** [https://bitwarden.com/help/api/](https://bitwarden.com/help/api/)
- **Base URL:** `https://api.bitwarden.com/public`

#### Tags

- Members
- Users
- Public API

#### Properties

- [Documentation](https://bitwarden.com/help/api/)
- [OpenAPI](openapi/bitwarden-public-swagger.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bitwarden-public-swagger.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bitwarden-public-swagger.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bitwarden Public API - Groups

Manages organization groups - collections of members granted shared collection access. Supports create, list, retrieve, update, delete, and member-membership operations.

- **Human URL:** [https://bitwarden.com/help/api/#tag/Groups](https://bitwarden.com/help/api/#tag/Groups)
- **Base URL:** `https://api.bitwarden.com/public`

#### Tags

- Groups
- Permissions
- Public API

#### Properties

- [Documentation](https://bitwarden.com/help/api/#tag/Groups)
- [OpenAPI](openapi/bitwarden-public-swagger.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bitwarden-public-swagger.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bitwarden-public-swagger.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bitwarden Public API - Collections

Manages collections (logical groupings of vault items shared with groups and members). Supports list, retrieve, update assignments, and delete; create is typically handled in the client. Includes default-collection management.

- **Human URL:** [https://bitwarden.com/help/api/#tag/Collections](https://bitwarden.com/help/api/#tag/Collections)
- **Base URL:** `https://api.bitwarden.com/public`

#### Tags

- Collections
- Sharing
- Public API

#### Properties

- [Documentation](https://bitwarden.com/help/api/#tag/Collections)
- [OpenAPI](openapi/bitwarden-public-swagger.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bitwarden-public-swagger.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bitwarden-public-swagger.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bitwarden Public API - Policies

Reads and updates enterprise policies (Two-Step Login, Master Password requirements, Send disable, Single Org, Personal Ownership, Password Generator, etc.). Available on Enterprise.

- **Human URL:** [https://bitwarden.com/help/api/#tag/Policies](https://bitwarden.com/help/api/#tag/Policies)
- **Base URL:** `https://api.bitwarden.com/public`

#### Tags

- Policies
- Enterprise
- Public API

#### Properties

- [Documentation](https://bitwarden.com/help/api/#tag/Policies)
- [OpenAPI](openapi/bitwarden-public-swagger.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bitwarden-public-swagger.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bitwarden-public-swagger.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bitwarden Public API - Event Logs

Retrieves organization activity events (60+ numeric event types covering member, vault item, collection, group, and policy actions). Returns paginated lists with a continuationToken; data is retained indefinitely.

- **Human URL:** [https://bitwarden.com/help/event-logs/](https://bitwarden.com/help/event-logs/)
- **Base URL:** `https://api.bitwarden.com/public`

#### Tags

- Events
- Audit Logs
- Compliance
- Public API

#### Properties

- [Documentation](https://bitwarden.com/help/event-logs/)
- [OpenAPI](openapi/bitwarden-public-swagger.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bitwarden-public-swagger.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bitwarden-public-swagger.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bitwarden Identity API

OAuth2 / OpenID Connect token endpoint that issues bearer tokens for the Public API and Vault Management API. Organization API keys use the client_credentials grant with scope api.organization; bearer tokens are valid for 3600 seconds.

- **Human URL:** [https://bitwarden.com/help/public-api/](https://bitwarden.com/help/public-api/)
- **Base URL:** `https://identity.bitwarden.com/connect/token`

#### Tags

- Identity
- OAuth
- Authentication

#### Properties

- [Documentation](https://bitwarden.com/help/public-api/)
- [Postman Collection](collections/bitwarden-public-swagger.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bitwarden-public-swagger.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bitwarden SCIM API

SCIM 2.0 endpoint for directory-driven provisioning of users and groups (used by Okta, Entra ID, OneLogin, JumpCloud, Google Workspace via SCIM). Supports automatic invite, update, and offboard flows on Teams and Enterprise.

- **Human URL:** [https://bitwarden.com/help/scim/](https://bitwarden.com/help/scim/)
- **Base URL:** `https://scim.bitwarden.com/v2`

#### Tags

- SCIM
- Provisioning
- Identity

#### Properties

- [Documentation](https://bitwarden.com/help/scim/)
- [Postman Collection](collections/bitwarden-public-swagger.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bitwarden-public-swagger.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bitwarden Vault Management API

Local Bitwarden CLI HTTP API for managing personal vault items, folders, sends, collections, organizations, the generator, and miscellaneous operations. Exposed by the bw CLI in serve mode and intended for local automation rather than remote access.

- **Human URL:** [https://bitwarden.com/help/vault-management-api/](https://bitwarden.com/help/vault-management-api/)
- **Base URL:** `http://localhost:8087`

#### Tags

- Vault Items
- CLI
- Local

#### Properties

- [Documentation](https://bitwarden.com/help/vault-management-api/)
- [Postman Collection](collections/bitwarden-public-swagger.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bitwarden-public-swagger.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bitwarden Secrets Manager API

Secrets Manager API for storing and retrieving application secrets and managing projects, service accounts, secrets, and access tokens used by infrastructure and developer tooling.

- **Human URL:** [https://bitwarden.com/help/secrets-manager-overview/](https://bitwarden.com/help/secrets-manager-overview/)
- **Base URL:** `https://api.bitwarden.com`

#### Tags

- Secrets Manager
- Secrets
- DevOps

#### Properties

- [Documentation](https://bitwarden.com/help/secrets-manager-overview/)
- [Postman Collection](collections/bitwarden-public-swagger.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bitwarden-public-swagger.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/bitwarden)
- [LinkedIn](https://www.linkedin.com/company/bitwarden1)
- [Website](https://bitwarden.com/)
- [Documentation](https://bitwarden.com/help/public-api/)
- [API Reference](https://bitwarden.com/help/api/)
- [Plans](plans/bitwarden-plans-pricing.yml)
- [Rate Limits](rate-limits/bitwarden-rate-limits.yml)
- [Fin Ops](finops/bitwarden-finops.yml)
- [Integrations](https://bitwarden.com/integrations/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
