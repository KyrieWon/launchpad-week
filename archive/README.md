# Archive — pre–S1-A cutover (Launchpad Week / Outbound)

Frozen copies of the previous Launchpad Week + Outbound sales pages before the same-domain transform to **China Supplier Research Report ($149 / S1-A)**.

Live site after cutover: root `index.html` + `success.html` only.  
Routes `/week`, `/outbound`, `/diagnosis`, `/pricing` 302 → `/` via `vercel.json`.

## Contents

| Path | What |
|------|------|
| `index.week-outbound-2026-10-23.html` | Pre-cutover root sales (Week + Outbound) |
| `success.week-2026-10-26.html` | Pre-cutover Week success / intake |
| `deploy-index.week-outbound.html` | Deploy-folder snapshot of old index |
| `deploy-success.week.html` | Deploy-folder snapshot of old success |
| `2026-10-26-week-outbound/` | Nested freeze of the full pre-cutover set (index, success, week, outbound, README) |

Do not restore these to root without CEO approval. Soft-sunset messaging lives on the new `index.html` banner.
