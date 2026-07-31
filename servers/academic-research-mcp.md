# Academic Research MCP Server

Scholarly search for AI agents: OpenAlex works, Crossref metadata, arXiv preprints, OpenCitations graphs and PubMed, behind one MCP endpoint. No result, no charge.

**Endpoint**

```
https://themineworks--academic-research-mcp.apify.actor/mcp
```

Transport is streamable HTTP. Authenticate with your own Apify API token as a
Bearer token. You are billed on your own Apify account, per result delivered.

## Tools (6)

- `search_papers`: Search 250M+ scholarly works on OpenAlex: title, authors, venue, year, citation count, open-access status. Most-cited fi
- `crossref_metadata`: Crossref work metadata by search: DOIs, journals, publication dates, reference counts. The canonical record for a paper.
- `search_preprints`: Search arXiv preprints: title, authors, abstract, category, PDF link. Field-tag syntax supported (ti:, au:, abs:, cat:).
- `citation_graph`: Who cites a paper and what it cites, from OpenCitations, by DOI. The evidence trail around a claim.
- `search_pubmed`: Search PubMed biomedical literature: title, abstract, journal, MeSH terms. Field tags supported ([ti], [au], [ta], [mh])
- `literature_report`: One-call literature scan for a topic: published works (OpenAlex), canonical metadata (Crossref), preprints (arXiv), and 

## Pricing

| Event | Price (FREE tier) | Billing |
|---|---|---|
| `citation_graph` | $0.04 | per event |
| `crossref_metadata` | $0.05 | per event |
| `literature_report` | $0.13 | per call |
| `literature_report_section` | $0.03 | per event |
| `partial_literature_report` | $0.08 | per call |
| `search_papers` | $0.05 | per event |
| `search_preprints` | $0.04 | per event |
| `search_pubmed` | $0.04 | per event |

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
    "academic-research-mcp": {
      "url": "https://themineworks--academic-research-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

## Underlying Actors (5)

Each tool calls one of our published Apify Actors. They can also be used
directly if you only need one source.

- `themineworks/arxiv-preprint-search`
- `themineworks/crossref-scholarly-metadata`
- `themineworks/openalex-scholarly-works`
- `themineworks/opencitations-citation-graph`
- `themineworks/pubmed-ncbi-scraper`

## Store listing

https://apify.com/themineworks/academic-research-mcp
