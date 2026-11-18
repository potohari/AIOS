---
name: onboard
description: Guided onboarding interview that writes the AIOS day-one context files. Use for first-time setup, or when the owner says "re-interview me", "update my context" or "onboard me again".
---

## Goal
context/about-me.md, about-business.md, priorities.md, voice.md and connections.md reflect the owner's real answers, and CLAUDE.md's behaviour section has his working-style preferences.

## Context
- Ask ONE question at a time. Encourage long answers (voice dictation is fine).
- Where a draft exists (starting facts below or existing context files), show it and ask him to confirm or correct instead of typing from zero.
- Save each raw answer to intake.md immediately, under a dated heading `## YYYY-MM-DD Q<n>`, word for word. Never wait until the end.
- Re-interview: read existing context files first; ask only what changed; move replaced versions to archives/context-YYYY-MM-DD/.

Starting facts: none. The facts in the setup guide were about someone else (owner said so on 2026-11-18). Do not reuse them; ask from zero.

## Steps
1. Who are you, what do you sell, and who do you sell it to? -> about-me.md, about-business.md
2. Paste one or two things you wrote recently, unedited. Say what each is (client message, team message, post). -> voice.md
3. What are your two or three biggest priorities for the next 90 days? -> priorities.md
4. Which tools do you use for revenue, customers, calendar, communication, tasks, meetings and knowledge? -> connections.md
5. What are your biggest pains or time drains right now? -> about-me.md
6. Who is on your team, and who do you depend on most? -> about-business.md
7. How do you like to work with an assistant: tone, detail level, things to never do? -> CLAUDE.md, voice.md
8. Generate the files:
   - about-business.md: offer, ideal customer, services, revenue model, team.
   - about-me.md: role, background, top pains.
   - priorities.md: 2-3 priorities, each with why it matters and a measurable outcome; if goals live in a tool, point there.
   - voice.md: samples verbatim + 5-10 style notes (sentence length, formality, phrases used, phrases avoided).
   - connections.md: fill the domain table (tool, purpose, status "not connected"), ranked by how much he uses it.
   - CLAUDE.md: add working-style preferences under "How to behave".
9. Log "onboarding completed" in decisions/log.md.
10. Close by telling him: what he can do today (ask "what should I focus on this week?"), what comes next (connect his most-used tool), and that the first /audit is due in about a week.

## Rules
- Specific beats generic: no placeholder text left in context files.
- Never invent facts. Mark unknowns as "unknown - ask".
- Keep each context file short; it is loaded often.
