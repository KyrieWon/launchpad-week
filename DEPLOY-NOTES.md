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
WHOP_CHECKOUT_URL = "https://whop.com/prismengine-xyz/4-10-chinese-suppliers-comparison-report/"
CONTACT_EMAIL = "launchpadweek@mail.grokbot.com"
checkoutReady = true // isLiveUrl still rejects a URL that includes "PLACEHOLDER"
```
Primary Buy CTAs link to the live $149 Whop plan. B and C stay on the waitlist.

## Blockers (do not deploy from this agent until cleared)
1. **Whop checkout URL** is set in `index.html` to the live $149 plan.
2. **Vercel team auth:** `team_Ij1tk9ouK1mPt96g4wowYB1u` (scope `alidapacewiczakb80-9741`) — MCP returned 403; needs `authorize_team_access` by parent/user.
3. **No local git remote** for launchpad-week; connected GitHub account (`KyrieWon`) has no launchpad-week repo visible. Deploy via Vercel dashboard/CLI file upload or Cloud Agent with team auth.

## After auth
1. Live plan URL is already in `index.html`. Do not swap it back to a stand-in string.
2. Deploy files to existing project `launchpad-week` (same domain). Do not create a new project. This change does not deploy.
