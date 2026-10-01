# Real Estate MCP

US property data: Zillow listings, sales, rentals and property details, plus Redfin, Realtor.com and Airbnb rental supply.

8 tools. Pay per call on Apify, billed to your own Apify account.
Current prices: https://apify.com/themineworks/real-estate-mcp

## Connect

Easiest, with Apify sign in (OAuth), in any client that supports remote MCP
servers:

```
https://mcp.apify.com/?tools=themineworks/real-estate-mcp
```

Direct, with your Apify API token as a Bearer token:

```json
{
  "mcpServers": {
    "real-estate-mcp": {
      "url": "https://themineworks--real-estate-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

Transport is streamable HTTP. Get a token at
https://console.apify.com/account/integrations.

## Tools (8)

- `search_listings`: Search homes currently for sale on Zillow by city, ZIP or neighborhood.
- `recently_sold`: Homes already sold on Zillow, with sale price and date. The comparables tool.
- `rental_listings`: Long-term rentals on Zillow, with monthly rent and availability date.
- `property_details`: Detail on specific Zillow properties by listing URL or ZPID: Zestimate, price history, tax history, HOA, year built and assigned schools.
- `redfin_search`: Search Redfin for-sale or recently-sold listings by location.
- `realtor_search`: Search Realtor.com for-sale or sold listings by location.
- `str_market`: Short-term rental supply on Airbnb for a location: nightly prices, ratings, and availability.
- `market_report`: One-call market picture for a location: active listings, recent solds, rentals, and short-term rental supply.

## Listings

- Apify Store: https://apify.com/themineworks/real-estate-mcp
- MCP Registry: `com.themineworks/real-estate-mcp`
