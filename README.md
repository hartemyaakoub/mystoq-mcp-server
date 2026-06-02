# @mystoq/mcp-server

> Model Context Protocol server for [Mystoq](https://mystoq.com) -
> let Claude (and other AI agents) read your store live.

[![MCP](https://img.shields.io/badge/MCP-2024--11--05-purple)](https://modelcontextprotocol.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## What is MCP?

The [Model Context Protocol](https://modelcontextprotocol.io) is an open
standard for connecting AI assistants to data sources. With this server,
your Mystoq store becomes a live "tool" that any MCP-aware agent
(Claude Desktop, Cursor, custom agents) can query.

## Use with Claude Desktop

Add to `~/Library/Application Support/Claude/claude_desktop_config.json`
(or the equivalent on your OS):

```json
{
  "mcpServers": {
    "mystoq": {
      "command": "npx",
      "args": ["-y", "@mystoq/mcp-server"],
      "env": {
        "MYSTOQ_API_KEY": "your_key",
        "MYSTOQ_TENANT": "your-store"
      }
    }
  }
}
```

Then ask Claude things like:
- "List my 10 most recent orders"
- "Which wilaya generates the most COD orders this week?"
- "Find products with low stock"

## Tools exposed

- `list_products(limit?)` - products in your store
- `list_orders(status?)` - orders (optionally filtered)
- `list_wilayas()` - 58 Algerian wilayas

## License

MIT.

Built by [Hartem Yaakoub](https://hartem.tkawen.com).

<!-- TKAWEN-ECOSYSTEM-FOOTER -->
## TKAWEN Ecosystem

This project is part of the [TKAWEN](https://tkawen.com) ecosystem — open APIs and tools for emerging-market digital infrastructure.

- [Mystoq](https://mystoq.com) — multi-tenant e-commerce platform for MENA
- [Algeria Certify](https://algeriacertify.com) — national digital credentialing
- [LIQAA](https://liqaa.io) — sovereign video conferencing
- [TKAWEN Academy](https://tkawen.com/academy) — online learning platform
- [SEO Toolkit](https://www.npmjs.com/package/@mystoq/seo-toolkit) — llms.txt, sitemap, Schema.org JSON-LD generators

Built by [Hartem Yaakoub](https://hartem.tkawen.com) - MIT licensed - Refreshed 2026-06-02.
