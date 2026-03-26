ZERO COOL — MASTER CONTEXT FILE
Owner: MintedxMorphy (Gregory)
Last Updated: [UPDATE THIS AT END OF EVERY SESSION]
Rule: READ THIS ENTIRE FILE before touching any code in any session.

WHO I'M WORKING WITH

Name: Gregory
GitHub: MintedxMorphy
Primary devices: Mac Studio, MacBook, iPad, Samsung Galaxy Flip
Communicates via: Telegram, Terminal/Open Claw, Discord
Style: Keep it simple. Mobile-first. No enterprise bloat. Fun where possible.
Critical rule: NEVER drop or recreate database tables without explicit confirmation.


ACTIVE PROJECTS
1. CARDTRACK

1. CARDTRACK

Repo: github.com/MintedxMorphy/ebay-card-dashboard
Local: ~/Projects/ebay-card-dashboard
Live URL: https://ebay-card-dashboard.vercel.app
Stack: Next.js, Supabase, Vercel, eBay Fulfillment API, eBay Browse API
What it is: Pokémon + sports card trading dashboard for Gabriel (Gregory's son). Tracks eBay sales, P&L, buys/sells.
Last commit: 57a3bd1 — Fix Supabase initialization in delete route (Mar 26, 2026)
Current status: ✅ PRODUCTION READY. All 9 eBay sales syncing, dates correct, P&L accurate, charts working, full transaction management. Vercel build passing.

CRITICAL WARNINGS — DO NOT:

Drop or recreate the transactions table
Change user_id column type (already fixed to VARCHAR — was UUID, broke everything)
Add ebay_transaction_id back (removed intentionally)
Touch the eBay portal RuName config (took all day to get right)

Current schema:

transactions: id (UUID), user_id (VARCHAR), transaction_type, card_category, amount, card_name, ebay_order_id, transaction_date
users: user_id (VARCHAR = 'gabriel_ebay_account'), ebay_access_token, token_expires_at

Status (as of March 26, 2026):

✅ FIXED: Transaction dates showing correctly (actual eBay order dates)
✅ FIXED: All 9 eBay sales syncing correctly (no missing transactions)
✅ CONFIRMED: Price input works with manual decimal entry — no UX change needed
✅ NEW: Transaction numbering (#1, #2, etc.) — sequential display
✅ NEW: Sorted by transaction_date (purchase/sale date) not insertion date — realistic timeline
✅ NEW: All Transactions view — removed 10-transaction limit, shows entire history
✅ NEW: Delete transaction function — click to edit, confirm to delete permanently
✅ NEW: Color palette (lib/colors.ts) — Cyan, Purple, Orange for charts (Green/Magenta UI unchanged)
✅ FIXED: Supabase initialization in delete route — Vercel build passing

Next priorities (features, not bugs):

Gamification (XP, ranks, badges) — not yet built
AI card photo valuation — Claude Vision API for condition/value assessment
Inventory manager — track cards in collection, organize by set/sport
Wishlist + price alerts — watch cards, alert when prices drop
Weekly recap screen — profit summary, best performers, trends


2. SOUNDSTAGE AI

Repo: github.com/MintedxMorphy/soundstage-ai (Private)
Local: ~/Projects/soundstage-ai
Stack: Expo (React Native, TypeScript, Expo Router), Supabase, Claude API, OpenAI API (fallback)
What it is: App for audiophiles and hi-fi enthusiasts. Gives bespoke equipment recommendations and room/space improvements for optimal listening experience.
Last commit: d295a6f — Revert to original SoundStageLOGO with proper padding (Mar 26, 2026)
Current status: ✅ PLAY STORE READY. Icons finalized, EAS builds passing, production APK ready for submission.

BUILDS & ARTIFACTS:

Production Build (AAB for Play Store):
- Build ID: 7a153cf7-60d1-40ed-ae50-c71d688452bf
- AAB: https://expo.dev/artifacts/eas/g5noJ3noPRiMrsZt6H18hT.aab
- Status: ✅ Ready for Google Play Store submission

Preview Build (APK for device testing):
- Build ID: 7e73a19f-d56d-44d1-964c-9cf25abf6635
- Install: https://expo.dev/accounts/gmgremil/projects/soundstage-ai/builds/7e73a19f-d56d-44d1-964c-9cf25abf6635
- Status: ✅ Ready to test on Samsung Galaxy Flip

App Icons (Updated Mar 26):
- icon.png: 1024x1024 (main app icon)
- icon-512.png: 512x512 (Google Play Store requirement)
- adaptive-icon.png: 1024x1024 (Android adaptive icon)
- favicon.png: 192x192 (web favicon)
- splash.png: 1280x2340 (portrait splash screen)
- All icons: Original SoundStageLOGO with full "Ai sound Stage" text, no distortion

EAS Configuration:
- Project ID: 40bf1753-6b5e-4a0e-8f69-147a7889978b
- eas.json: Configured for production store distribution
- iOS bundle ID: com.gmgremil.soundstageai
- Android package: com.gmgremil.soundstageai

CRITICAL WARNINGS:

Do NOT delete EAS Project ID from app.config.ts
Do NOT change iOS/Android bundle identifiers without legal/certificate updates
Do NOT modify the app.config.ts entry unless updating EAS credentials

Status (as of March 26, 2026):

✅ COMPLETED: Logo processing and icon generation
✅ COMPLETED: EAS build configuration for production
✅ COMPLETED: Production AAB build (ready for Play Store)
✅ COMPLETED: Preview APK build (ready for device testing)
✅ READY: Play Store submission (icons, AAB, credentials all set)

Next Steps:

Upload AAB to Google Play Console (internal testing track)
Complete store listing (screenshots, description, privacy policy)
Submit for review
(After approval) Release to production

Next Priorities (Features):

Speaker Placement Calculator — Floor plan + optimal positioning (3-4 days)
System Synergy Analysis — Impedance/power/character matching (2-3 days)
Upgrade Recommendation Engine — Weakest link identification (3-4 days)
Budget Optimization Tools — Allocation percentages + genre-specific (2-3 days)


3. CLAWWORK

Repo 1: github.com/MintedxMorphy/clawwork-agent-sdk (Public) — Agent SDK, autonomous job posting and bidding on Ethereum
Local 1: ~/Projects/clawwork-agent-sdk
Repo 2: github.com/MintedxMorphy/clawwork-board (Private) — Job board UI
Local 2: ~/Projects/clawwork-board
Stack: JavaScript/TypeScript, Ethereum smart contracts
What it is: Agent-to-agent job marketplace with smart contracts. Takes a percentage cut of all jobs passing through the platform.
Last known status: Check CONTEXT.md in each repo before touching anything.


4. MISSION CONTROL

Repo: github.com/MintedxMorphy/mission-control (Private)
Local: ~/Projects/mission-control
Status: Still a work in progress. Low priority. Do not touch unless explicitly asked by Gregory.


SESSION PROTOCOL — FOLLOW THIS EVERY TIME
START OF SESSION:

Read this file completely
Ask Gregory: "Which project are we working on today?"
Read that project's CONTEXT.md in its repo
Run: git log --oneline -5 to see recent commits
Check git status — confirm nothing is uncommitted
Tell Gregory: "I'm up to speed. Here's what I know: [summary]. What do you want to work on?"
DO NOT touch any code until you've confirmed current state

END OF SESSION:

Run git status — commit everything
Push to GitHub
Update the project's CONTEXT.md with:

What was built today
Current working state
Next priorities
Any critical warnings


Update the Last Updated date in this file
Tell Gregory: "All pushed. Last commit: [hash]. Here's what's ready for next session: [summary]"


GLOBAL RULES — ALWAYS APPLY

Always work from ~/Projects/ on Mac Studio. Never use /tmp/ or other temporary directories — /tmp/ is wiped on restart and causes data loss.
Never drop databases or tables without explicit typed confirmation from Gregory
Always push to GitHub at end of session
Always confirm current state before making changes
Mobile-first on all UI work
Keep it simple — no enterprise complexity
When in doubt, ask Gregory before acting
If something was working and now isn't, check git log before writing new code
Never paste credentials or secrets into chat


HOW TO USE THIS FILE

Always fetch PROJECTS.md from the GitHub URL above. Never read a local copy of PROJECTS.md — it may be outdated

Gregory will start sessions with:

"Read PROJECTS.md and tell me what you know."

Fetch it from:

https://raw.githubusercontent.com/MintedxMorphy/zero-cool-brain/main/PROJECTS.md

Confirm you've read it, summarize the active project status, then ask what to work on.
