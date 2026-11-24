# Decisions log

Dated record of decisions made together. Newest at the bottom.

- 2026-11-18: Built AIOS from "AIOS Setup Guide for Claude Code" (Nate Herk's AIOS method). Plain folders + markdown so it moves between agent tools.
- 2026-11-18: Starter skills follow the current Claude Code skills docs (SKILL.md with name + description frontmatter, under 500 lines, details in reference files).
- 2026-11-18: Owner said the guide's 'starting facts' (Hasnat / BotBytesAI / OrderFlow) are not them. Removed them; owner name left as {OWNER} until onboarding.
- 2026-11-18: Owner is Isa, a Level 4 AI and Automation Practitioner apprentice. Onboarding adapted for an apprentice, not a business owner.
- 2026-11-18: Main apprenticeship project switched to Majestic Meat CRM (Route A); HACCP paused pending tutor meeting. Mentor = Admin. Context files written from Isa's pasted Project chat.
- 2026-11-18: AIOS pushed to private repo potohari/AIOS. Personal cloud environment 'AIOS' created for it. Stitch (Google UI design MCP) requested; key must go in env Network secrets (X-Goog-Api-Key), never chat. First pasted key was exposed in chat -> rotate.
- 2026-11-18: Stitch MCP added at user scope on Isa's request (key kept out of repo). Connected. Does not persist to new cloud sessions; key was again shared in chat, rotate when convenient.
- 2026-11-18: CRM working method agreed: split into sections; 25+ brainstorm questions per section (3 options + recommendation each), then build that section. Saved as crm-section skill. Section 1 = scope and approach (build vs buy first, as the brief requires a genuine comparison).
- 2026-11-22: AIOS runs cloud-first (claude.ai/code + GitHub). Isa said "yes always push": commit and push at the end of every piece of work.
- 2026-11-22: Exposed Stitch keys revoked by Isa. Stitch tested working in cloud session (list_projects OK).
- 2026-11-22: Tutor and employer informed about the CRM project.
- 2026-11-22: Isa said "always push" for the CRM screens branch too. First Stitch screen: Admin dashboard (Isa's choice).
- 2026-11-22: CRM v1 screen drafts made in Stitch (dashboard desktop r2, customer page, salesman quick-log, email approvals). Dashboard phone + quiet list generated but not retrievable via MCP. Review notes in projects/crm/designs/v1/REVIEW.md.
- 2026-11-24: CRM Section 1 (scope and approach) brainstorm done: 26 questions answered by Isa via interactive questions. Key: custom build on Supabase + Cloudflare, pilot Admin + 1-2 salesmen for 4 weeks, all trade customers, Claude API with pseudonymised data. Open: email automation in v1 vs online-shop phase.
- 2026-11-24: Email automation stays in v1, small, for trade customers with email + consent (prove it works, gain experience). Voice notes may be a main logging method because salesmen struggle with tech/English at times.
- 2026-11-24: Voice notes from salesmen are transcribed into logs by a human (Isa/Admin), not AI - poor English and Potohari would not be understood by AI. Section 2 (data foundations) started.
- 2026-11-24: CRM Section 2 (data foundations) brainstorm done: 25 questions. Key: 2-year SYSDEM CSV import + weekly upload page, CRM match table for messy codes, seasonal 'gone quiet' rule from history, minimum contact data + consent record, fake data for building.
