# The Mine Works MCP servers

Nine remote MCP servers with 80 tools in total, for AI agents that need
web data: India jobs, company diligence, recruiting, social listening,
e-commerce, US and India real estate, lead generation and academic research.
Each server runs on Apify as a Standby Actor and speaks streamable HTTP.

Pricing: pay per call on Apify, billed to your own Apify account. Current
prices for each tool are on the server's Apify Store page.

This repository holds the interface: tool lists, server manifests and client
configuration. The scrapers behind the tools run on Apify and are not
included here.

| Server | Tools | What it covers |
|---|---|---|
| [India Jobs MCP](servers/india-jobs-mcp.md) | 14 | India job market data: Naukri, Indeed India, Foundit, Shine, Apna, CutShort, Hirist, Instahyre and Internshala, plus LinkedIn candidate sourcing and AmbitionBox employer snapshots. |
| [Company Diligence MCP](servers/company-diligence-mcp.md) | 13 | Company diligence from official sources: SEC EDGAR, GLEIF LEI, EU VIES VAT, US state registries, UK Companies House, CourtListener, USAspending, SAM.gov and FEC, plus Trustpilot and news. |
| [Recruiting and Jobs MCP](servers/recruiting-jobs-mcp.md) | 10 | Job and candidate data for recruiting: ATS postings (Greenhouse, Lever, Workday, Ashby), LinkedIn, Indeed, SimplyHired, Naukri and CutShort, plus candidate sourcing and employer snapshots. |
| [Social Research MCP](servers/social-research-mcp.md) | 8 | Social listening: Reddit, X, Threads, LinkedIn posts, YouTube transcripts, Google News and Google Trends. |
| [E-commerce Intel MCP](servers/ecommerce-intel-mcp.md) | 8 | Product research: Amazon products and reviews, AliExpress prices, Shopify catalogs, TikTok Shop, Meta Ad Library and Google Trends. |
| [Real Estate MCP](servers/real-estate-mcp.md) | 8 | US property data: Zillow listings, sales, rentals and property details, plus Redfin, Realtor.com and Airbnb rental supply. |
| [Lead Generation MCP](servers/lead-generation-mcp.md) | 8 | B2B and local leads: people with work emails, email verification, website contacts, Google Maps, Yellow Pages and Trustpilot. |
| [Academic Research MCP](servers/academic-research-mcp.md) | 6 | Scholarly search: OpenAlex, Crossref, arXiv, OpenCitations and PubMed. |
| [India Real Estate MCP](servers/india-real-estate-mcp.md) | 5 | India property listings: 99acres, MagicBricks, NoBroker and Housing.com. Rent and sale, residential and commercial. |

## Connect

There are two ways in. Both reach the same tools.

**1. Through Apify's MCP gateway (easiest).** Add the URL below as a remote
MCP server in Claude, ChatGPT developer mode, Cursor, VS Code or Claude Code,
then sign in with your Apify account when the client asks. No token to copy.

```
https://mcp.apify.com/?tools=themineworks/india-jobs-mcp
```

Swap `india-jobs-mcp` for any server name in the table. The gateway prefixes
tool names with a short hash; clients read the names at connect time, so this
does not affect use.

**2. Direct to the server.** Point the client at the server's own endpoint
and send your Apify API token as a Bearer token.

```json
{
  "mcpServers": {
    "india-jobs-mcp": {
      "url": "https://themineworks--india-jobs-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

Get a token at https://console.apify.com/account/integrations.

## Registry

All nine servers are published on the official MCP Registry under the
`com.themineworks` namespace:

```
curl -s "https://registry.modelcontextprotocol.io/v0/servers?search=com.themineworks"
```

## Licence

MIT for the contents of this repository (manifests and documentation). The
Actors themselves are separately licensed and not included here.
