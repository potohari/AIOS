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
| Google Stitch | AI UI design for Majestic Meat CRM v1 screens | MCP, project `.mcp.json` (https://stitch.googleapis.com/mcp, HTTP, no key in file) | X-Goog-Api-Key header, injected by AIOS env Network secret (host stitch.googleapis.com). Key must NOT be in repo. | Blocked: env had NO network secret saved, so calls return "missing authentication". request_credential cannot save X-Goog-Api-Key headers. Fix: Isa adds it manually in env settings, then fresh session. | 2026-11-18 |

## Phrase mapping
What the owner means by common words (fill in per tool after wiring it): "message" = ?, "task" = ?, "comment" = ?

## Lessons
- 2026-11-18 Stitch: `get_environment` showed `network_secrets: []`, so the key was never saved (earlier session used ephemeral user-scope config). The secure credential form only supports `Authorization`-style headers and refuses `X-Goog-Api-Key`. Fix: add the secret by hand (environment menu > Edit > Network secrets: host `stitch.googleapis.com`, header `X-Goog-Api-Key`). Verify with `get_environment` (secret listed) before starting design work. MCP server config lives in project `.mcp.json` so it survives new containers.
