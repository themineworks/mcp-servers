# The Mine Works MCP servers

Seven remote MCP servers that expose 53 web scrapers as tools
for AI agents. Hosted on Apify, streamable HTTP, billed per result delivered on
the caller's own Apify account.

This repository holds the interface: tool lists, server manifests, pricing and
client configuration. The scrapers themselves are closed source and run on
Apify.

| Server | Tools | Actors | Listing |
|---|---|---|---|
| [Company Diligence MCP](servers/company-diligence-mcp.md) | 10 | 10 | [Store](https://apify.com/themineworks/company-diligence-mcp) |
| [Social & Market Research MCP](servers/social-research-mcp.md) | 8 | 7 | [Store](https://apify.com/themineworks/social-research-mcp) |
| [Recruiting & Jobs MCP](servers/recruiting-jobs-mcp.md) | 10 | 10 | [Store](https://apify.com/themineworks/recruiting-jobs-mcp) |
| [Real Estate MCP](servers/real-estate-mcp.md) | 8 | 7 | [Store](https://apify.com/themineworks/real-estate-mcp) |
| [Lead Generation MCP Server](servers/lead-generation-mcp.md) | 8 | 7 | [Store](https://apify.com/themineworks/lead-generation-mcp) |
| [E-commerce Intelligence MCP Server](servers/ecommerce-intel-mcp.md) | 8 | 7 | [Store](https://apify.com/themineworks/ecommerce-intel-mcp) |
| [Academic Research MCP Server](servers/academic-research-mcp.md) | 6 | 5 | [Store](https://apify.com/themineworks/academic-research-mcp) |

## Connecting

Every server takes the same shape. Point your client at the endpoint and send
your Apify API token as a Bearer token.

```json
{
  "mcpServers": {
    "company-diligence": {
      "url": "https://themineworks--company-diligence-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

Get a token at https://console.apify.com/account/integrations. Works in Claude
Desktop, Claude Code, Cursor, Windsurf and any client supporting remote MCP
servers.

## Billing

Pay per event, on your own Apify account. Prices are listed per server. The
figure quoted is the FREE tier, which is the most anyone pays; Apify applies
tiered discounts automatically.

One rule holds across all seven: **a tool call that returns nothing is never
billed.** Empty searches, blocked fetches and failed lookups cost zero.

## Composite report tools

Each server carries a report tool that fans out across several of its own tools
in one call and returns a single structured document. Reports are priced below
the sum of their parts, and a report that finds nothing charges nothing.

Report tools run inside Apify Standby's five minute response ceiling, so their
internal budget is capped accordingly.

## Status

All seven servers are public and live on the Apify Store. Tool counts and
prices in this repository are generated from the deployed configuration.

## Licence

MIT for the contents of this repository (manifests, schemas, documentation).
The Actors themselves are separately licensed and not included here.
