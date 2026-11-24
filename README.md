<img src="assets/logo.png" alt="Techny" width="72" height="72">

# Techny MCP server

[![Techny MCP connector](https://glama.ai/mcp/connectors/dev.techny/techny/badges/score.svg)](https://glama.ai/mcp/connectors/dev.techny/techny)

Open tech roles in **Egypt, Saudi Arabia and the UAE**, and remote roles open to people there, for your AI assistant.
[Techny](https://techny.dev) reads each company's own careers page every 3 hours and lists only tech roles:
engineering, data and AI, infrastructure and IT, security, product and design.

- **Server:** `https://techny.dev/mcp` (Streamable HTTP)
- **Sign-in:** none. Free.
- **Docs:** https://techny.dev/agents

This repository holds only the connection files for Cursor and Gemini CLI. The server itself runs at techny.dev.

## Tools

| Tool | What it does |
|---|---|
| `search_roles` | Search roles by words, country, city, level, job type, field, pay and how recent |
| `get_role` | One role's full description, places, level, pay and apply link |
| `company_roles` | One company's open roles and profile: sector, headquarters, stage and funding rounds with their sources |
| `create_alert` | A free Telegram alert for new roles matching a search; nothing is sent until the person presses Start |

`search_roles`, `get_role` and `company_roles` only read. In Claude, ChatGPT and other MCP Apps hosts, results show as
Techny's cards with an Apply button that opens the company's own job page.

## Connect

**Claude:** Settings → Connectors → Add custom connector → `https://techny.dev/mcp`

**ChatGPT** (web, any plan): Plugins → Add → Add custom MCP server. Name it Techny, paste `https://techny.dev/mcp`, choose No authentication, then Create and Connect.

**Cursor:** [Add to Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=techny&config=eyJ1cmwiOiJodHRwczovL3RlY2hueS5kZXYvbWNwIn0%3D), or in `~/.cursor/mcp.json`:

```json
{ "mcpServers": { "techny": { "url": "https://techny.dev/mcp" } } }
```

**Gemini CLI:**

```sh
gemini extensions install https://github.com/techny-dev/techny-mcp
```

**Claude Code:**

```sh
claude mcp add --transport http techny https://techny.dev/mcp
```

**VS Code:** in `.vscode/mcp.json`:

```json
{ "servers": { "techny": { "type": "http", "url": "https://techny.dev/mcp" } } }
```

## Try

- "Find me AI engineer jobs in Egypt"
- "Is Thndr hiring?"
- "Remote backend roles I can do from Cairo, mid-level, posted this week"
- "Tell me when new frontend roles in Dubai come in"

## Listed in

- [Official MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers?search=dev.techny) as `dev.techny/techny`
- [Glama](https://glama.ai/mcp/connectors/dev.techny/techny)

## Privacy and support

- Privacy: https://techny.dev/privacy
- Terms: https://techny.dev/terms
- Support: https://techny.dev/support
