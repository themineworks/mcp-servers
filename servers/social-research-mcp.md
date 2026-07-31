# Social & Market Research MCP

What the internet is saying: Reddit, X, Threads, LinkedIn, YouTube transcripts, Google News and Trends behind one MCP endpoint. No result, no charge.

**Endpoint**

```
https://themineworks--social-research-mcp.apify.actor/mcp
```

Transport is streamable HTTP. Authenticate with your own Apify API token as a
Bearer token. You are billed on your own Apify account, per result delivered.

## Tools (8)

- `search_reddit`: Search Reddit posts by keyword or pull a subreddit feed, with scores, timestamps, and optional top comments. What people
- `search_x`: Search X (Twitter) posts by keyword or pull a specific account timeline, with engagement metrics.
- `search_threads`: Search Threads posts by keyword or hashtag, or pull a profile feed.
- `youtube_transcript`: Fetch the transcript of a YouTube video, the full spoken text, optionally with timestamps. No API key needed.
- `google_trends`: Google Trends interest for one or more keywords: interest over time, related queries and topics, and regional breakdown.
- `news_search`: Search Google News for recent coverage of a brand, topic, or event, with source and publication date.
- `linkedin_posts`: Search public LinkedIn posts by keyword, what professionals and companies are posting about a topic.
- `brand_pulse_report`: What the internet is saying about a brand or topic right now: Reddit, X, Threads, LinkedIn, news, and search interest in

## Pricing

| Event | Price (FREE tier) | Billing |
|---|---|---|
| `brand_pulse_report` | $0.25 | per call |
| `google_trends` | $0.15 | per event |
| `linkedin_posts` | $0.05 | per event |
| `news_search` | $0.05 | per event |
| `partial_brand_pulse` | $0.1 | per call |
| `pulse_source` | $0.025 | per event |
| `search_reddit` | $0.04 | per event |
| `search_threads` | $0.05 | per event |
| `search_x` | $0.025 | per event |
| `youtube_transcript` | $0.02 | per event |

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
    "social-research-mcp": {
      "url": "https://themineworks--social-research-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

## Underlying Actors (7)

Each tool calls one of our published Apify Actors. They can also be used
directly if you only need one source.

- `themineworks/google-news`
- `themineworks/google-trends-pro`
- `themineworks/linkedin-post-search`
- `themineworks/reddit-scraper`
- `themineworks/threads-scraper`
- `themineworks/twitter-x-scraper`
- `themineworks/youtube-transcript-scraper`

## Store listing

https://apify.com/themineworks/social-research-mcp
