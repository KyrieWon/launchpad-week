# Deploy notes — S1-A cutover (same domain)

**Target:** Vercel project `launchpad-week` (`prj_fGrRWpqUE5jUFFk9hn3KhhoCrGWr`) → `https://launchpad-week.vercel.app`  
**Local source:** `/workspace/launchpad-week-site/` (no `.git` in this folder)  
**CEO path C:** NO new GitHub repo · transform in place · archive kept  

## Files ready to push
| File | Role |
|------|------|
| `index.html` | A $149 sales page + soft-sunset banner + Coming soon B/C waitlist |
| `success.html` | A intake only (Category* · market* · email* · Confirm* + optionals) |
| `vercel.json` | cleanUrls + 302 `/week` `/outbound` `/diagnosis` `/pricing` → `/` |
| `archive/` | Pre-cutover Week/Outbound HTML |

## Constants
```js
WHOP_CHECKOUT_URL = "https://whop.com/checkout/PLACEHOLDER-A149"
CONTACT_EMAIL = "launchpadweek@mail.grokbot.com"
checkoutReady = !String(WHOP_CHECKOUT_URL).includes("PLACEHOLDER")
```
Primary CTA = waitlist until PLACEHOLDER removed.

## Blockers (do not deploy from this agent until cleared)
1. **Whop checkout URL** still PLACEHOLDER (parent creates SKU).
2. **Vercel team auth:** `team_Ij1tk9ouK1mPt96g4wowYB1u` (scope `alidapacewiczakb80-9741`) — MCP returned 403; needs `authorize_team_access` by parent/user.
3. **No local git remote** for launchpad-week; connected GitHub account (`KyrieWon`) has no launchpad-week repo visible. Deploy via Vercel dashboard/CLI file upload or Cloud Agent with team auth.

## After auth + Whop URL
1. Replace PLACEHOLDER-A149 with live plan URL in `index.html`.
2. Deploy files to existing project `launchpad-week` (same domain). Do not create a new project.
