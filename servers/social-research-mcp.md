# Social Research MCP

Social listening: Reddit, X, Threads, LinkedIn posts, YouTube transcripts, Google News and Google Trends.

8 tools. Pay per call on Apify, billed to your own Apify account.
Current prices: https://apify.com/themineworks/social-research-mcp

## Connect

Easiest, with Apify sign in (OAuth), in any client that supports remote MCP
servers:

```
https://mcp.apify.com/?tools=themineworks/social-research-mcp
```

Direct, with your Apify API token as a Bearer token:

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

Transport is streamable HTTP. Get a token at
https://console.apify.com/account/integrations.

## Tools (8)

- `search_reddit`: Search Reddit posts by keyword or pull a subreddit feed, with scores, timestamps, and optional top comments.
- `search_x`: Pull an X (Twitter) account timeline by handle, with engagement metrics.
- `search_threads`: Search Meta Threads by keyword, by hashtag, or pull one profile's posts.
- `youtube_transcript`: Fetch the full spoken transcript of a YouTube video by URL or ID, optionally timestamped.
- `google_trends`: Google Trends interest for one or more keywords: interest over time, related queries and topics, and regional breakdown.
- `news_search`: Search Google News for recent coverage of a brand, topic or event, returning headline, source, publication date and link.
- `linkedin_posts`: Search public LinkedIn posts by keyword: post text, author, and engagement counts.
- `brand_pulse_report`: What the internet is saying about a brand or topic right now: Reddit, X, Threads, LinkedIn, news, and search interest in one call.

## Listings

- Apify Store: https://apify.com/themineworks/social-research-mcp
- MCP Registry: `com.themineworks/social-research-mcp`
