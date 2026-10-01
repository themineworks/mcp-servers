# Lead Generation MCP

B2B and local leads: people with work emails, email verification, website contacts, Google Maps, Yellow Pages and Trustpilot.

8 tools. Pay per call on Apify, billed to your own Apify account.
Current prices: https://apify.com/themineworks/lead-generation-mcp

## Connect

Easiest, with Apify sign in (OAuth), in any client that supports remote MCP
servers:

```
https://mcp.apify.com/?tools=themineworks/lead-generation-mcp
```

Direct, with your Apify API token as a Bearer token:

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

Transport is streamable HTTP. Get a token at
https://console.apify.com/account/integrations.

## Tools (8)

- `find_leads`: Find people and their work emails at a company: names, roles and directly-listed emails from the company site plus LinkedIn discovery.
- `verify_emails`: Verify email addresses: syntax, DNS MX, live SMTP handshake, disposable-domain and role-mailbox detection.
- `find_site_contacts`: Extract emails, phone numbers and social profiles straight from company websites (homepage plus /contact, /about, /team pages).
- `maps_leads`: Local business leads from Google Maps with MX-verified emails: name, address, phone, website, rating and a verified email per lead.
- `search_places`: Raw Google Maps place search without email extraction: name, category, address, phone, rating, hours.
- `yellowpages_search`: US business listings from Yellow Pages by category and city: name, phone, address, and website.
- `trustpilot_lookup`: Find businesses on Trustpilot by keyword or category: domain, TrustScore and review count.
- `prospect_dossier`: One-call prospect pack for a company: people with emails, site contact channels, live verification of every email found, and Trustpilot reputation.

## Listings

- Apify Store: https://apify.com/themineworks/lead-generation-mcp
- MCP Registry: `com.themineworks/lead-generation-mcp`
