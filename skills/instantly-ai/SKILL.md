---
name: instantly-ai
description: Use when building, reviewing, or debugging Instantly.ai integrations with the latest Instantly API v2, including campaigns, leads, accounts, emails, webhooks, analytics, OAuth, workspace management, and secure API key handling.
---

# Instantly AI

Use this skill for Instantly.ai API work. It is written against the currently published Instantly API v2 docs and should be preferred over v1 guidance.

## Security rules

- Use `INSTANTLY_API_KEY` from the environment. Do not hardcode it in code, tests, docs, curl history, commits, or screenshots.
- Prefer a dedicated API key per integration and grant only the scopes required for the endpoints you are using.
- Never echo the raw key back to the user. If you need to confirm configuration, confirm presence, not value.
- Do not commit `.env` files. This repo ignores them by default.
- Treat the key as write-capable workspace access. If a key leaks, rotate it instead of trying to reuse it.

## Workflow

1. Read [references/instantly-api-v2.md](./references/instantly-api-v2.md) for auth, rate limits, migration status, and safe usage rules.
2. Read [references/instantly-api-v2-endpoints.md](./references/instantly-api-v2-endpoints.md) for the full current resource and endpoint catalog.
3. When implementing a call, map the task to the correct resource group first, then the exact endpoint.
4. Check whether the operation is synchronous, paginated, or background-job based before writing client code.
5. Design for workspace-wide rate limits, because the limit is shared across API keys and across v1 and v2.

## Implementation defaults

- Base URL: `https://api.instantly.ai`
- Auth header: `authorization: Bearer ${INSTANTLY_API_KEY}`
- API version: `v2`
- Timeouts: set explicit HTTP timeouts in clients.
- Retries: retry only idempotent requests by default, and back off on `429` or `5xx`.
- Logging: redact `authorization`, API keys, and any secret-bearing headers.

## Quick examples

### cURL

```bash
curl --request GET \
  --url "https://api.instantly.ai/api/v2/campaigns" \
  --header "authorization: Bearer ${INSTANTLY_API_KEY}"
```

### TypeScript

```ts
const apiKey = process.env.INSTANTLY_API_KEY;

if (!apiKey) {
  throw new Error("INSTANTLY_API_KEY is required");
}

const response = await fetch("https://api.instantly.ai/api/v2/campaigns", {
  headers: {
    authorization: `Bearer ${apiKey}`,
  },
});
```

## When to be careful

- Bulk lead, campaign, account, and enrichment flows can generate large request volumes quickly.
- API key, webhook, workspace, billing, and ownership endpoints have higher blast radius and should use the narrowest possible scopes.
- Webhook consumers should verify origin assumptions, store delivery identifiers, and make handlers idempotent.

## Source of truth

The detailed reference files in this skill were generated from Instantly's official documentation and sitemap. If a new endpoint appears in the published docs, update the generated references before relying on memory.
