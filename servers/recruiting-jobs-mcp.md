# Recruiting & Jobs MCP

Live job-market data for recruiting agents: ATS postings (Greenhouse/Lever/Workday/Ashby), LinkedIn jobs, Naukri, candidate sourcing, and employer snapshots. No result, no charge.

**Endpoint**

```
https://themineworks--recruiting-jobs-mcp.apify.actor/mcp
```

Transport is streamable HTTP. Authenticate with your own Apify API token as a
Bearer token. You are billed on your own Apify account, per result delivered.

## Tools (10)

- `search_jobs_ats`: Pull live job postings straight from company applicant-tracking systems (Greenhouse, Lever, Workday, Ashby). The posting
- `search_jobs_linkedin`: Search LinkedIn job postings by keyword and location. No cookies or login required.
- `search_jobs_india`: Search Naukri, India\'s largest job board, with salary, experience, work-mode and recency filters. Attacks a 1,624-user 
- `search_jobs_cutshort`: Search CutShort for Indian tech and startup roles. Returns skill tags, INR salary bands, experience ranges and remote fl
- `search_jobs_indeed`: Search Indeed, the widest job board available here, across eight country sites. Returns salary text as published, job ty
- `search_jobs_simplyhired`: Search SimplyHired US job postings: title, company, location, salary text as published, and posting age. A second sweep 
- `find_candidates`: Find people at a company by job title — a sourcing list with names, roles, and profile URLs. No cookies required.
- `enrich_profile`: Enrich a LinkedIn profile URL into structured data: name, headline, current role, experience, and skills.
- `company_snapshot`: Employer snapshot for recruiting: LinkedIn company profile (size, industry) plus AmbitionBox employee ratings and salary
- `hiring_signals_report`: Is this company hiring, and for what? Live ATS postings, LinkedIn postings, and an employer snapshot in one call. Billed

## Pricing

| Event | Price (FREE tier) | Billing |
|---|---|---|
| `company_snapshot` | $0.08 | per event |
| `enrich_profile` | $0.06 | per event |
| `find_candidates` | $0.1 | per event |
| `hiring_signal_section` | $0.03 | per event |
| `hiring_signals_report` | $0.12 | per call |
| `partial_hiring_signals` | $0.07 | per call |
| `search_jobs_ats` | $0.04 | per event |
| `search_jobs_cutshort` | $0.04 | per event |
| `search_jobs_indeed` | $0.05 | per event |
| `search_jobs_india` | $0.04 | per event |
| `search_jobs_linkedin` | $0.05 | per event |
| `search_jobs_simplyhired` | $0.05 | per event |

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
    "recruiting-jobs-mcp": {
      "url": "https://themineworks--recruiting-jobs-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

## Underlying Actors (10)

Each tool calls one of our published Apify Actors. They can also be used
directly if you only need one source.

- `themineworks/ambitionbox-companies`
- `themineworks/ats-jobs`
- `themineworks/cutshort-jobs-scraper`
- `themineworks/indeed-scraper`
- `themineworks/linkedin-company-details`
- `themineworks/linkedin-employees`
- `themineworks/linkedin-jobs-scraper`
- `themineworks/linkedin-profile-scraper`
- `themineworks/naukri-jobs`
- `themineworks/simplyhired-scraper`

## Store listing

https://apify.com/themineworks/recruiting-jobs-mcp
