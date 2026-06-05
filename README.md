# Bitwarden (bitwarden)

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
