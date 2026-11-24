# 02 Data foundations
Status: brainstorming (started 2026-11-24)

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

## Decisions
## Open questions
## Build notes
