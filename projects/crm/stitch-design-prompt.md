# Prompt: CRM screen designs with Stitch (paste into a new AIOS session)

```
Read CLAUDE.md, context/priorities.md and connections.md first.

TASK: Help me design version 1 screens for the Majestic Meat CRM (my Level 4 apprenticeship project) using the Stitch MCP server.

STEP 0 - Check Stitch works
- Confirm the Stitch tools are loaded. If they are not: the key is saved as a network secret on my AIOS environment (host stitch.googleapis.com, header X-Goog-Api-Key). Add Stitch as a project MCP server in .mcp.json (https://stitch.googleapis.com/mcp, HTTP) with NO real key in any file, tell me to start a fresh session, and stop.
- Never print, log or commit any key. If a call fails, write the cause and fix into connections.md.

STEP 1 - My design decisions come first (ask me one question at a time)
Before designing, ask me:
1. Which screen do I want first?
2. Who uses it (Admin, salesman, me) and on what device (desktop / phone)?
3. What 3-5 things must that person see or do on it?
4. Any colours, logo or style to match Majestic Meat?
Use my answers as the brief. Do not decide the content for me.

SCREENS (v1 candidates - I pick the order)
a) Customer page (Admin, desktop): status badge (active / gone quiet, X days), last order + usual order gap, spend this quarter vs last, top product, last price offered, timeline of calls / WhatsApp / orders (SYSDEM) / lost deals with reason, AI insight with drafted follow-up, contact with hidden phone and marketing-consent status.
b) Admin dashboard (desktop): quiet customers this week, lost deals and reasons, follow-ups overdue, emails waiting for approval. Avoid ranking or scoring individual salesmen.
c) Salesman quick-log (phone): log a call or WhatsApp in 3 taps: customer, outcome, price offered, optional note.
d) Email approval queue (Admin): AI draft, why it was suggested, consent status, Approve / Edit / Reject. Nothing sends without approval.
e) Quiet customers list (Admin): filter by days quiet, salesman, product.
(Online shop customers are a later phase - do not design them yet.)

RULES (from my project risks - must show in every design)
- Made-up data only: no real customer names, phone numbers or prices.
- Hide phone numbers by default; show marketing consent / soft opt-in status before any email action.
- AI suggestions use purchase history only - never name, area or anything that could link to religion or ethnicity.
- Human approval before any email is sent.
- Salesman activity must show business context (stock, price, season) so data is not read as judging the salesman.

FOR EACH SCREEN
1. Generate it in Stitch from my brief. Show me the result (screenshot).
2. Ask what I would change; iterate until I am happy (max 3 rounds).
3. Save the final export and a screenshot to projects/crm/designs/v1/<screen-name>/ (keep earlier rounds in a rounds/ subfolder - they are evidence of iteration).
4. Add a row to projects/crm/designs/design-log.md: date | screen | what changed and why. Leave the "why" for ME to write in my own words - put [ISA TO WRITE] there. Do not write assessed wording for me.

AT THE END
- Short summary: screens done, what is next (show v1 to Admin and one salesman, record feedback, then v2).
- Log the session in decisions/log.md. Commit. Ask me before pushing.
```
