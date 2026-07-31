# E-commerce Intelligence MCP Server

Product intelligence for AI agents: Amazon products and reviews, AliExpress supplier prices, Shopify catalogs, TikTok Shop, Meta Ad Library competitor ads, and search interest. No result, no charge.

**Endpoint**

```
https://themineworks--ecommerce-intel-mcp.apify.actor/mcp
```

Transport is streamable HTTP. Authenticate with your own Apify API token as a
Bearer token. You are billed on your own Apify account, per result delivered.

## Tools (8)

- `search_amazon`: Search Amazon or look up specific ASINs: title, price, rating, review count, availability across 8 marketplaces (US, UK,
- `amazon_reviews`: Amazon customer reviews for specific ASINs: rating, title, text, verified-purchase flag. Sort by recent or helpful, filt
- `search_aliexpress`: Search AliExpress by keyword: price in your ship-to currency, orders, rating. The supplier-side price check.
- `shopify_store`: Full product catalog of any Shopify storefront: titles, prices, SKUs, variants. Works on any Shopify-hosted domain.
- `tiktok_shop`: TikTok Shop products by keyword: price, sales count, seller. The social-commerce side of a product check.
- `competitor_ads`: Live and past ads from the Meta Ad Library for a brand or keyword: creative text, media type, run dates, advertiser page
- `search_interest`: Google Trends interest over time for a keyword, matching the Social server\'s pricing for the same underlying data.
- `product_intel_report`: One-call product picture for a brand or keyword: Amazon products, reviews of the top hit, AliExpress supplier prices, an

## Pricing

| Event | Price (FREE tier) | Billing |
|---|---|---|
| `amazon_reviews` | $0.12 | per event |
| `competitor_ads` | $0.12 | per event |
| `partial_product_intel` | $0.14 | per call |
| `product_intel_report` | $0.23 | per call |
| `product_intel_section` | $0.02 | per event |
| `search_aliexpress` | $0.06 | per event |
| `search_amazon` | $0.02 | per event |
| `search_interest` | $0.12 | per event |
| `shopify_store` | $0.04 | per event |
| `tiktok_shop` | $0.12 | per event |

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
    "ecommerce-intel-mcp": {
      "url": "https://themineworks--ecommerce-intel-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

## Underlying Actors (7)

Each tool calls one of our published Apify Actors. They can also be used
directly if you only need one source.

- `themineworks/aliexpress-products`
- `themineworks/amazon-products`
- `themineworks/amazon-reviews`
- `themineworks/google-trends-pro`
- `themineworks/meta-ad-library-scraper`
- `themineworks/shopify-store-scraper`
- `themineworks/tiktok-shop-products`

## Store listing

https://apify.com/themineworks/ecommerce-intel-mcp
