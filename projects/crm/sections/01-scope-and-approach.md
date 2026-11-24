# 01 Scope and approach
Status: decided (Isa to confirm summary) - 26 questions answered 2026-11-24

## Questions (batch 1)
1. #1 problem v1 must solve - A visibility record / B win back quiet customers / C email automation - ★A - Isa: A (visibility record)
2. Build or buy - A off-the-shelf / B custom on Supabase + Cloudflare / C hybrid - ★B (updated 22 Nov) - Isa: B custom on Supabase (still score HubSpot vs custom for the brief)
3. Users in v1 - A Admin + Isa / B Admin + Isa + 1-2 pilot salesmen / C all 4 salesmen - ★B - Isa: B
4. Customers in v1 - A ~50 active / B all ~300 trade / C trade + online - ★B - Isa: "all, let me have an option to label customers dead or remove them entirely"
5. How data gets in - A manual entry / B weekly SYSDEM export + quick-log / C live SYSDEM link - ★B - Isa: B

## Questions (batch 2) - answered via interactive questions 2026-11-24
6. Dead / remove customers - A archive ('dead', restorable) + Admin-only real delete with confirm (GDPR erasure) / B archive only / C anyone can delete - ★A - Isa: A
7. When to build - A prototype now, main build Month 5 / B wait until Month 5 / C build fully now - ★A - Isa: A
8. Running-cost budget - A free tiers first (Supabase + Cloudflare), upgrade only if needed / B small paid budget / C unknown, ask CEO - ★A - Isa: A

## Questions (batch 3) - 2026-11-24
9. Logins - A email + magic link / B email + password / C Google sign-in - ★A - Isa: "accounts named by users with their own passcodes" (named personal accounts, own passcode; no shared logins)
10. Salesmen see each other's customers - A own only (Admin/management see all) / B everyone sees all / C own + read-only others - ★A - Isa: A
11. Who sees prices offered - A Admin + management + that salesman (Sage data stays out) / B all users / C Admin only - ★A - Isa: A
12. How we know v1 worked - A baseline now + 3 measures (quiet customers won back, % calls logged, Admin chasing time) / B feedback only / C sales increase only - ★A - Isa: A

## Questions (batch 4) - 2026-11-24
13. Passcode type - A password + phone PIN / B password only / C PIN only - ★A - Isa: A
14. Salesmen devices - A own phones (web app, nothing stored, lock/log-out rule) / B company phones / C unsure - ★A - Isa: A
15. HubSpot vs custom comparison - A scored table + short HubSpot trial with fake data / B table only / C ask tutor - ★A - Isa: A
16. HACCP while CRM runs - A paused, decide with tutor / B finish as normal work / C drop - ★A - Isa: A

## Questions (batch 5) - 2026-11-24
17. AI provider - A Claude API (send pseudonymised purchase data only) / B OpenAI API / C no AI in v1 - ★A - Isa: A
18. Data retention - A 6 years then review; dead customers archived then deleted / B forever / C ask Admin/CEO - ★A - Isa: A
19. No signal when logging - A queue on phone, send when online, then clear / B must be online / C not a problem - ★A - Isa: A
20. Involving salesmen before build - A show drafts to 1-2 salesmen + short chat, record concerns / B tell at launch / C Admin briefs - ★A - Isa: A

## Questions (batch 6) - 2026-11-24
21. Pilot length - A 4 weeks / B 2 weeks / C 8 weeks - ★A - Isa: A
22. Support once live - A Isa, Admin as backup (weekly import + add users from a guide) / B Isa only / C outside developer later - ★A - Isa: A
23. Training - A 10-min demo + 1-page guide / B video / C learn as they go - ★A - Isa: "ill have to individually show them how to use and probably chase em up a bit with phonecalls etc" (1-to-1 demos + follow-up calls)
24. Online shop timing - A after trade v2 is stable / B straight after pilot / C not in this project - ★A - Isa: A

## Questions (batch 7) - 2026-11-24
25. Biggest risk - A salesmen don't log / B bad SYSDEM data / C time - ★A - Isa: "if they dont log theyre gonna get a call by me, if theyre too stupid to log i can make a little sheet for them to fill or ask them to send me a voice note on what theyve done so i fill for them" (= adoption risk; fallbacks: follow-up call, paper sheet, voice note to Isa)
26. Cut first if short of time - A email automation / B AI insights / C dashboard - ★A - Isa: B "ai insights since they can miss nuance if reasons arent properly entered, email automations are more essential for me since i believe they can boost online shop sales + maybe we can automate social media i.e build on marketing automations as a whole"

## Notes from discussion
- 2026-11-22: Isa works from many different PCs. Requirement: CRM must be cloud/web-based (any PC or phone, nothing installed). Dev work can also be cloud (Claude Code on the web + GitHub); VS Code at home PC is optional. Option B (custom on Supabase + Cloudflare, same as HACCP) now a strong candidate - still compare against off-the-shelf.

## Decisions (summary of Isa's answers - no new decisions)
- Goal v1: a written record of every customer's dealings (visibility).
- Approach: custom web app on Supabase + Cloudflare (cloud, any device). Still compare against HubSpot with a scored table + short trial using fake data.
- Users v1: Admin, Isa, 1-2 pilot salesmen. Pilot 4 weeks, then v2. Isa supports it, Admin is backup.
- Customers: all ~300 trade. Can mark "dead" (archived, restorable) or delete (Admin-only, confirm step, for GDPR erasure).
- Data in: weekly SYSDEM export + salesman quick-log. Sage stays out; prices offered are new data.
- Logins: named personal accounts, password + phone PIN. Salesmen use own phones (web app, offline queue, nothing kept on phone).
- Visibility: salesmen see own customers; Admin/management see all. Prices offered: Admin + management + that salesman.
- AI: Claude API, pseudonymised purchase data only. Retention: 6 years then review.
- Timing/budget: prototype now, main build Month 5; free tiers first.
- People: show drafts to 1-2 salesmen before building; train 1-to-1 + follow-up calls; fallbacks for non-loggers (paper sheet, voice note).
- Success: baseline now + 3 measures (quiet customers won back, % calls logged, Admin chasing time).
- Scope: online shop after trade v2. If short of time, cut AI insights first; email automation is a priority.
- HACCP: paused, decide with tutor.

## Open questions
- Q24 vs Q26 tension: email automation is the priority mainly for the ONLINE SHOP, but the online shop comes after trade v2. Trade customers are mostly phone/WhatsApp with few emails. Decide: (a) keep emails in v1 for trade customers with email + consent, or (b) move email automation to the online-shop phase.
- Voice-note fallback: Isa typing logs for salesmen = extra workload + accuracy risk; voice notes with customer details on WhatsApp need a GDPR handling rule.
- For assessed write-up: describe non-loggers as an adoption barrier (time, habit, trust), not ability. [ISA TO WRITE]
- Social media / wider marketing automation: future idea, not v1 (added to expansions.md).

## Build notes
