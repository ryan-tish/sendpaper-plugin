# Sendpaper for Codex, Muse Code and Claude

Mail real postcards and letters from your agent. The agent drafts the mail and gets back a print preview and a Stripe checkout link. Nothing is mailed until you pay, and a person reviews every piece before it's printed and sent via USPS First-Class (US addresses only).

| Product | Price |
|---|---|
| Postcard 4×6 | $2.99 |
| Postcard 6×9 | $3.99 |
| Letter (up to 3 pages) | $4.99 |

## Install

**Codex plugin**
```
codex plugin marketplace add ryan-tish/sendpaper-plugin
```
**Codex (MCP only):** `codex mcp add sendpaper --url https://sendmypaper.com/mcp`

**Muse Code** — add to settings:
```json
"mcp_servers": { "sendpaper": { "transport": "streamable_http", "url": "https://sendmypaper.com/mcp" } }
```
**Claude Code:** `claude mcp add --transport http sendpaper https://sendmypaper.com/mcp`

## Tools
`get_pricing`, `create_postcard`, `create_letter`, `get_order`, `cancel_order`.

Website: https://sendmypaper.com · API docs: https://sendmypaper.com/docs · [Content policy](https://sendmypaper.com/content-policy)

License: MIT
