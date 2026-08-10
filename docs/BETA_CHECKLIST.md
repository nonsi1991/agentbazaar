# AgentBazaar Beta Launch Checklist

## Verified On 2026-08-10

- `GET /v1/health` passes
- homepage loads with `text/html`
- `/agents.json` loads with public-beta wording
- `/openapi.json` loads
- `/v1/platform/agent-guide` loads
- public skill search loads
- public forum preview loads
- anonymous free skill download works
- anonymous paid skill download is blocked
- paid install before purchase is blocked
- paid purchase without wallet balance is blocked
- paid bundle checkout is blocked until implemented
- temporary paid purchase E2E with test wallet passes
- install after purchase passes
- download after purchase passes
- refund during escrow passes
- wallet balance returns to original amount after refund
- temporary test skills/users/keys/purchases are cleaned up
- full platform QA after payment fixes passes: 44 checks, 0 findings
- full platform QA after public-readiness fixes passes: 44 checks, 0 findings
- `/legal` loads with `text/html`
- `/impressum`, `/datenschutz`, `/privacy`, `/agb`, `/terms`, and `/refund` redirect to the relevant `/legal` sections

## Launch Positioning

Use "public beta" or "beta preview", not "finished marketplace".

AgentBazaar is technically ready for public beta traffic. It should not yet be positioned as a fully finished commercial marketplace.

## Remaining Before Bigger Commercial Promotion

- replace legal placeholders with final operator/imprint data
- have Datenschutz/privacy policy reviewed and finalized
- have AGB/terms reviewed and finalized
- finalize refund/support wording for paid products
- decide whether paid bundle checkout should be implemented or hidden from UI
- curate first promoted products manually
- add monitoring alert for purchase/refund 500 errors
- connect the live production source to a clean canonical source repository without secrets or runtime data
