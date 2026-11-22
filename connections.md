# Connections

Every tool the AIOS can reach. Route preference: direct API > official CLI > MCP > browser automation.

| Priority | Domain | Tool | Purpose | Route | Auth (.env key / method) | Status | Last tested |
|---|---|---|---|---|---|---|---|
| | Revenue | | | | | not mapped | |
| | Customer | | | | | not mapped | |
| | Calendar | | | | | not mapped | |
| | Comms | | | | | not mapped | |
| | Tasks | | | | | not mapped | |
| | Meetings | | | | | not mapped | |
| | Knowledge | | | | | not mapped | |

## Already available in Claude sessions (claude.ai connectors)
Gmail, Google Calendar and Google Drive connectors are attached to the owner's Claude account. Not yet tested or registered for AIOS use (Phase 3).

## Other tools
| Tool | Purpose | Route | Auth | Status | Last tested |
|---|---|---|---|---|---|
| Google Stitch | AI UI design: CRM screen mockups (projects/crm/stitch-design-prompt.md) | MCP, https://stitch.googleapis.com/mcp | X-Goog-Api-Key header via AIOS environment, never in repo/chat. Old keys pasted in chat were revoked 2026-11-22. | Connected: list_projects call succeeded (no projects yet) | 2026-11-22 |

## Phrase mapping
What the owner means by common words (fill in per tool after wiring it): "message" = ?, "task" = ?, "comment" = ?
