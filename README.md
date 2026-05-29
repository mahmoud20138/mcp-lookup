# awesome-mcp-lookup

[![npm version](https://img.shields.io/npm/v/awesome-mcp-lookup)](https://www.npmjs.com/package/awesome-mcp-lookup)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

OpenClaude plugin — search **2425+ MCP servers** across **39 domains** with ready-to-use configs.

## Install

### Option 1: Via Claude Code plugin system (recommended)

```
/plugin install awesome-mcp-lookup@mahmoud20138-plugins
```

If the marketplace isn't registered yet, add it first:

```
/plugin marketplace add github:mahmoud20138/claude-plugins
```

### Option 2: Via npm

```bash
npm install -g awesome-mcp-lookup
```

Then in Claude Code:

```
/plugin install awesome-mcp-lookup
```

### Option 3: Direct from GitHub

```
/plugin install github:mahmoud20138/mcp-lookup
```

## Usage

### Auto-invoked skill

Just ask Claude about MCP servers — the skill activates automatically:

> "What MCP servers exist for database work?"
> "Find me an MCP server for web scraping"
> "I need an MCP server for finance and trading"

### Slash command

Use `/mcp-search` for direct searches:

```
/mcp-search firecrawl
/mcp-search database postgres
/mcp-search finance
```

## What's Included

| Skill | Type | Description |
|-------|------|-------------|
| `mcp-lookup` | Model-invoked | Auto-activates when you ask about MCP servers |
| `mcp-search` | User-invoked | `/mcp-search <query>` for direct search |

## Domains (39)

AI, Analytics, Web, Search, Finance, Design, Security, Productivity, Files, Geo, Knowledge, Database, HR, Automation, DevOps, ECommerce, Blockchain, Media, Communication, Cloud, Science, Testing, Translation, Government, Networking, Legal, Social, ERP, News, Audio, Gaming, Travel, Healthcare, IoT, Weather, Education, Caching, Utility, Messaging, Food, CRM, Fitness, CMS

## Structure

```
awesome-mcp-lookup/
├── .claude-plugin/
│   └── plugin.json              # Plugin metadata
├── commands/
│   └── mcp-search.md            # /mcp-search slash command
├── skills/
│   └── mcp-lookup/
│       ├── SKILL.md             # Auto-invoked skill
│       └── references/
│           └── mcp-servers-lookup.md  # Server catalog (2425+)
├── package.json
├── README.md
└── LICENSE
```

## Data Source

Server data sourced from [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers).

## License

MIT
