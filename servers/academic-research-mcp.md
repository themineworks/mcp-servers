# Academic Research MCP

Scholarly search: OpenAlex, Crossref, arXiv, OpenCitations and PubMed.

6 tools. Pay per call on Apify, billed to your own Apify account.
Current prices: https://apify.com/themineworks/academic-research-mcp

## Connect

Easiest, with Apify sign in (OAuth), in any client that supports remote MCP
servers:

```
https://mcp.apify.com/?tools=themineworks/academic-research-mcp
```

Direct, with your Apify API token as a Bearer token:

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

Transport is streamable HTTP. Get a token at
https://console.apify.com/account/integrations.

## Tools (6)

- `search_papers`: Search 250M+ scholarly works on OpenAlex: title, authors, venue, year, citation count, open-access status.
- `crossref_metadata`: Crossref work metadata by search: DOIs, journals, publication dates, reference counts.
- `search_preprints`: Search arXiv preprints: title, authors, abstract, category, PDF link.
- `citation_graph`: Citation graph around a paper, by DOI: which papers cite it, and which it cites, from OpenCitations.
- `search_pubmed`: Search PubMed biomedical literature: title, abstract, journal, MeSH terms.
- `literature_report`: One-call literature scan for a topic: published works (OpenAlex), canonical metadata (Crossref), preprints (arXiv), and biomedical hits (PubMed).

## Listings

- Apify Store: https://apify.com/themineworks/academic-research-mcp
- MCP Registry: `com.themineworks/academic-research-mcp`
