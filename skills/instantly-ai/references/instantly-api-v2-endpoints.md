# Instantly API v2 Endpoint Catalog

Generated from Instantly official API reference group pages on 2026-03-30.

Total resource groups: **29**

## Account

- Docs: https://developer.instantly.ai/api-reference/groups/account
- Scope: An email account that can be used to send campaigns
- Related schemas: [Account](https://developer.instantly.ai/api-reference/schemas/account)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/accounts` | Create account |
| `GET` | `/api/v2/accounts` | List account |
| `GET` | `/api/v2/accounts/{email}` | Get account |
| `PATCH` | `/api/v2/accounts/{email}` | Patch account |
| `DELETE` | `/api/v2/accounts/{email}` | Delete account |
| `POST` | `/api/v2/accounts/warmup/enable` | Enable warmup for accounts |
| `POST` | `/api/v2/accounts/warmup/disable` | Disable warmup for accounts |
| `POST` | `/api/v2/accounts/{email}/pause` | Pause an account |
| `POST` | `/api/v2/accounts/{email}/resume` | Resume a paused account |
| `POST` | `/api/v2/accounts/{email}/mark-fixed` | Mark an account as fixed |
| `GET` | `/api/v2/accounts/ctd/status` | Get custom tracking domain status |
| `POST` | `/api/v2/accounts/move` | Move accounts between workspaces |

## Account Campaign Mapping

- Docs: https://developer.instantly.ai/api-reference/groups/account-campaign-mapping
- Scope: Account Campaign Mapping
- Related schemas: [Account Campaign Mapping](https://developer.instantly.ai/api-reference/schemas/account-campaign-mapping)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/account-campaign-mappings/{email}` | Get campaigns associated with an email |

## Analytics

- Docs: https://developer.instantly.ai/api-reference/groups/analytics
- Scope: Endpoints related to analytics

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/accounts/warmup-analytics` | Get warmup analytics |
| `GET` | `/api/v2/accounts/analytics/daily` | Get daily account analytics |
| `POST` | `/api/v2/accounts/test/vitals` | Test account vitals |
| `GET` | `/api/v2/campaigns/analytics` | Get campaign(s) analytics |
| `GET` | `/api/v2/campaigns/analytics/overview` | Get campaign(s) analytics overview |
| `GET` | `/api/v2/campaigns/analytics/daily` | Get daily campaign analytics |
| `GET` | `/api/v2/campaigns/analytics/steps` | Get campaign steps analytics |

## API Key

- Docs: https://developer.instantly.ai/api-reference/groups/api-key
- Scope: API Key
- Related schemas: [API Key](https://developer.instantly.ai/api-reference/schemas/api-key)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/api-keys` | Create api key |
| `GET` | `/api/v2/api-keys` | List api key |
| `DELETE` | `/api/v2/api-keys/{id}` | Delete api key |

## Audit Log

- Docs: https://developer.instantly.ai/api-reference/groups/audit-log
- Scope: Audit log records for tracking system activities
- Related schemas: [Audit Log](https://developer.instantly.ai/api-reference/schemas/audit-log)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/audit-logs` | List audit log |

## Background Job

- Docs: https://developer.instantly.ai/api-reference/groups/background-job
- Scope: A background job that can be used to perform long-running tasks
- Related schemas: [Background Job](https://developer.instantly.ai/api-reference/schemas/background-job)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/background-jobs` | List background job |
| `GET` | `/api/v2/background-jobs/{id}` | Get background job |

## Block List Entry

- Docs: https://developer.instantly.ai/api-reference/groups/block-list-entry
- Scope: A blocked email or domain
- Related schemas: [Block List Entry](https://developer.instantly.ai/api-reference/schemas/block-list-entry)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/block-lists-entries` | Create block list entry |
| `GET` | `/api/v2/block-lists-entries` | List block list entry |
| `GET` | `/api/v2/block-lists-entries/{id}` | Get block list entry |
| `PATCH` | `/api/v2/block-lists-entries/{id}` | Patch block list entry |
| `DELETE` | `/api/v2/block-lists-entries/{id}` | Delete block list entry |
| `DELETE` | `/api/v2/block-lists-entries` | Delete all block list entries |
| `POST` | `/api/v2/block-lists-entries/bulk-create` | Bulk create block list entry |
| `POST` | `/api/v2/block-lists-entries/bulk-delete` | Bulk delete block list entry |
| `GET` | `/api/v2/block-lists-entries/download` | Download all block list entries as CSV |

## Campaign

- Docs: https://developer.instantly.ai/api-reference/groups/campaign
- Scope: A campaign that can be sent to a list of recipients
- Related schemas: [Campaign](https://developer.instantly.ai/api-reference/schemas/campaign)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/campaigns` | Create campaign |
| `GET` | `/api/v2/campaigns` | List campaign |
| `GET` | `/api/v2/campaigns/{id}` | Get campaign |
| `PATCH` | `/api/v2/campaigns/{id}` | Patch campaign |
| `DELETE` | `/api/v2/campaigns/{id}` | Delete campaign |
| `POST` | `/api/v2/campaigns/{id}/activate` | Activate(start), or resume a campaign |
| `POST` | `/api/v2/campaigns/{id}/pause` | Stop(or pause) a campaign |
| `GET` | `/api/v2/campaigns/search-by-contact` | Search campaigns by lead email |
| `POST` | `/api/v2/campaigns/{id}/share` | Share a campaign |
| `POST` | `/api/v2/campaigns/{id}/from-export` | Create campaign from shared one |
| `POST` | `/api/v2/campaigns/{id}/export` | Export campaign to JSON format |
| `POST` | `/api/v2/campaigns/{id}/duplicate` | Duplicate campaign |
| `GET` | `/api/v2/campaigns/count-launched` | Get launched campaigns count |
| `POST` | `/api/v2/campaigns/{id}/variables` | Add campaign variables |
| `GET` | `/api/v2/campaigns/{id}/sending-status` | Get campaign sending status |

## Campaign Subsequence

- Docs: https://developer.instantly.ai/api-reference/groups/campaign-subsequence
- Scope: A subsequence entity representing a follow-up sequence
- Related schemas: [Campaign Subsequence](https://developer.instantly.ai/api-reference/schemas/campaign-subsequence)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/subsequences` | Create campaign subsequence |
| `GET` | `/api/v2/subsequences` | List campaign subsequence |
| `GET` | `/api/v2/subsequences/{id}` | Get campaign subsequence |
| `PATCH` | `/api/v2/subsequences/{id}` | Patch campaign subsequence |
| `DELETE` | `/api/v2/subsequences/{id}` | Delete campaign subsequence |
| `POST` | `/api/v2/subsequences/{id}/duplicate` | Duplicate a subsequence |
| `POST` | `/api/v2/subsequences/{id}/pause` | Pause a subsequence |
| `POST` | `/api/v2/subsequences/{id}/resume` | Resume a paused subsequence |
| `GET` | `/api/v2/subsequences/{id}/sending-status` | Get subsequence sending status |

## CRM Actions

- Docs: https://developer.instantly.ai/api-reference/groups/crm-actions
- Scope: CRM related actions
- Related schemas: [CRM Actions](https://developer.instantly.ai/api-reference/schemas/crm-actions)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/crm-actions/phone-numbers` | List phone numbers |
| `DELETE` | `/api/v2/crm-actions/phone-numbers/{id}` | Delete phone number |

## Custom Tag

- Docs: https://developer.instantly.ai/api-reference/groups/custom-tag
- Scope: A custom tag for organizing and categorizing accounts and campaigns. You can use them as filters in apis that list accounts and campaigns.
- Related schemas: [Custom Tag](https://developer.instantly.ai/api-reference/schemas/custom-tag)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/custom-tags` | Create custom tag |
| `GET` | `/api/v2/custom-tags` | List custom tag |
| `GET` | `/api/v2/custom-tags/{id}` | Get custom tag |
| `PATCH` | `/api/v2/custom-tags/{id}` | Patch custom tag |
| `DELETE` | `/api/v2/custom-tags/{id}` | Delete custom tag |
| `POST` | `/api/v2/custom-tags/toggle-resource` | Assign or unassign tags to resources |

## Custom Tag Mapping

- Docs: https://developer.instantly.ai/api-reference/groups/custom-tag-mapping
- Scope: This entity represents a tag being assigned to a specific campaign or email account.
- Related schemas: [Custom Tag Mapping](https://developer.instantly.ai/api-reference/schemas/custom-tag-mapping)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/custom-tag-mappings` | List custom tag mapping |

## DFY Email Account Order

- Docs: https://developer.instantly.ai/api-reference/groups/dfy-email-account-order
- Scope: A Done-For-You email account order
- Related schemas: [DFY Email Account Order](https://developer.instantly.ai/api-reference/schemas/dfy-email-account-order)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/dfy-email-account-orders` | Place a DFY email account order |
| `GET` | `/api/v2/dfy-email-account-orders` | List dfy email account order |
| `POST` | `/api/v2/dfy-email-account-orders/domains/similar` | Generate similar available domains |
| `POST` | `/api/v2/dfy-email-account-orders/domains/check` | Check domains availability |
| `POST` | `/api/v2/dfy-email-account-orders/domains/pre-warmed-up-list` | Get pre-warmed up domains |
| `GET` | `/api/v2/dfy-email-account-orders/accounts` | List DFY ordered email accounts |
| `POST` | `/api/v2/dfy-email-account-orders/accounts/cancel` | Cancel dfy email accounts |

## Email

- Docs: https://developer.instantly.ai/api-reference/groups/email
- Scope: A campaign email, a reply, a manually sent email, or any other email that's visible in the Unibox
- Related schemas: [Email](https://developer.instantly.ai/api-reference/schemas/email)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/emails/test` | Send a test email |
| `POST` | `/api/v2/emails/reply` | Reply to an email |
| `POST` | `/api/v2/emails/forward` | Forward an email |
| `GET` | `/api/v2/emails` | List email |
| `GET` | `/api/v2/emails/{id}` | Get email |
| `PATCH` | `/api/v2/emails/{id}` | Patch email |
| `DELETE` | `/api/v2/emails/{id}` | Delete email |
| `GET` | `/api/v2/emails/unread/count` | Count unread emails |
| `POST` | `/api/v2/emails/threads/{thread_id}/mark-as-read` | Mark all emails in a thread as read |

## Email Verification

- Docs: https://developer.instantly.ai/api-reference/groups/email-verification
- Scope: A single email verification
- Related schemas: [Email Verification](https://developer.instantly.ai/api-reference/schemas/email-verification)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/email-verification` | Create email verification |
| `GET` | `/api/v2/email-verification/{email}` | Check an email verification status |

## Inbox Placement Analytics

- Docs: https://developer.instantly.ai/api-reference/groups/inbox-placement-analytics
- Scope: Analytics data for individual emails in inbox placement tests
- Related schemas: [Inbox Placement Analytics](https://developer.instantly.ai/api-reference/schemas/inbox-placement-analytics)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/inbox-placement-analytics` | List inbox placement analytics |
| `GET` | `/api/v2/inbox-placement-analytics/{id}` | Get inbox placement analytics |
| `POST` | `/api/v2/inbox-placement-analytics/stats-by-test-id` | Retrieve inbox placement analytics stats by test id |
| `POST` | `/api/v2/inbox-placement-analytics/deliverability-insights` | Retrieve inbox placement analytics deliverability insights |
| `POST` | `/api/v2/inbox-placement-analytics/stats-by-date` | Get inbox placement analytics stats by date |

## Inbox Placement Blacklist & SpamAssassin Report

- Docs: https://developer.instantly.ai/api-reference/groups/inbox-placement-reports
- Scope: Report data for an inbox placement test
- Related schemas: [Endpoints](https://developer.instantly.ai/api-reference/schemas/inbox-placement-blacklist-spamassassin-report)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/inbox-placement-reports` | GET |

## Inbox Placement Test

- Docs: https://developer.instantly.ai/api-reference/groups/inbox-placement-test
- Scope: An inbox placement test
- Related schemas: [Inbox Placement Test](https://developer.instantly.ai/api-reference/schemas/inbox-placement-test)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/inbox-placement-tests` | Create inbox placement test |
| `GET` | `/api/v2/inbox-placement-tests` | List inbox placement test |
| `GET` | `/api/v2/inbox-placement-tests/{id}` | Get inbox placement test |
| `PATCH` | `/api/v2/inbox-placement-tests/{id}` | Patch inbox placement test |
| `DELETE` | `/api/v2/inbox-placement-tests/{id}` | Delete inbox placement test |
| `GET` | `/api/v2/inbox-placement-tests/email-service-provider-options` | Get ESP options |

## Lead

- Docs: https://developer.instantly.ai/api-reference/groups/lead
- Scope: A lead entity representing an individual lead
- Related schemas: [Lead](https://developer.instantly.ai/api-reference/schemas/lead)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/leads` | Create lead |
| `DELETE` | `/api/v2/leads` | Delete leads in bulk |
| `POST` | `/api/v2/leads/list` | List leads |
| `GET` | `/api/v2/leads/{id}` | Get lead |
| `PATCH` | `/api/v2/leads/{id}` | Patch lead |
| `DELETE` | `/api/v2/leads/{id}` | Delete lead |
| `POST` | `/api/v2/leads/merge` | Merge two leads |
| `POST` | `/api/v2/leads/update-interest-status` | Update the interest status of a lead |
| `POST` | `/api/v2/leads/subsequence/remove` | Remove a lead from a subsequence |
| `POST` | `/api/v2/leads/bulk-assign` | Bulk assign leads to organization users |
| `POST` | `/api/v2/leads/move` | Move leads to a campaign or list |
| `POST` | `/api/v2/leads/subsequence/move` | Move a lead to a subsequence |
| `POST` | `/api/v2/leads/add` | Add leads in bulk to a campaign or list |

## Lead Label

- Docs: https://developer.instantly.ai/api-reference/groups/lead-label
- Scope: A custom label for categorizing and managing leads
- Related schemas: [Lead Label](https://developer.instantly.ai/api-reference/schemas/lead-label)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/lead-labels` | Create lead label |
| `GET` | `/api/v2/lead-labels` | List lead label |
| `GET` | `/api/v2/lead-labels/{id}` | Get lead label |
| `PATCH` | `/api/v2/lead-labels/{id}` | Patch lead label |
| `DELETE` | `/api/v2/lead-labels/{id}` | Delete lead label |
| `POST` | `/api/v2/lead-labels/ai-reply-label` | Test AI reply label prediction |

## Lead List

- Docs: https://developer.instantly.ai/api-reference/groups/lead-list
- Scope: A list used to store leads
- Related schemas: [Lead List](https://developer.instantly.ai/api-reference/schemas/lead-list)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/lead-lists` | Create lead list |
| `GET` | `/api/v2/lead-lists` | List lead list |
| `GET` | `/api/v2/lead-lists/{id}` | Get lead list |
| `PATCH` | `/api/v2/lead-lists/{id}` | Patch lead list |
| `DELETE` | `/api/v2/lead-lists/{id}` | Delete lead list |
| `GET` | `/api/v2/lead-lists/{id}/verification-stats` | Get verification statistics for a lead list |

## OAuth

- Docs: https://developer.instantly.ai/api-reference/groups/oauth
- Scope: OAuth authentication endpoints for connecting Google and Microsoft email accounts

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/oauth/google/init` | Initialize google oauth |
| `POST` | `/api/v2/oauth/microsoft/init` | Initialize microsoft oauth |
| `GET` | `/api/v2/oauth/session/status/{sessionId}` | Get oauth session status |

## SuperSearch Enrichment

- Docs: https://developer.instantly.ai/api-reference/groups/supersearch-enrichment
- Scope: An enrichment can take different forms, including standard data enrichment and AI-powered enrichment.
- Related schemas: [SuperSearch Enrichment](https://developer.instantly.ai/api-reference/schemas/supersearch-enrichment)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/supersearch-enrichment/enrich-leads-from-supersearch` | Enrich leads from supersearch |
| `GET` | `/api/v2/supersearch-enrichment/{resource_id}` | Get enrichment for resource |
| `POST` | `/api/v2/supersearch-enrichment` | Create an enrichment |
| `PATCH` | `/api/v2/supersearch-enrichment/{resource_id}/settings` | Update enrichment settings for resource |
| `POST` | `/api/v2/supersearch-enrichment/ai` | Create AI enrichment |
| `GET` | `/api/v2/supersearch-enrichment/ai/{resource_id}/in-progress` | Get AI enrichment for resource |
| `GET` | `/api/v2/supersearch-enrichment/history/{resource_id}` | Get enrichment history |
| `POST` | `/api/v2/supersearch-enrichment/run` | Run enrichment for resource |
| `POST` | `/api/v2/supersearch-enrichment/count-leads-from-supersearch` | Count leads from supersearch |
| `POST` | `/api/v2/supersearch-enrichment/preview-leads-from-supersearch` | Preview leads from supersearch |

## Webhook

- Docs: https://developer.instantly.ai/api-reference/groups/webhook
- Scope: A webhook subscription for receiving event notifications
- Related schemas: [Webhook](https://developer.instantly.ai/api-reference/schemas/webhook)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/webhooks` | List webhooks |
| `POST` | `/api/v2/webhooks` | Create webhook |
| `GET` | `/api/v2/webhooks/{id}` | Get webhook |
| `PATCH` | `/api/v2/webhooks/{id}` | Patch webhook |
| `DELETE` | `/api/v2/webhooks/{id}` | Delete webhook |
| `GET` | `/api/v2/webhooks/event-types` | List available event types |
| `POST` | `/api/v2/webhooks/{id}/test` | Test a webhook |
| `POST` | `/api/v2/webhooks/{id}/resume` | Resume a webhook |

## Webhook Event

- Docs: https://developer.instantly.ai/api-reference/groups/webhook-event
- Scope: A webhook event that was sent or attempted to be sent
- Related schemas: [Webhook Event](https://developer.instantly.ai/api-reference/schemas/webhook-event)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/webhook-events` | List webhook event |
| `GET` | `/api/v2/webhook-events/{id}` | Get webhook event |
| `GET` | `/api/v2/webhook-events/summary` | Get overview aggregates for webhook events |
| `GET` | `/api/v2/webhook-events/summary-by-date` | Get overview aggregates for webhook events by date |

## Workspace

- Docs: https://developer.instantly.ai/api-reference/groups/workspace
- Scope: A workspace entity representing a workspace
- Related schemas: [Workspace](https://developer.instantly.ai/api-reference/schemas/workspace)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/workspaces/current` | Get workspace |
| `PATCH` | `/api/v2/workspaces/current` | Patch workspace |
| `POST` | `/api/v2/workspaces/current/whitelabel-domain` | Set the agency domain for the workspace |
| `GET` | `/api/v2/workspaces/current/whitelabel-domain` | Get organization verified agency domain information |
| `DELETE` | `/api/v2/workspaces/current/whitelabel-domain` | Delete organization agency domain |
| `POST` | `/api/v2/workspaces/current/change-owner` | Change workspace owner |

## Workspace Billing

- Docs: https://developer.instantly.ai/api-reference/groups/workspace-billing
- Scope: Workspace Billing
- Related schemas: [Workspace Billing](https://developer.instantly.ai/api-reference/schemas/workspace-billing)

| Method | Path | Purpose |
| --- | --- | --- |
| `GET` | `/api/v2/workspace-billing/plan-details` | Get workspace plan details |
| `GET` | `/api/v2/workspace-billing/subscription-details` | Get workspace subscription details |

## Workspace Group Member

- Docs: https://developer.instantly.ai/api-reference/groups/workspace-group-member
- Scope: A member of a workspace group.
- Related schemas: [Workspace Group Member](https://developer.instantly.ai/api-reference/schemas/workspace-group-member)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/workspace-group-members` | Create workspace group member |
| `GET` | `/api/v2/workspace-group-members` | List workspace group member |
| `GET` | `/api/v2/workspace-group-members/{id}` | Get workspace group member |
| `DELETE` | `/api/v2/workspace-group-members/{id}` | Delete workspace group member |
| `GET` | `/api/v2/workspace-group-members/admin` | Get the current workspace admin workspace |

## Workspace Member

- Docs: https://developer.instantly.ai/api-reference/groups/workspace-member
- Scope: A member of a workspace with associated user details
- Related schemas: [Workspace Member](https://developer.instantly.ai/api-reference/schemas/workspace-member)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/api/v2/workspace-members` | Create workspace member |
| `GET` | `/api/v2/workspace-members` | List workspace member |
| `GET` | `/api/v2/workspace-members/{id}` | Get workspace member |
| `PATCH` | `/api/v2/workspace-members/{id}` | Patch workspace member |
| `DELETE` | `/api/v2/workspace-members/{id}` | Delete workspace member |

