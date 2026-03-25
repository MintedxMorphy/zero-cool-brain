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

Repo: github.com/MintedxMorphy/ebay-card-dashboard
Live URL: https://ebay-card-dashboard.vercel.app
Stack: Next.js, Supabase, Vercel, eBay Fulfillment API
What it is: Pokémon + sports card trading dashboard for Gabriel (Gregory's son). Tracks eBay sales, P&L, buys/sells.
Last commit: 4c27b8b — Add Log a Sell form
Current status: WORKING. eBay OAuth live, real sales syncing, buy/sell forms working, correct amounts showing.

CRITICAL WARNINGS — DO NOT:

Drop or recreate the transactions table
Change user_id column type (already fixed to VARCHAR — was UUID, broke everything)
Add ebay_transaction_id back (removed intentionally)
Touch the eBay portal RuName config (took all day to get right)

Current schema:

transactions: id (UUID), user_id (VARCHAR), transaction_type, card_category, amount, card_name, ebay_order_id, transaction_date
users: user_id (VARCHAR = 'gabriel_ebay_account'), ebay_access_token, token_expires_at

Known issues / next priorities:

Dates all showing today instead of actual transaction date — needs fix
Missing 1 of 9 eBay sells — investigate
Buy/sell form price input UX needs decimal clarity
Gamification (XP, ranks, badges) — not yet built
AI card photo valuation — not yet built
Inventory manager — not yet built


2. SOUNDSTAGE AI

Repo: github.com/MintedxMorphy/soundstage-ai (Private)
Stack: TypeScript (check repo for full stack)
What it is: App for audiophiles and hi-fi enthusiasts. Gives bespoke equipment recommendations and room/space improvements for optimal listening experience.
Last known status: Built to Play Store version. DO NOT assume current state — read CONTEXT.md in repo before touching anything.

CRITICAL WARNINGS:

Always check git log before making any changes
Confirm what's working before touching anything
Gregory is concerned about session amnesia destroying recent work


3. CLAWWORK

Repo 1: github.com/MintedxMorphy/clawwork-agent-sdk (Public) — Agent SDK, autonomous job posting and bidding on Ethereum
Repo 2: github.com/MintedxMorphy/clawwork-board (Private) — Job board UI
Stack: JavaScript/TypeScript, Ethereum smart contracts
What it is: Agent-to-agent job marketplace with smart contracts. Takes a percentage cut of all jobs passing through the platform.
Last known status: Check CONTEXT.md in each repo before touching anything.


4. MISSION CONTROL

Repo: github.com/MintedxMorphy/mission-control (Private)
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
