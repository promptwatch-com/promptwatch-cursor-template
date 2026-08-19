# Promptwatch for Cursor

Track your brand's visibility, citations, and sentiment across ChatGPT, Claude, Gemini, Perplexity, and AI Overviews, directly from Cursor.

This plugin connects Cursor to the [Promptwatch](https://promptwatch.com) MCP server. A Promptwatch account and API key are required.

## Install

### Cursor Marketplace

1. Open **Customize → Plugins**, search for **Promptwatch**, and click **Install**.
2. When prompted, paste your API key. Create one under **Settings → API Keys** in the [Promptwatch dashboard](https://app.promptwatch.com).

You can set or change the key later under **Plugins → Configure**.

### One-click install

Click the button below. Cursor opens an install dialog. Replace `YOUR_API_KEY` with your key, then click **Install**:

[![Install MCP Server](https://cursor.com/deeplink/mcp-install-dark.svg)](cursor://anysphere.cursor-deeplink/mcp/install?name=promptwatch&config=eyJ1cmwiOiJodHRwczovL3NlcnZlci5wcm9tcHR3YXRjaC5jb20vbWNwIiwiaGVhZGVycyI6eyJBdXRob3JpemF0aW9uIjoiQmVhcmVyIFlPVVJfQVBJX0tFWSJ9fQ==)

### Manual configuration

Add to `~/.cursor/mcp.json` (global) or `.cursor/mcp.json` (project):

```json
{
  "mcpServers": {
    "promptwatch": {
      "url": "https://server.promptwatch.com/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

## What you can ask

- "How visible is my brand in AI search results?"
- "Which sources are LLMs citing when they mention us?"
- "Compare our AI visibility against competitors."
- "What content gaps should I address?"
- "How much traffic are we getting from AI tools?"

Full tool reference and setup for other clients (Claude, ChatGPT): [promptwatch.com/docs/mcp](https://promptwatch.com/docs/mcp/setup)

## Links

- Website: [promptwatch.com](https://promptwatch.com)
- Documentation: [promptwatch.com/docs](https://promptwatch.com/docs/mcp/setup)
- Contact: [team@promptwatch.com](mailto:team@promptwatch.com)
