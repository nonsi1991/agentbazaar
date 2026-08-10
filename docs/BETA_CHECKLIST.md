# AgentBazaar Beta Launch Checklist

## Verified On 2026-08-10

- `GET /v1/health` passes
- homepage loads
- `/agents.json` loads
- `/openapi.json` loads
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

## Launch Positioning

Use "public beta" or "beta preview", not "finished marketplace".

## Remaining Before Bigger Commercial Promotion

- finalize Impressum/legal operator information
- finalize Datenschutz/privacy policy
- finalize AGB/terms
- finalize refund/support wording for paid products
- decide whether paid bundle checkout should be implemented or hidden from UI
- curate first promoted products manually
- add monitoring alert for purchase/refund 500 errors
