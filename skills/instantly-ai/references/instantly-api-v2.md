# Instantly API v2 Reference

Verified against Instantly official documentation on 2026-03-30.

## Current status

- Current published API generation: `v2`.
- API v1 was deprecated on **January 19, 2026**. New integrations should target `v2`.
- Published surface captured in this snapshot: **29 resource groups** and **166 resource endpoints** from the official group pages.

## Secure authentication

- Create a dedicated API key in Instantly integrations settings and grant only the scopes needed for the integration.
- Instantly documents that the key is shown only once when created. Store it immediately in a secure secret store or a local `.env` file that is not committed.
- Use Bearer auth with the `authorization` header: `Bearer ${INSTANTLY_API_KEY}`.
- Never hardcode the key in source, tests, notebooks, screenshots, or sample payloads.
- Prefer one key per service or environment so rotation is isolated.

### Safe defaults

- Base URL: `https://api.instantly.ai`
- Version prefix: `/api/v2`
- Auth header: `authorization: Bearer ${INSTANTLY_API_KEY}`
- Secret name: `INSTANTLY_API_KEY`
- Logging rule: redact `authorization` and any copied curl commands before sharing logs.

## Rate limits

- Limits are shared across API v1 and API v2.
- Limits apply at the **workspace** level, even if multiple API keys are used.
- Instantly documents two hard limits: **100 requests per second** and **6,000 requests per minute**.
- If either limit is exceeded, requests fail with `429`.
- Instantly recommends batching large jobs and waiting between batches rather than sending bursts.

## Working model

- Choose the resource group first, then the exact endpoint.
- Expect a mix of CRUD APIs, analytics reads, bulk operations, webhook-driven workflows, and background-job style flows.
- Treat workspace, API key, billing, and ownership endpoints as high-blast-radius operations.
- For webhook consumers, make handlers idempotent and resilient to retries or duplicates.

## Resource map

| Resource group | Endpoints | What it covers |
| --- | ---: | --- |
| [Account](https://developer.instantly.ai/api-reference/groups/account) | 12 | An email account that can be used to send campaigns |
| [Account Campaign Mapping](https://developer.instantly.ai/api-reference/groups/account-campaign-mapping) | 1 | Account Campaign Mapping |
| [Analytics](https://developer.instantly.ai/api-reference/groups/analytics) | 7 | Endpoints related to analytics |
| [API Key](https://developer.instantly.ai/api-reference/groups/api-key) | 3 | API Key |
| [Audit Log](https://developer.instantly.ai/api-reference/groups/audit-log) | 1 | Audit log records for tracking system activities |
| [Background Job](https://developer.instantly.ai/api-reference/groups/background-job) | 2 | A background job that can be used to perform long-running tasks |
| [Block List Entry](https://developer.instantly.ai/api-reference/groups/block-list-entry) | 9 | A blocked email or domain |
| [Campaign](https://developer.instantly.ai/api-reference/groups/campaign) | 15 | A campaign that can be sent to a list of recipients |
| [Campaign Subsequence](https://developer.instantly.ai/api-reference/groups/campaign-subsequence) | 9 | A subsequence entity representing a follow-up sequence |
| [CRM Actions](https://developer.instantly.ai/api-reference/groups/crm-actions) | 2 | CRM related actions |
| [Custom Tag](https://developer.instantly.ai/api-reference/groups/custom-tag) | 6 | A custom tag for organizing and categorizing accounts and campaigns. You can use them as filters in apis that list accounts and campaigns. |
| [Custom Tag Mapping](https://developer.instantly.ai/api-reference/groups/custom-tag-mapping) | 1 | This entity represents a tag being assigned to a specific campaign or email account. |
| [DFY Email Account Order](https://developer.instantly.ai/api-reference/groups/dfy-email-account-order) | 7 | A Done-For-You email account order |
| [Email](https://developer.instantly.ai/api-reference/groups/email) | 9 | A campaign email, a reply, a manually sent email, or any other email that's visible in the Unibox |
| [Email Verification](https://developer.instantly.ai/api-reference/groups/email-verification) | 2 | A single email verification |
| [Inbox Placement Analytics](https://developer.instantly.ai/api-reference/groups/inbox-placement-analytics) | 5 | Analytics data for individual emails in inbox placement tests |
| [Inbox Placement Blacklist & SpamAssassin Report](https://developer.instantly.ai/api-reference/groups/inbox-placement-reports) | 1 | Report data for an inbox placement test |
| [Inbox Placement Test](https://developer.instantly.ai/api-reference/groups/inbox-placement-test) | 6 | An inbox placement test |
| [Lead](https://developer.instantly.ai/api-reference/groups/lead) | 13 | A lead entity representing an individual lead |
| [Lead Label](https://developer.instantly.ai/api-reference/groups/lead-label) | 6 | A custom label for categorizing and managing leads |
| [Lead List](https://developer.instantly.ai/api-reference/groups/lead-list) | 6 | A list used to store leads |
| [OAuth](https://developer.instantly.ai/api-reference/groups/oauth) | 3 | OAuth authentication endpoints for connecting Google and Microsoft email accounts |
| [SuperSearch Enrichment](https://developer.instantly.ai/api-reference/groups/supersearch-enrichment) | 10 | An enrichment can take different forms, including standard data enrichment and AI-powered enrichment. |
| [Webhook](https://developer.instantly.ai/api-reference/groups/webhook) | 8 | A webhook subscription for receiving event notifications |
| [Webhook Event](https://developer.instantly.ai/api-reference/groups/webhook-event) | 4 | A webhook event that was sent or attempted to be sent |
| [Workspace](https://developer.instantly.ai/api-reference/groups/workspace) | 6 | A workspace entity representing a workspace |
| [Workspace Billing](https://developer.instantly.ai/api-reference/groups/workspace-billing) | 2 | Workspace Billing |
| [Workspace Group Member](https://developer.instantly.ai/api-reference/groups/workspace-group-member) | 5 | A member of a workspace group. |
| [Workspace Member](https://developer.instantly.ai/api-reference/groups/workspace-member) | 5 | A member of a workspace with associated user details |

## Common task mapping

- Campaign creation and sending: start with `Campaign`, then pair with `Account`, `Lead`, `Lead List`, `Lead Label`, and `Campaign Subsequence` as needed.
- Sending-account operations: use `Account`, `OAuth`, `DFY Email Account Order`, `Workspace`, and member/group resources.
- Inbox and reply flows: use `Email`, `Webhook`, and `Webhook Event`.
- Reporting and health: use `Analytics`, `Campaign`, `Account`, `Inbox Placement Test`, `Inbox Placement Analytics`, `Inbox Placement Reports`, and `Audit Log`.
- CRM and enrichment workflows: use `SuperSearch Enrichment`, `CRM Actions`, `Lead`, and `Lead List`.

## Sources

- Introduction: https://developer.instantly.ai/api-reference/introduction
- Getting started: https://developer.instantly.ai/getting-started/getting-started
- Authorization: https://developer.instantly.ai/getting-started/authorization
- Rate limits: https://developer.instantly.ai/getting-started/rate-limit
- API v1 migration: https://developer.instantly.ai/guides/api-v1-migration
- Webhook events guide: https://developer.instantly.ai/guides/webhook-events
- OAuth connection flow: https://developer.instantly.ai/guides/oauth-connection-flow
- Workspace group guide: https://developer.instantly.ai/guides/workspace-group
- Sitemap: https://developer.instantly.ai/sitemap.xml
