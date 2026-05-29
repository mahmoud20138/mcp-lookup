---
name: mcp-lookup
description: Use ONLY when the user explicitly asks to find, search, discover, or browse MCP servers, or asks "what MCP servers exist for X". Do NOT activate for general MCP questions, MCP config help, or casual mentions of MCP.
version: 1.0.1
---

# MCP Server Lookup

Search 2425+ MCP servers across 39 domains. Returns ready-to-use configs.

## Activation Rules

**ONLY activate when the user explicitly wants to FIND or SEARCH for MCP servers.** Examples:
- "find MCP servers for databases"
- "what MCP servers exist for web scraping"
- "search MCP servers for finance"
- "browse available MCP servers"

**Do NOT activate for:**
- General questions about MCP protocol
- Help configuring an already-known MCP server
- Casual mentions of "MCP" without a search intent
- Questions about how MCP works

## How to Search (LAZY LOAD — never read the full file)

The catalog is at: `skills/mcp-lookup/references/mcp-servers-lookup.md` (1.1MB — NEVER read the full file)

**Always use Grep to search.** Never use Read on the full file.

1. **By keyword**: `Grep pattern="<keyword>" path="skills/mcp-lookup/references/mcp-servers-lookup.md"`
2. **By domain**: `Grep pattern="### <Domain>" path="skills/mcp-lookup/references/mcp-servers-lookup.md"` to find the section header, then grep for specific terms within that domain
3. **By name**: `Grep pattern="<owner/repo>" path="skills/mcp-lookup/references/mcp-servers-lookup.md"`

### Presenting Results

For each match, show:
- Server name with GitHub link
- Install command
- Domain tags
- Description
- **Config JSON** (ready to copy into `mcpServers`)

### Config Format

```json
"server-name":{"type":"stdio","command":"npx","args":["-y","package-name"]}
```

## Performance Rules

- **NEVER read the full reference file** — it's 1.1MB and will waste context
- **Always use Grep** to search for specific terms
- **Limit output**: Show max 5-10 results for broad queries
- **Suggest domains** if the query is vague — don't grep blindly
