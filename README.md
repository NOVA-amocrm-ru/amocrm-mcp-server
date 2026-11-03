# NOVA MCP Server for amoCRM

Hosted **remote MCP server** for **amoCRM** by **ООО «НОВАЦРМ» (NOVACRM LLC)** (NOVA). Lets Claude, ChatGPT, Cursor, Perplexity and other MCP clients work with your amoCRM account.

> This repository contains **documentation only**. The server is a closed-source SaaS operated by ООО «НОВАЦРМ» (NOVACRM LLC).

- **Endpoint:** `https://sp1-nova.ru/api/mcp-server/mcp/` (Streamable HTTP)
- **Auth:** OAuth 2.1 via amoCRM (dynamic client registration, PKCE). No API keys. Without a token the server returns 401 — expected.
- **Docs:** https://nova-amocrm.ru/widgets/mcp_server
- **Support:** sales@nova-amocrm.ru
- **Privacy policy:** https://nova-amocrm.ru/policy

## Connect
**Claude** (claude.ai / Desktop): Settings → Connectors → Add custom connector → paste the endpoint.
Claude Code: `claude mcp add --transport http amocrm https://sp1-nova.ru/api/mcp-server/mcp/`

**ChatGPT:** Settings → Apps & Connectors → Developer mode → Create → paste the endpoint, auth OAuth.

**Cursor** (`~/.cursor/mcp.json`):
```json
{ "mcpServers": { "amocrm": { "url": "https://sp1-nova.ru/api/mcp-server/mcp/" } } }
```
**VS Code** (`.vscode/mcp.json`):
```json
{ "servers": { "amocrm": { "type": "http", "url": "https://sp1-nova.ru/api/mcp-server/mcp/" } } }
```
**Perplexity:** Plugins → Add custom → Add MCP connector → Remote → paste the endpoint, Authentication: OAuth.

On first use the client opens amoCRM OAuth: choose the account and allow access. The server acts only within the rights of the authorizing user.

## Capabilities
- Leads, contacts, companies, customers: list/search, get, create, update, delete
- Tasks and notes; tags; custom fields; catalogs and links
- Pipelines and stages, Digital Pipeline
- Events, users
- Lead chats and mail
- Salesbot: list, run, edit
- Webhooks

Read-only by default; write methods are enabled in the widget settings. Enable human confirmation in your client for destructive tools.

## Русский
Удалённый MCP-сервер для amoCRM от ООО «НОВАЦРМ» (NOVACRM LLC). Адрес: `https://sp1-nova.ru/api/mcp-server/mcp/`, вход через OAuth amoCRM, ключи не нужны. Вставьте адрес в настройки Claude, ChatGPT, Cursor или Perplexity (см. выше) и разрешите доступ. Инструкция: https://nova-amocrm.ru/widgets/mcp_server. Поддержка: sales@nova-amocrm.ru. Политика конфиденциальности: https://nova-amocrm.ru/policy. В репозитории только документация, код сервера закрыт.
