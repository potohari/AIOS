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
| Google Stitch | AI UI design: CRM v1 screen mockups | MCP via Stitch connector on Isa's Claude account (mcp__stitch__*) | Connector auth. Env has no Stitch network secret. Old keys pasted in chat revoked 2026-11-22. Never put a key in repo/chat. | Connected: list_projects OK, no auth error | 2026-11-22 |

## Phrase mapping
What the owner means by common words (fill in per tool after wiring it): "message" = ?, "task" = ?, "comment" = ?

## Lessons
- 2026-11-18 Stitch: `get_environment` showed `network_secrets: []`, so the key was never saved (earlier session used ephemeral user-scope config). The secure credential form only supports `Authorization`-style headers and refuses `X-Goog-Api-Key`. Fix: add the secret by hand (environment menu > Edit > Network secrets: host `stitch.googleapis.com`, header `X-Goog-Api-Key`). Verify with `get_environment` (secret listed) before starting design work. MCP server config lives in project `.mcp.json` so it survives new containers.
- 2026-11-22 Stitch auth: the X-Goog-Api-Key header cannot be saved via the secure key form, and the AIOS environment has no network secret for it. A raw call without a key returns "missing required authentication credential"; a project .mcp.json entry without a key makes Claude Code try OAuth ("does not support dynamic client registration"). What works: the Stitch connector attached to Isa's Claude account (tools load as mcp__stitch__*; list_projects returns OK with no auth error). Do NOT add a second keyless stitch entry in .mcp.json - it clashes with the working connector. If the connector stops working, add the key by hand in environment Network secrets (host stitch.googleapis.com, header X-Goog-Api-Key) and use a placeholder header in .mcp.json; never the real key.
