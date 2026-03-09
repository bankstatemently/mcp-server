# Bankstatemently MCP Server

**Parse bank statement PDFs into structured financial data — directly from AI agents and coding assistants.**

→ **Full documentation:** [bankstatemently.com/developers/mcp](https://bankstatemently.com/developers/mcp)
→ **API reference:** [bankstatemently.com/developers/api](https://bankstatemently.com/developers/api)
→ **Get an API key:** [bankstatemently.com/developers](https://bankstatemently.com/developers)

---

## Overview

The Bankstatemently MCP server implements the [Model Context Protocol](https://modelcontextprotocol.io) over stateless HTTP. It lets AI agents — Claude, Cursor, Copilot, and others — parse bank statement PDFs and work with the resulting transaction data without leaving the agent session.

**Server URL:** `https://api.bankstatemently.com/mcp`

**Authentication:** API key via `Authorization: Bearer <key>` or `X-API-Key` header.

**Supports 500+ banks** across the US, UK, Singapore, Australia, Hong Kong, Malaysia, and more.

---

## Tools

| Tool | Description |
|------|-------------|
| `parse_statement` | Upload a PDF (as base64 or URL) and parse it into structured transactions, balances, and account metadata |
| `get_statement` | Retrieve parsed data for a previously uploaded document |
| `list_statements` | Browse previously parsed statements |
| `get_credits` | Check your remaining credit balance |

---

## Quick Start

### Claude Desktop (`claude_desktop_config.json`)

```json
{
  "mcpServers": {
    "bankstatemently": {
      "type": "http",
      "url": "https://api.bankstatemently.com/mcp",
      "headers": {
        "X-API-Key": "your_api_key"
      }
    }
  }
}
```

### Cursor (`.cursor/mcp.json`)

```json
{
  "mcpServers": {
    "bankstatemently": {
      "type": "http",
      "url": "https://api.bankstatemently.com/mcp",
      "headers": {
        "X-API-Key": "your_api_key"
      }
    }
  }
}
```

---

## Example Usage

Once connected, you can ask your AI agent:

> *"Parse this bank statement PDF and give me a summary of all transactions over $500."*

> *"Convert the attached Chase statement to a CSV and categorise each transaction."*

> *"How much did I spend on subscriptions last month? Here's my bank statement."*

---

## Pricing

1 credit = 1 PDF page. Credits are available as one-time packs or monthly subscriptions.

→ [View pricing](https://bankstatemently.com/pricing)

---

## Links

- Website: [bankstatemently.com](https://bankstatemently.com)
- MCP docs: [bankstatemently.com/developers/mcp](https://bankstatemently.com/developers/mcp)
- API docs: [bankstatemently.com/developers/api](https://bankstatemently.com/developers/api)
- REST API spec: [github.com/Bankstatemently/api](https://github.com/Bankstatemently/api)
- Support: [help@bankstatemently.com](mailto:help@bankstatemently.com)
