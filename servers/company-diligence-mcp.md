# Company Diligence MCP

Official-registry company diligence for AI agents: SEC EDGAR, GLEIF LEI, EU VAT, court records, federal awards, reputation. No result, no charge.

**Endpoint**

```
https://themineworks--company-diligence-mcp.apify.actor/mcp
```

Transport is streamable HTTP. Authenticate with your own Apify API token as a
Bearer token. You are billed on your own Apify account, per result delivered.

## Tools (10)

- `resolve_company`: Resolve a company name to verified identifiers and registry records (LEI, SEC EDGAR CIK, national registries). Grounds a
- `get_sec_filings`: Fetch SEC EDGAR filings (10-K, 10-Q, 8-K, …) for a company by ticker or CIK, newest first.
- `search_filings_fulltext`: Full-text keyword search across SEC EDGAR filings (what the EDGAR UI calls EFTS).
- `verify_vat`: Validate an EU VAT number against the official VIES service. A well-formed "invalid" verdict is a result; only service f
- `get_lei_record`: Look up Legal Entity Identifier (LEI) records from GLEIF by company name or exact LEI code.
- `get_state_registration`: Look up a company in official US state business registries: entity status, type, formation date, registered agent, princ
- `get_court_records`: US federal and state court opinions and dockets from CourtListener, filtered by query, court, and date.
- `get_federal_awards`: US federal contracts, grants, and awards for a recipient company from USAspending.gov.
- `get_reputation`: Company reputation snapshot: Trustpilot rating and recent reviews plus recent news coverage. Trustpilot requires the com
- `full_diligence_report`: One-call company dossier: identity resolution, LEI, US state registrations (officers & agents), SEC filings + full-text 

## Pricing

| Event | Price (FREE tier) | Billing |
|---|---|---|
| `full_diligence_report` | $0.5 | per call |
| `get_court_records` | $0.12 | per event |
| `get_federal_awards` | $0.1 | per event |
| `get_lei_record` | $0.05 | per event |
| `get_reputation` | $0.12 | per event |
| `get_sec_filings` | $0.08 | per event |
| `resolve_company` | $0.1 | per event |
| `search_filings_fulltext` | $0.1 | per event |
| `verify_vat` | $0.05 | per event |

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
    "company-diligence-mcp": {
      "url": "https://themineworks--company-diligence-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

## Underlying Actors (10)

Each tool calls one of our published Apify Actors. They can also be used
directly if you only need one source.

- `themineworks/company-identity-resolver`
- `themineworks/courtlistener-court-records`
- `themineworks/eu-vat-vies-validator`
- `themineworks/gleif-lei-lookup`
- `themineworks/google-news`
- `themineworks/sec-edgar-filings`
- `themineworks/sec-edgar-fulltext-search`
- `themineworks/trustpilot-reviews`
- `themineworks/us-state-business-registry`
- `themineworks/usaspending-federal-awards`

## Store listing

https://apify.com/themineworks/company-diligence-mcp
