# India Jobs MCP

India job market data: Naukri, Indeed India, Foundit, Shine, Apna, CutShort, Hirist, Instahyre and Internshala, plus LinkedIn candidate sourcing and AmbitionBox employer snapshots.

14 tools. Pay per call on Apify, billed to your own Apify account.
Current prices: https://apify.com/themineworks/india-jobs-mcp

## Connect

Easiest, with Apify sign in (OAuth), in any client that supports remote MCP
servers:

```
https://mcp.apify.com/?tools=themineworks/india-jobs-mcp
```

Direct, with your Apify API token as a Bearer token:

```json
{
  "mcpServers": {
    "india-jobs-mcp": {
      "url": "https://themineworks--india-jobs-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

Transport is streamable HTTP. Get a token at
https://console.apify.com/account/integrations.

## Tools (14)

- `search_jobs_naukri`: Search Naukri, India's largest broad-market job board, with salary, experience, work-mode and recency filters.
- `search_jobs_indeed_india`: Search Indeed India (indeed.co.in) by keyword and location: title, company, job type, remote flag, and posting age.
- `search_jobs_foundit`: Search Foundit (formerly Monster India), a broad-market India job board, with experience, salary and recency filters.
- `search_jobs_shine`: Search Shine.com (Times Group), a broad-market India job board, with experience, salary and employment-type filters.
- `search_jobs_apna`: Browse Apna, India's largest blue-collar and early-career job app, by category, city and job-type.
- `search_jobs_cutshort`: Browse CutShort for Indian tech and startup roles by category: skill tags, INR salary bands, experience ranges and remote flags.
- `search_jobs_hirist`: Search Hirist, an India job board specific to technology roles, by keyword or category with experience-level and location filters.
- `search_jobs_instahyre`: Browse Instahyre, an India tech-recruiting platform, by job function, employment type and company size.
- `search_internshala`: Search Internshala for internships, regular jobs and fresher jobs in India.
- `search_all_india_jobs`: Search Naukri, Indeed India, Foundit, Shine, Hirist, and Internshala in one call.
- `find_candidates`: Find people at a company by job title.
- `enrich_profile`: Turn a LinkedIn profile URL into structured fields: name, headline, current role, past experience, education, and skills.
- `company_snapshot`: Employer snapshot for India recruiting: LinkedIn company profile (size, industry) plus AmbitionBox employee ratings and salary bands where available.
- `hiring_signals_india`: Live postings for one company across Naukri, Indeed India, Foundit, Shine, Hirist and Internshala, plus an employer snapshot, in one call.

## Listings

- Apify Store: https://apify.com/themineworks/india-jobs-mcp
- MCP Registry: `com.themineworks/india-jobs-mcp`
