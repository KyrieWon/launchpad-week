# S1-A draft notes · 2026-10-26 Asia/Shanghai

## Files changed (this draft)
- `/workspace/launchpad-week-site/index.html` — home/sales A@$149
- `/workspace/launchpad-week-site/success.html` — post-pay intake for A only
- `/workspace/launchpad-week-site/week.html` — soft-sunset stub → /
- `/workspace/launchpad-week-site/outbound.html` — soft-sunset stub → /
- `/workspace/launchpad-week-sales.html` — synced = index
- `/workspace/launchpad-week-success.html` — synced = success
- `/workspace/launchpad-week-site/S1A-DRAFT-NOTES.md` — this file

## Routing
- `vercel.json` — `cleanUrls` plus 302 `/week`, `/outbound`, `/diagnosis`, `/pricing` → `/`. `week.html` and `outbound.html` stay in the repo for reference; the redirects take precedence.
- Archive `/workspace/launchpad-week-site/archive/2026-10-26-week-outbound/` — old Week/Outbound HTML copies kept; no live stubs stored there

## Checkout
- `WHOP_CHECKOUT_URL` on the sales page is the live $149 Whop plan
- `checkoutReady = true`; `isLiveUrl` still returns false if the URL includes `PLACEHOLDER`
- Primary Buy CTAs navigate to Whop. B and C still open the waitlist modal

## Constants (sales)
```js
const WHOP_CHECKOUT_URL = "https://whop.com/prismengine-xyz/4-10-chinese-suppliers-comparison-report/"; // live $149 plan
const CONTACT_EMAIL = "launchpadweek@mail.grokbot.com";
const KICKOFF_URL = "";
const checkoutReady = true; // still gate on !includes("PLACEHOLDER")
```

## Copy source
- Preferred paste: `/workspace/soft-connect/s1-a-sales-page-en-paste-1026.md` (used)
- Skeleton: `/workspace/s1-a-page-skeleton-intake-2026-10-26.md`
- IA: `/workspace/s1-a-ia-migration-2026-10-26.md`

## Bans checked
- [x] No Week $99 / Outbound $499 purchasable CTAs
- [x] No B/C price, Buy, Add to cart, or Checkout
- [x] Method honesty sentence present (verbatim from paste)
- [x] Soft-sunset banner present (Week & Outbound paused)
- [x] Footer: Only the $149 research report is for sale today
- [x] Success primary = A intake (required + optional + confirm)
- [x] No Kickoff/Cal, no Diagnosis
- [x] No Vercel deploy attempted (local draft only)
- [x] No GitHub repo created
- [x] Archive old copies preserved

## Deploy
**None.** Local rewrite only. No Vercel MCP calls. Domain stays `launchpad-week.vercel.app` for a later explicit ask.
