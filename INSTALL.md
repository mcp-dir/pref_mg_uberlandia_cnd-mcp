# Instalação rápida

Prefeitura MG Uberlândia: Certidão Negativa de Débitos é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_pref_mg_uberlandia_cnd`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Prefeitura MG Uberlândia: Certidão Negativa de Débitos` / `https://api.mcp.ai/p_pref_mg_uberlandia_cnd`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "pref_mg_uberlandia_cnd": { "type": "http", "url": "https://api.mcp.ai/p_pref_mg_uberlandia_cnd" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=pref_mg_uberlandia_cnd&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wcmVmX21nX3ViZXJsYW5kaWFfY25kIn0=)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "pref_mg_uberlandia_cnd": { "url": "https://api.mcp.ai/p_pref_mg_uberlandia_cnd" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=pref_mg_uberlandia_cnd&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_pref_mg_uberlandia_cnd%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "pref_mg_uberlandia_cnd": { "type": "http", "url": "https://api.mcp.ai/p_pref_mg_uberlandia_cnd" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_pref_mg_uberlandia_cnd
```

Dúvidas? [pref_mg_uberlandia_cnd@mcp.ai](mailto:pref_mg_uberlandia_cnd@mcp.ai)
