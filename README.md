# PromptWatch Cursor Plugin

AI visibility monitoring, citation tracking, and content gap analysis for brands in LLM responses.

## Installation

Install from the Cursor Marketplace, or add the MCP server directly:

```json
{
  "promptwatch": {
    "url": "https://server.promptwatch.com/mcp",
    "headers": {
      "Authorization": "Bearer YOUR_API_KEY"
    }
  }
}
```

## Configuration

Set your API key as an environment variable:

```bash
export PROMPTWATCH_API_KEY=your_api_key_here
```

Get your API key at [promptwatch.com](https://promptwatch.com).

## Components

### Skills

| Skill | Description |
|-------|-------------|
| `setup` | Onboard to PromptWatch — create projects, monitors, brands, prompts |
| `visibility-report` | Comprehensive AI visibility report across LLMs |
| `citation-analysis` | Analyze which sources LLMs cite for your brand |
| `content-gap-analysis` | Find content gaps and get recommendations |
| `competitor-analysis` | Compare brand vs competitors across AI responses |
| `traffic-analysis` | Analyze AI-referred traffic and crawler activity |

### Agent

| Agent | Description |
|-------|-------------|
| `seo-strategist` | AI visibility strategist — produces GEO strategies from PromptWatch data |

### Rules

| Rule | Description |
|------|-------------|
| `promptwatch-conventions` | API conventions: date formats, project resolution, bulk operations |

### MCP Server

Connects to the PromptWatch API with 65+ tools across: monitors, prompts, citations, brands, responses, visitors, crawlers, content gaps, tags, personas, projects, and models.

## Plugin Structure

```
plugins/promptwatch/
├── .cursor-plugin/
│   └── plugin.json
├── mcp.json
├── assets/
│   └── logo.svg
├── skills/
│   ├── setup/
│   ├── visibility-report/
│   ├── citation-analysis/
│   ├── content-gap-analysis/
│   ├── competitor-analysis/
│   └── traffic-analysis/
├── rules/
│   └── promptwatch-conventions.mdc
└── agents/
    └── seo-strategist.md
```

## Validation

```bash
node scripts/validate-template.mjs
```
