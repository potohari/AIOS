# Claude Code skills: reference (checked 2026-11-18 from code.claude.com/docs/en/skills)

## Layout
.claude/skills/<name>/SKILL.md (required), reference.md / examples.md (loaded when referenced), scripts/ (executed, not loaded).
Project scope: .claude/skills/ (this repo). Personal: ~/.claude/skills/ (all projects on that machine; NOT read by cloud sessions).
Same-name precedence: enterprise > personal > project. Edits are live-reloaded; a new top-level skills dir needs /reload-skills.

## Frontmatter (must start on line 1, between --- markers; bad YAML = no fields; unknown fields ignored)
- name: command name (defaults to folder name)
- description (recommended): what + when; key use case first. description + when_to_use truncated at 1,536 chars.
- when_to_use: extra trigger phrases
- argument-hint, arguments: autocomplete hint / named args ($name, $ARGUMENTS, $0)
- disable-model-invocation: true = manual /name only (description not in context)
- user-invocable: false = hidden from / menu, Claude-only
- allowed-tools / disallowed-tools: pre-approve or remove tools for the invoking turn
- model, effort (low..max): overrides
- context: fork (+ agent, background): run as a sub-agent without conversation history
- hooks, paths (globs limiting auto-activation), shell (bash|powershell)
- Substitutions: ${CLAUDE_SKILL_DIR}, ${CLAUDE_PROJECT_DIR}, ${CLAUDE_SESSION_ID}
- Dynamic context: !`command` runs before Claude sees the skill; a failing command aborts invocation.

## Loading
1. Description always in context (~100 tokens). 2. Body on invocation; stays for the session. 3. Supporting files only when read.
After compaction: last invocation re-attached (first 5,000 tokens; 25,000 combined).

## Best practices
- Keep SKILL.md < 500 lines and concise (recurring token cost).
- Clear trigger descriptions; state what to do.
- Gate side-effect workflows with disable-model-invocation: true.
- Test in a fresh session; leftover context hides gaps.
- Audit unused skills with /skill-doctor.
