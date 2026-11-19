# Wigoo

[Wigoo](https://getwigoo.com) is an AI travel companion, and this server brings it into your AI assistant.

**Today** it covers mobile data abroad: the catalog of travel eSIMs for more than 190 countries and regions, which mobile networks each plan uses, data sizes and validity, unlimited day passes and top ups, and the price in 55 currencies, with a link to buy.

**Coming next** to the same server: planning a trip and the other travel services Wigoo offers in its app. New tools appear here without changing how you connect.

This repository holds the MCP server's connection details, an agent skill and the plugin manifests. The server itself is hosted at `https://api.getwigoo.com/api/mcp`.

[Docs](https://docs.getwigoo.com/mcp) · [Claude](https://claude.ai/directory/connectors/wigoo) · [ChatGPT](https://chatgpt.com/plugins/plugin_asdk_app_6ae205880e5c8191b19b807c732b4e01) · Official MCP Registry: `com.getwigoo/wigoo`

## Connect

```bash
claude mcp add --transport http wigoo https://api.getwigoo.com/api/mcp
```

Any other MCP client: add `https://api.getwigoo.com/api/mcp` as a remote server over Streamable HTTP. No sign-in and no key. See the [quickstart](https://docs.getwigoo.com/mcp/quickstart).

To add only the skill:

```bash
npx skills add youssbim/wigoo-mcp
```

## Tools

All of them only read. None places an order.

| Tool | What it does |
| --- | --- |
| `search_destinations` | Countries and regions Wigoo sells eSIMs for, with the starting price and a link |
| `get_destination` | What a destination offers: networks, data sizes, validity, day passes, top ups |
| `list_plans` | The plans on sale for a destination, with data, validity, networks and price |
| `get_quote` | The price of one plan in the requested currency, and the link to buy it |

## What it sends

This package holds configuration only: no local code, no binaries, no credentials. Every tool call goes to `api.getwigoo.com` with the destination, plan and currency asked for. The server needs no account and asks for no personal data. See the [privacy policy](https://getwigoo.com/en/privacy). The tools are served by the remote server, so they can change without a new commit here.

## Buying

The catalog is free to use. The traveler buys on getwigoo.com through the link `get_quote` returns, with an email address and no account.

## License

MIT for what is in this repository. The Wigoo service itself is not open source.
