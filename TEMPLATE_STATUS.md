# Template Status & Verification

**Classification:** Configurable n8n template asset — not a verified production deployment.

The repository proves a version-controlled workflow structure and documented intended use. It does not by itself prove a current configured run, production reliability, SLA, ROI, or client outcome.

## Verification gate
1. Parse/import into a clean current n8n instance.
2. Inspect all connections, expressions, routing branches, and Code nodes.
3. Replace every placeholder credential, mailbox, queue, webhook, model, label, URL, or resource ID.
4. Confirm current provider/model API requirements.
5. Run representative billing/support/sales/unknown ticket cases plus malformed-input and provider-failure cases.
6. Verify exactly one intended route/action is produced per ticket and record the test date/result.

## Security
Never commit API keys, OAuth secrets, mailbox credentials, private webhooks, customer PII, or production email content. Use synthetic tickets and fresh test credentials.

## Change record
- **2026-09-03:** Added repository verification/security/status control. No workflow-logic change or runtime pass is implied.
