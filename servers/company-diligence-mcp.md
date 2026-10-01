# Company Diligence MCP

Company diligence from official sources: SEC EDGAR, GLEIF LEI, EU VIES VAT, US state registries, UK Companies House, CourtListener, USAspending, SAM.gov and FEC, plus Trustpilot and news.

13 tools. Pay per call on Apify, billed to your own Apify account.
Current prices: https://apify.com/themineworks/company-diligence-mcp

## Connect

Easiest, with Apify sign in (OAuth), in any client that supports remote MCP
servers:

```
https://mcp.apify.com/?tools=themineworks/company-diligence-mcp
```

Direct, with your Apify API token as a Bearer token:

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

Transport is streamable HTTP. Get a token at
https://console.apify.com/account/integrations.

## Tools (13)

- `resolve_company`: Resolve a company name to verified identifiers and registry records (LEI, SEC EDGAR CIK, national registries).
- `get_state_registration`: Look up a company in official US state business registries: entity status, type, formation date, registered agent, principal address, and officers where the state publishes them.
- `get_sec_filings`: Fetch SEC filings for one known company, by ticker or CIK, newest first.
- `search_filings_fulltext`: Search the text inside SEC filings across all companies for a phrase, such as a product name, an executive or a risk factor.
- `verify_vat`: Validate an EU VAT number against the official VIES service.
- `get_lei_record`: Look up a company's Legal Entity Identifier (LEI) in GLEIF, the global registry, by legal name or exact LEI code.
- `get_court_records`: US court opinions and dockets from CourtListener, by party name, phrase, court, or date.
- `get_federal_awards`: US federal contracts, grants and loans awarded to a company, from USAspending.gov.
- `get_federal_contracts`: Search live US federal contract opportunities on SAM.gov by keyword, NAICS code, notice type or agency. Needs your own free SAM.gov API key.
- `get_campaign_finance`: Search US federal campaign finance via the official OpenFEC API: candidates by name, committees/PACs by name, or itemized Schedule A contributions for one committee.
- `get_uk_company_registration`: Look up UK companies on the official Companies House register: status, incorporation date, registered address, SIC codes and officers. Needs your own free Companies House API key.
- `get_reputation`: Company reputation snapshot: Trustpilot rating and recent reviews plus recent news coverage.
- `full_diligence_report`: One-call company dossier: identity resolution, LEI, US state registrations (officers & agents), SEC filings + full-text mentions, court records, federal awards, VAT (if given), and reputation.

## Listings

- Apify Store: https://apify.com/themineworks/company-diligence-mcp
- MCP Registry: `com.themineworks/company-diligence-mcp`
