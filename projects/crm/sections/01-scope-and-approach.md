# 01 Scope and approach
Status: brainstorming

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

## Notes from discussion
- 2026-11-22: Isa works from many different PCs. Requirement: CRM must be cloud/web-based (any PC or phone, nothing installed). Dev work can also be cloud (Claude Code on the web + GitHub); VS Code at home PC is optional. Option B (custom on Supabase + Cloudflare, same as HACCP) now a strong candidate - still compare against off-the-shelf.

## Decisions
## Open questions
## Build notes
