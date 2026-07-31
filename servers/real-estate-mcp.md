# Real Estate MCP

The Zillow API that doesn't exist. Listings, solds, rentals, comps, Redfin, Realtor.com and Airbnb supply behind one MCP endpoint. No result, no charge.

**Endpoint**

```
https://themineworks--real-estate-mcp.apify.actor/mcp
```

Transport is streamable HTTP. Authenticate with your own Apify API token as a
Bearer token. You are billed on your own Apify account, per result delivered.

## Tools (8)

- `search_listings`: Search homes for sale on Zillow by location, with price, bedroom, and property-type filters.
- `recently_sold`: Recently sold homes on Zillow, the comparables an agent or investor actually needs to price a property.
- `rental_listings`: Rental listings on Zillow by location, with rent range and bedroom filters.
- `property_details`: Full detail for specific Zillow listings: Zestimate, price history, tax history, and assigned schools.
- `redfin_search`: Search Redfin for-sale or recently-sold listings by location, a second opinion on Zillow data.
- `realtor_search`: Search Realtor.com listings by location, for sale or sold.
- `str_market`: Short-term rental supply on Airbnb for a location: nightly prices, ratings, and availability, the STR side of an invest
- `market_report`: One-call market picture for a location: active listings, recent solds, rentals, and short-term rental supply. Billed by 

## Pricing

| Event | Price (FREE tier) | Billing |
|---|---|---|
| `market_report` | $0.16 | per call |
| `market_report_section` | $0.04 | per event |
| `partial_market_report` | $0.1 | per call |
| `property_details` | $0.08 | per event |
| `realtor_search` | $0.06 | per event |
| `recently_sold` | $0.05 | per event |
| `redfin_search` | $0.06 | per event |
| `rental_listings` | $0.05 | per event |
| `search_listings` | $0.05 | per event |
| `str_market` | $0.08 | per event |

Prices shown are the FREE tier, which is the maximum anyone pays. Apify applies
tiered discounts (BRONZE, SILVER, GOLD and above) automatically based on your
plan. Your tier is shown on your Apify billing page.

**No result, no charge.** A tool call that returns nothing fires no billable
event.

## Client configuration

Claude Desktop, Cursor, Windsurf and any MCP client that supports remote
servers:

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

## Underlying Actors (7)

Each tool calls one of our published Apify Actors. They can also be used
directly if you only need one source.

- `themineworks/airbnb-scraper`
- `themineworks/realtor-scraper`
- `themineworks/redfin-scraper`
- `themineworks/zillow-property-details`
- `themineworks/zillow-recently-sold`
- `themineworks/zillow-rental-listings`
- `themineworks/zillow-search-scraper`

## Store listing

https://apify.com/themineworks/real-estate-mcp
