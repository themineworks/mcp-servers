# E-commerce Intel MCP

Product research: Amazon products and reviews, AliExpress prices, Shopify catalogs, TikTok Shop, Meta Ad Library and Google Trends.

8 tools. Pay per call on Apify, billed to your own Apify account.
Current prices: https://apify.com/themineworks/ecommerce-intel-mcp

## Connect

Easiest, with Apify sign in (OAuth), in any client that supports remote MCP
servers:

```
https://mcp.apify.com/?tools=themineworks/ecommerce-intel-mcp
```

Direct, with your Apify API token as a Bearer token:

```json
{
  "mcpServers": {
    "ecommerce-intel-mcp": {
      "url": "https://themineworks--ecommerce-intel-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

Transport is streamable HTTP. Get a token at
https://console.apify.com/account/integrations.

## Tools (8)

- `search_amazon`: Search Amazon or look up specific ASINs: title, price, rating, review count, availability across 8 marketplaces (US, UK, DE, FR, JP, IN, CA, AU).
- `amazon_reviews`: Amazon customer reviews for specific ASINs: rating, title, text, verified-purchase flag.
- `search_aliexpress`: Search AliExpress by keyword: price in your ship-to currency, order counts, and seller rating.
- `shopify_store`: Full product catalog of any Shopify storefront: titles, prices, SKUs, variants.
- `tiktok_shop`: TikTok Shop products by keyword: price, units sold, and seller.
- `competitor_ads`: Live and past ads from the Meta Ad Library for a brand or keyword: creative text, media type, run dates, advertiser page.
- `search_interest`: Google Trends interest over time for a keyword.
- `product_intel_report`: One-call product picture for a brand or keyword: Amazon products, reviews of the top hit, AliExpress supplier prices, and search interest.

## Listings

- Apify Store: https://apify.com/themineworks/ecommerce-intel-mcp
- MCP Registry: `com.themineworks/ecommerce-intel-mcp`
