---
description: Search 2425+ MCP servers by keyword, domain, or name
argument-hint: <query> [--domain <name>]
disable-model-invocation: true
allowed-tools: [Read, Grep]
---

# /mcp-search

Search 2425+ MCP servers and get ready-to-use configs.

## Arguments

The user invoked this command with: $ARGUMENTS

## Instructions

1. Parse the user's search query from `$ARGUMENTS`
2. Open the reference file at `skills/mcp-lookup/references/mcp-servers-lookup.md`
3. Search using Grep for the query terms
4. If `--domain` is specified, filter to that domain section only
5. Present the results in a clean format:

### Output Format

For each match, show:
- Server name with GitHub link
- Install command
- Domain tags
- Description
- **Config JSON** (ready to copy into `mcpServers`)

### If No Results

- Suggest related domains from the catalog
- Offer to browse a specific domain
- Suggest alternative search terms

### If Too Many Results

- Show the top 10 most relevant matches
- Suggest narrowing with `--domain`
- Group results by domain

## Available Domains

AI, Analytics, Web, Search, Finance, Design, Security, Productivity, Files, Geo, Knowledge, Database, HR, Automation, DevOps, Ecommerce, Blockchain, Media, Communication, Cloud, Science, Testing, Translation, Government, Networking, Legal, Social, ERP, News, Audio, Gaming, Travel, Healthcare, IoT, Weather, Education, Caching, Utility, Messaging, Food, CRM, Fitness, CMS
