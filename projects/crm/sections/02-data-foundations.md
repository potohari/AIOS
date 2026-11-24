# 02 Data foundations
Status: decided (Isa to confirm summary) - 25 questions answered 2026-11-24

## Questions (batch 1) - 2026-11-24
1. How Claude sees the SYSDEM export - A pseudonymised sample (~50 rows via Isa's pseudonymiser) / B describe columns / C screenshot - ★A - Isa: A
2. Export format - A CSV/Excel / B PDF only / C unsure - ★A - Isa: "csv"
3. History in first import - A 12 months / B 2 years / C everything - ★A - Isa: B (2 years: better year-on-year seasonal comparison)
4. Matching customers week to week - A SYSDEM account code / B name / C phone - ★A - Isa: "sysdem names and codes are currently a mess but we can use and fix them i guess"

## Questions (batch 2) - 2026-11-24
5. Where to fix messy names/codes - A match table in the CRM (SYSDEM untouched; keep before/after copies) / B clean SYSDEM itself / C both - ★A - Isa: A
6. Who confirms duplicates - A CRM suggests, Isa + Admin confirm / B Isa alone / C auto-merge - ★A - Isa: B (Isa reviews every match)
7. 'Gone quiet' rule - A twice usual gap / B fixed 21 days / C usual gap + seasonal adjust (Christmas, Eid) - ★A - Isa: C
8. Baseline timing - A now, from 2-year export (+ Admin estimate of weekly chasing time) / B right before pilot / C after build - ★A - Isa: A

## Questions (batch 3) - 2026-11-24
9. Which seasons to expect - Christmas / Eid al-Adha / Ramadan-Eid al-Fitr / Summer (multi-select) - Isa: "every season has its own trends the data should tell u this already" -> learn seasonality from the 2-year history (compare each customer with the same period last year). Note: Eid/Ramadan move ~11 days earlier each year, so match by Islamic calendar, not calendar week.
10. Contact data stored - A minimum (business name, main contact, phone, email, delivery day, consent) / B minimum + free notes / C everything - ★A - Isa: A
11. Marketing consent record - A status + date + source / B yes/no / C assume trade is fine - ★A - Isa: A
12. Product names - A short clean list mapped from SYSDEM codes / B SYSDEM names as-is / C very detailed - ★A - Isa: A

## Questions (batch 4) - 2026-11-24
13. Weekly import - A upload page in CRM (preview before saving) / B Isa runs script / C email-in - ★A - Isa: A
14. Bad rows - A import good rows, report bad ones / B stop whole import / C import everything - ★A - Isa: A
15. Build/test data - A fake generated data (300 customers, 2 years of orders) / B pseudonymised real / C real - ★A - Isa: A
16. Backups (Supabase free has no daily backups) - A weekly export to a private store / B upgrade Supabase / C SYSDEM is the backup - ★A - Isa: "private store till need something else" (A, revisit later)

## Questions (batch 5) - 2026-11-24
17. Price offered record - A product + £/kg + date + who / B + quantity + delivery terms / C free text - ★A - Isa: "product, price offered, who to, simple options for them to read and put in answers" (date auto-filled; simple pick-lists for salesmen)
18. Lost/quiet reasons - A fixed list + Other / B fixed only / C free text - ★A - Isa: A
19. Salesman-customer assignment - A Admin assigns in CRM / B from SYSDEM / C salesmen claim - ★A - Isa: A
20. AI data access - A customer ID + purchase data only / B + business names / C everything - ★A - Isa: A

## Questions (batch 6) - 2026-11-24
21. Suggest 'dead' - A suggest after 6 months, Admin confirms / B after 12 months / C never, by hand - ★A - Isa: "by hand, they can come back alive maybe but yeah by hand" (C; dead is reversible)
22. Raw CSV files after import - A keep last 4 weeks then delete / B keep all / C delete straight away - ★A - Isa: A
23. Who can upload imports - A Admin + Isa / B Isa only / C any manager - ★A - Isa: A
24. Measuring Admin chasing time - A Admin logs one normal week / B estimate / C skip - ★A - Isa: A

## Questions (batch 7) - 2026-11-24
25. Pseudonymised SYSDEM sample (~50 rows) - A this week / B next week / C need Admin's OK - ★A - Isa: A

## Decisions (summary of Isa's answers - no new decisions)
- Source: SYSDEM CSV export; first import = last 2 years; weekly imports after that via an Import page (Admin + Isa only), with preview; good rows go in, bad rows listed for fixing. Raw CSVs kept 4 weeks then deleted.
- Messy SYSDEM names/codes: fixed in a CRM match table (SYSDEM untouched, before/after copies kept). Isa reviews every duplicate match.
- Customer record: minimum data only - business name, main contact, phone, email, delivery day, marketing consent (status + date + source). Salesman assigned by Admin in the CRM.
- Products: short clean list, each SYSDEM product code mapped to one.
- Prices offered: product, price, which customer, by whom (date automatic), with simple pick-lists for salesmen.
- Reasons (lost deal / gone quiet): fixed list + Other.
- 'Gone quiet': each customer's usual gap, adjusted for seasonal patterns learned from the 2-year history (Eid/Ramadan matched by Islamic calendar).
- 'Dead': marked by hand only, reversible.
- AI sees customer ID + purchase data only.
- Build with fake generated data; real data only after security is done. Backups: weekly export to a private store for now.
- Baseline now from the 2-year export + Admin logs one normal week of chasing time.

## Open questions
- Isa to send pseudonymised ~50-row SYSDEM sample this week (to-do).
- Where the private backup store lives (e.g. company Google Drive) and who can access it.

## Build notes
