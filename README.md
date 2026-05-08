# Bitwarden (bitwarden)

Bitwarden is an open-source password and secret management platform. The Bitwarden Public API exposes organization-level resources - members, groups, collections, policies, and event logs - plus a separate Vault Management API for personal vault items, an Identity (OAuth2) endpoint for token issuance, a SCIM endpoint for directory-based provisioning, and the Secrets Manager API for application secrets.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=bitwarden-api-evangelist&utm_content=repo)

## Type

- **x-type:** company

## Tags

- Security, Password Manager, Open Source, Vault, Identity, SCIM

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-08

## APIs

| API | Description |
|---|---|
| Bitwarden Public API - Members | Invite, list, retrieve, update, reinvite, and remove organization members. |
| Bitwarden Public API - Groups | Manage organization groups and their member memberships. |
| Bitwarden Public API - Collections | Manage shared collections and their assignments to groups and members. |
| Bitwarden Public API - Policies | Read and update enterprise policies (Two-Step Login, Master Password, Send disable, etc.). |
| Bitwarden Public API - Event Logs | Retrieve organization activity events with continuationToken pagination. |
| Bitwarden Identity API | OAuth2 token endpoint for client_credentials flow with scope api.organization. |
| Bitwarden SCIM API | SCIM 2.0 directory-driven provisioning of users and groups. |
| Bitwarden Vault Management API | Local CLI HTTP API exposed by `bw serve` for personal vault items, folders, and sends. |
| Bitwarden Secrets Manager API | Application-secret management with projects, service accounts, secrets, and access tokens. |

## Cloud Regions

- **US:** https://api.bitwarden.com (identity at https://identity.bitwarden.com)
- **EU:** https://api.bitwarden.eu (identity at https://identity.bitwarden.eu)
- **Self-Hosted:** https://your.domain.com/api

## Common Properties

- [Website](https://bitwarden.com/)
- [Documentation](https://bitwarden.com/help/public-api/)
- [API Reference](https://bitwarden.com/help/api/)
- [Plans](plans/bitwarden-plans-pricing.yml) - API Commons Plans 0.1
- [RateLimits](rate-limits/bitwarden-rate-limits.yml) - API Commons Rate Limits 0.1
- [FinOps](finops/bitwarden-finops.yml) - FOCUS-aligned FinOps Framework 1.0

## Plans

- **Free** - Personal; unlimited devices and items; no API access.
- **Premium** - $9.99/year; integrated TOTP, file attachments, emergency access; no API access.
- **Families** - $40/year for up to 6 users; unlimited sharing.
- **Teams** - $4/user/month annual; Public API, SCIM, directory connector, event logs.
- **Enterprise** - $6/user/month annual; SSO, enterprise policies, account recovery, self-host, complimentary Families per user.
- **Secrets Manager (Add-On)** - Sold separately; per-user-per-month with included machine accounts.

## Rate Limits

- 429 Too Many Requests on dynamic per-client throttling.
- Lists exceeding 50 results return a continuationToken.
- Identity bearer tokens are valid for 3600 seconds; reuse them.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
