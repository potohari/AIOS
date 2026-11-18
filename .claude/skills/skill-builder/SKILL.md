---
name: skill-builder
description: Creates a new AIOS skill or improves an existing one using the six-step framework (name/trigger, goal, process, references, rules, improvement loop). Use when the owner says "build a skill", "make this a skill", "turn this into a skill", "fix/improve the X skill", or a skill misfires.
---

## Goal
A working skill folder in .claude/skills/<name>/ registered in CLAUDE.md, tested at least once, with the decision logged.

## Steps
1. Read reference.md (current Claude Code skill format) first.
2. Best build method: if the task has not been done together yet, do it once now in conversation, step by step. Turn that exact path into the skill.
3. Interview ONE question at a time, filling gaps only:
   1. Name and trigger: what is it called, what phrases should start it?
   2. Goal: the one-sentence output that exists at the end.
   3. Process: exact manual steps in order; what is looked at, what is decided.
   4. Reference files: voice, brand, priorities, templates, API notes needed.
   5. Rules: what could go wrong; the guard rails.
   6. Improvement loop: how will we judge a run good?
4. Create .claude/skills/<name>/SKILL.md (sections: Goal, Context, Steps, References, Rules), plus reference.md / scripts/ if needed. Use fixed scripts for parts that must be identical every time.
5. Register it in CLAUDE.md "Your skills" with trigger phrases. Log in decisions/log.md.
6. Run it once and review with the owner. Apply the fix table below; repeat.

## Fixing a skill
| Symptom | Fix |
|---|---|
| Wrong steps or order | Edit the steps |
| Misses tone/style/context | Add a reference file and point to it |
| Same mistake keeps happening | Add an explicit rule |
| Keeps searching / struggles with a tool | Save it in a reference doc; hard-code stable IDs |
| Good but not great | Run repeatedly, correct details each time |
| Does not trigger | Make the description more specific |
| Triggers too often | Narrow the description or set disable-model-invocation: true |
| Uses too much context searching | Hand the search to a sub-agent (context: fork) |

## Rules
- SKILL.md under 500 lines; details go in reference files.
- Side-effect skills (send, post, delete, deploy) get disable-model-invocation: true until trusted.
- Read every file of a third-party skill before installing; adapt to owner context.
