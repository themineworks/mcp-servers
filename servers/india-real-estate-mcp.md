# India Real Estate MCP

India property listings: 99acres, MagicBricks, NoBroker and Housing.com. Rent and sale, residential and commercial.

5 tools. Pay per call on Apify, billed to your own Apify account.
Current prices: https://apify.com/themineworks/india-real-estate-mcp

## Connect

Easiest, with Apify sign in (OAuth), in any client that supports remote MCP
servers:

```
https://mcp.apify.com/?tools=themineworks/india-real-estate-mcp
```

Direct, with your Apify API token as a Bearer token:

```json
{
  "mcpServers": {
    "india-real-estate-mcp": {
      "url": "https://themineworks--india-real-estate-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

Transport is streamable HTTP. Get a token at
https://console.apify.com/account/integrations.

## Tools (5)

- `search_properties_99acres`: 99acres property search with one filter covering rent, sale, PG/guest-house and commercial listings.
- `search_properties_magicbricks`: MagicBricks residential listings for rent or sale across Indian cities, filterable by BHK count and locality.
- `search_properties_nobroker`: NoBroker residential listings for rent or sale across 10 major Indian cities.
- `search_properties_housing`: Housing.com property search: residential rent/sale, or commercial rent/sale as its own listing types, across 32 major cities.
- `search_all_india_properties`: Search 99acres, MagicBricks, NoBroker, and Housing.com in one call.

## Listings

- Apify Store: https://apify.com/themineworks/india-real-estate-mcp
- MCP Registry: `com.themineworks/india-real-estate-mcp`
