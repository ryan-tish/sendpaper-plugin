# Sendpaper for Codex, Muse Code and Claude

Mail real postcards and letters from your agent. The agent drafts the mail and gets back a print preview and a Stripe checkout link. Nothing is mailed until it's paid, by you or by your agent with your approval, and a person reviews every piece before it's printed and sent via USPS First-Class (US addresses only).

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
**Claude Code plugin** (MCP server plus the `send-mail` skill):
```
/plugin marketplace add ryan-tish/sendpaper-plugin
/plugin install sendpaper@sendpaper
```
**Claude Code (MCP only):** `claude mcp add --transport http sendpaper https://sendmypaper.com/mcp`

## Tools
`get_pricing`, `create_postcard`, `create_letter`, `pay_order`, `get_order`, `cancel_order`.

Agents can pay with a Stripe shared payment token you approve (via Stripe Link). See https://docs.sendmypaper.com/guides/agent-payments.

Website: https://sendmypaper.com · Docs: https://docs.sendmypaper.com · Support: support@sendmypaper.com · [Content policy](https://sendmypaper.com/content-policy)

License: MIT
