---
name: mcp-lookup
description: This skill should be used when the user asks about MCP servers, Model Context Protocol tools, wants to find or discover MCP servers, asks "what MCP servers exist for X", needs MCP server configs, or discusses integrating external tools with Claude Code. Provides a searchable catalog of 2425+ MCP servers across 39 domains.
version: 1.0.0
---

# MCP Server Lookup

Search and discover 2425+ MCP servers across 39 domains with ready-to-use configs.

## When This Skill Applies

Activate when the user:
- Asks about MCP servers for a specific task or domain
- Wants to find, discover, or browse MCP servers
- Needs an MCP server config to add to their setup
- Asks "what MCP servers exist for X" or "is there an MCP server for Y"
- Discusses integrating external tools, APIs, or services with Claude Code
- Mentions Model Context Protocol, MCP tools, or MCP integrations

## How to Search

The full server catalog is at: `skills/mcp-lookup/references/mcp-servers-lookup.md`

### Search Strategy

1. **By domain**: The catalog is organized into 39 domains. Check the domains table at the top of the file to find the relevant section:
   - AI, Analytics, Web, Search, Finance, Design, Security, Productivity, Files, Geo, Knowledge, Database, HR, Automation, DevOps, Ecommerce, Blockchain, Media, Communication, Cloud, Science, Testing, Translation, Government, Networking, Legal, Social, ERP, News, Audio, Gaming, Travel, Healthcare, IoT, Weather, Education, Caching, Utility, Messaging, Food, CRM, Fitness, CMS

2. **By keyword**: Use Grep to search the reference file for keywords matching the user's need (e.g., "github", "docker", "postgres", "slack", "stripe")

3. **By name**: If the user mentions a specific server name, grep for it directly

### Presenting Results

When you find matching servers:
1. Show the server name with its GitHub link
2. Show the install command
3. Show the domain tags
4. Show the description
5. **Always include the ready-to-use config JSON** — this is the key value of this plugin

### Config Format

Each server entry includes a config JSON block like:
```json
"server-name":{"type":"stdio","command":"npx","args":["-y","package-name"]}
```

To use it, tell the user to add it to their `~/.openclaude.json` under `mcpServers`, or to their project's `.mcp.json`.

## Tips

- If the user's query is vague, suggest 2-3 relevant domains and ask which interests them
- For broad queries, show the top 5-10 most relevant results, not all matches
- Always note the total count of matches found
- If a server appears dead (link broken), mention it but still show the config
