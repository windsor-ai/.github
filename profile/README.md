Connect AI assistants and your own code to 350+ business data sources — ads, analytics, CRM, e-commerce, finance — through one MCP server and API.

## Quick Start

### Connect your AI 🔌

- **Claude** — native connector in the [Claude directory](https://claude.com/connectors/windsor-ai) · [setup guide](https://windsor.ai/documentation/windsor-mcp/how-to-integrate-data-into-claude/)
- **ChatGPT** — available as a ChatGPT app · [setup guide](https://windsor.ai/documentation/windsor-mcp/how-to-integrate-data-into-chatgpt/)
- **Claude Code** — [`claude-windsor-ai-plugin`](https://github.com/windsor-ai/claude-windsor-ai-plugin): `/plugin install windsor-ai@claude-plugin-directory`
- **Cursor** — [`windsor-ai-cursor-plugin`](https://github.com/windsor-ai/windsor-ai-cursor-plugin) · [setup guide](https://windsor.ai/documentation/windsor-mcp/how-to-integrate-data-into-cursor/)
- **Any MCP client** — [guide](https://windsor.ai/documentation/windsor-mcp/how-to-connect-windsor-mcp-to-any-ai-client/), or add this to your client's MCP settings:

```json
{ "mcpServers": { "windsor": { "url": "https://mcp.windsor.ai/" } } }
```

### Build in code 💻

```bash
pip install pywindsorai   # Python — or install.packages("windsoraiR") on CRAN
```

```python
from pywindsorai.client import Client

client = Client(api_key)  # API key from onboard.windsor.ai
rows = client.connectors(date_preset="last_7d", fields=["date", "source", "campaign", "clicks", "spend"])
```

Every connected source comes back as plain rows with the fields you asked for:

```python
[
    {"date": "2026-08-10", "source": "google_ads", "campaign": "brand_search",   "clicks": 152, "spend": 84.31},
    {"date": "2026-08-10", "source": "facebook",   "campaign": "retargeting_eu", "clicks": 98,  "spend": 45.02},
    {"date": "2026-08-10", "source": "tiktok",     "campaign": "summer_promo",   "clicks": 61,  "spend": 22.40},
]
```

Or call the [Connectors API](https://windsor.ai/api-documentation) over plain HTTP from any language. You'll need an API key, which you can get at [onboard.windsor.ai](https://onboard.windsor.ai).

## Primitives

- [Windsor MCP](https://mcp.windsor.ai/docs) — one hosted MCP server connecting Claude, ChatGPT, Cursor and any MCP client to 350+ sources, with write actions (pause campaigns, adjust budgets) on supported ad platforms.
- [Connectors API](https://windsor.ai/api-documentation) — unified REST API over every source; OAuth or API key.
- [dbt packages](https://github.com/windsor-ai/dbt-facebook-big_query) — dbt models that turn synced data into analytics-ready warehouse tables.
- [Destinations](https://windsor.ai/destinations/) — BigQuery, Snowflake, Redshift, Looker Studio, Power BI, Tableau, Sheets and more.

## Resources

- [Connector directory](https://windsor.ai/data-integration/) — browse all 350+ data sources
- [Destinations directory](https://windsor.ai/destinations/) — everywhere your data can land: warehouses, BI tools, sheets, AI assistants
- [Developer docs](https://windsor.ai/api-documentation) — API reference, auth, rate limits, write actions
- [llms.txt](https://mcp.windsor.ai/llms.txt) — machine-readable index of Windsor.ai's capabilities for AI agents ([full version](https://mcp.windsor.ai/llms-full.txt) · [live connector list](https://mcp.windsor.ai/datasources))
