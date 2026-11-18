---
name: audit
description: Scores the AIOS out of 100 across the Four Cs (Context, Connections, Capabilities, Cadence), lists strengths and the top three gaps by leverage. Use when the owner says "audit", "score my AIOS", "how is my AIOS doing", or on the weekly Friday review.
---

## Goal
A scored audit with strengths, top three gaps and a next step, optionally saved to audits/YYYY-MM-DD.md.

## Steps
1. Scan the project: CLAUDE.md, context/, connections.md, references/, .claude/skills/, decisions/log.md, audits/ (previous scores), git log and remotes. Check .env key NAMES only (never print values).
2. Score each pillar 0-25 using reference.md. Show the evidence for each score in one line.
3. List 3-5 strengths.
4. List the top three gaps ranked by leverage (what unlocks the most next), each with the concrete fix.
5. Compare with the previous audit if one exists (delta per pillar).
6. Offer to save to audits/YYYY-MM-DD.md. Suggest running level-up next.

## Rules
- Be strict: placeholders and untested connections score zero.
- Never print secrets.
