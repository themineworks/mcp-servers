# Recruiting and Jobs MCP

Job and candidate data for recruiting: ATS postings (Greenhouse, Lever, Workday, Ashby), LinkedIn, Indeed, SimplyHired, Naukri and CutShort, plus candidate sourcing and employer snapshots.

10 tools. Pay per call on Apify, billed to your own Apify account.
Current prices: https://apify.com/themineworks/recruiting-jobs-mcp

## Connect

Easiest, with Apify sign in (OAuth), in any client that supports remote MCP
servers:

```
https://mcp.apify.com/?tools=themineworks/recruiting-jobs-mcp
```

Direct, with your Apify API token as a Bearer token:

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

Transport is streamable HTTP. Get a token at
https://console.apify.com/account/integrations.

## Tools (10)

- `search_jobs_ats`: Pull live job postings straight from company applicant-tracking systems (Greenhouse, Lever, Workday, Ashby).
- `search_jobs_linkedin`: Search LinkedIn job postings by keyword and location: title, company, location, and posting date.
- `search_jobs_indeed`: Search Indeed job postings across eight country sites: salary text as published, job type, remote flag and posting age.
- `search_jobs_simplyhired`: Search SimplyHired US job postings: title, company, location, salary text as published, and posting age.
- `search_jobs_india`: Search Naukri, India's largest job board, with salary, experience, work-mode and recency filters.
- `search_jobs_cutshort`: Search CutShort for Indian tech and startup roles.
- `find_candidates`: Find people at a company by job title.
- `enrich_profile`: Turn a LinkedIn profile URL into structured fields: name, headline, current role, past experience, education, and skills.
- `company_snapshot`: Employer snapshot for recruiting: LinkedIn company profile (size, industry) plus AmbitionBox employee ratings and salary bands where available.
- `hiring_signals_report`: Live ATS postings, LinkedIn postings and an employer snapshot for one company, in one call.

## Listings

- Apify Store: https://apify.com/themineworks/recruiting-jobs-mcp
- MCP Registry: `com.themineworks/recruiting-jobs-mcp`
