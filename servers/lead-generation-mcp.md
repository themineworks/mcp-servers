# Lead Generation MCP Server

B2B and local lead generation for AI agents: people with verified emails, website contacts, Google Maps and Yellow Pages leads, and Trustpilot reputation. No result, no charge.

**Endpoint**

```
https://themineworks--lead-generation-mcp.apify.actor/mcp
```

Transport is streamable HTTP. Authenticate with your own Apify API token as a
Bearer token. You are billed on your own Apify account, per result delivered.

## Tools (8)

- `find_leads`: Find people and their work emails at a company: names, roles and directly-listed emails from the company site plus Linke
- `verify_emails`: Verify email addresses: syntax, DNS MX, live SMTP handshake, disposable-domain and role-mailbox detection. An "invalid" 
- `find_site_contacts`: Extract emails, phone numbers and social profiles straight from company websites (homepage plus /contact, /about, /team 
- `maps_leads`: Local business leads from Google Maps with MX-verified emails: name, address, phone, website, rating and a verified emai
- `search_places`: Raw Google Maps place search without email extraction: name, category, address, phone, rating, hours. The cheaper option
- `yellowpages_search`: US business listings from Yellow Pages by category and city: name, phone, address, website.
- `trustpilot_lookup`: Find businesses on Trustpilot by keyword or category: domain, TrustScore and review count. The reputation check before a
- `prospect_dossier`: One-call prospect pack for a company: people with emails, site contact channels, live verification of every email found,

## Pricing

| Event | Price (FREE tier) | Billing |
|---|---|---|
| `find_leads` | $0.06 | per event |
| `find_site_contacts` | $0.02 | per event |
| `maps_leads` | $0.04 | per event |
| `partial_prospect_dossier` | $0.06 | per call |
| `prospect_dossier` | $0.11 | per call |
| `prospect_dossier_section` | $0.02 | per event |
| `search_places` | $0.03 | per event |
| `trustpilot_lookup` | $0.04 | per event |
| `verify_emails` | $0.02 | per event |
| `yellowpages_search` | $0.04 | per event |

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
    "lead-generation-mcp": {
      "url": "https://themineworks--lead-generation-mcp.apify.actor/mcp",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

## Underlying Actors (7)

Each tool calls one of our published Apify Actors. They can also be used
directly if you only need one source.

- `themineworks/b2b-leads-finder`
- `themineworks/email-verifier-validator`
- `themineworks/google-maps-search-scraper`
- `themineworks/maps-leads`
- `themineworks/trustpilot-business-search`
- `themineworks/website-contact-finder`
- `themineworks/yellowpages-us`

## Store listing

https://apify.com/themineworks/lead-generation-mcp
