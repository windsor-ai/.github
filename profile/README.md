<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://windsor.ai/wp-content/uploads/2019/12/rsz_windsorai-white-png-transparent.png">
  <img alt="Windsor.ai" src="https://windsor.ai/wp-content/uploads/2019/12/rsz_windsorai-dark-blue-png-transparent.png" width="200">
</picture>

Give any AI live access to 350+ business data sources — ads, analytics, CRM, e-commerce, finance — through one MCP server and API. No code, no exports.

## Quick Start

### Connect your AI 🔌

- **Claude** — native connector in the [Claude directory](https://claude.com/connectors/windsor-ai) · [setup guide](https://windsor.ai/documentation/windsor-mcp/how-to-integrate-data-into-claude/)
- **ChatGPT** — available as a ChatGPT app · [setup guide](https://windsor.ai/documentation/windsor-mcp/how-to-integrate-data-into-chatgpt/)
- **Claude Code** — [`claude-windsor-ai-plugin`](https://github.com/windsor-ai/claude-windsor-ai-plugin): `/plugin install windsor-ai@claude-plugin-directory`
- **Cursor** — [`windsor-ai-cursor-plugin`](https://github.com/windsor-ai/windsor-ai-cursor-plugin) · [setup guide](https://windsor.ai/documentation/windsor-mcp/how-to-integrate-data-into-cursor/)
- **Any MCP client** — [guide](https://windsor.ai/documentation/windsor-mcp/how-to-connect-windsor-mcp-to-any-ai-client/), or point it at:

```json
{ "mcpServers": { "windsor": { "url": "https://mcp.windsor.ai/" } } }
```

### Build in code 💻

```bash
pip install pywindsorai   # Python — or install.packages("windsoraiR") on CRAN
```

Or call the [Connectors API](https://windsor.ai/api-documentation) directly. Get a free API key at [onboard.windsor.ai](https://onboard.windsor.ai) — free forever plan, no credit card.

## Primitives

- [Windsor MCP](https://mcp.windsor.ai/docs) — one hosted MCP server connecting Claude, ChatGPT, Cursor and any MCP client to 350+ sources, with write actions (pause campaigns, adjust budgets) on supported ad platforms.
- [Connectors API](https://windsor.ai/api-documentation) — unified REST API over every source; OAuth or API key.
- [dbt packages](https://github.com/windsor-ai/dbt-facebook-big_query) — production-ready models turning synced data into analytics-ready warehouse tables.
- [Destinations](https://windsor.ai/data-integration/) — BigQuery, Snowflake, Redshift, Looker Studio, Power BI, Tableau, Sheets and more.

## Resources

- [Connector directory](https://windsor.ai/data-integration/) — browse all 350+ sources and destinations
- [Developer docs](https://windsor.ai/api-documentation) — API reference, auth, rate limits, write actions
- [llms.txt](https://mcp.windsor.ai/llms.txt) — machine-readable index of Windsor.ai's capabilities for AI agents ([full version](https://mcp.windsor.ai/llms-full.txt) · [live connector list](https://mcp.windsor.ai/datasources))
