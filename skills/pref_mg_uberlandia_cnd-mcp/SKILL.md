---
name: pref_mg_uberlandia_cnd-mcp
description: Skill da REST API do Prefeitura MG Uberlândia: Certidão Negativa de Débitos na MCP.AI: 1 endpoint em /api/pref_mg_uberlandia_cnd. Prefeitura MG Uberlândia: Certidão Negativa de Débitos, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Prefeitura MG Uberlândia: Certidão Negativa de Débitos — REST API skill

Você tem acesso à **Prefeitura MG Uberlândia: Certidão Negativa de Débitos** REST API na MCP.AI.

> Prefeitura MG Uberlândia: Certidão Negativa de Débitos, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/pref_mg_uberlandia_cnd
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/pref_mg_uberlandia_cnd/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/pref_mg_uberlandia_cnd/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `pref_mg_uberlandia_cnd_consultar`

Prefeitura MG Uberlândia: Certidão Negativa de Débitos, consulta em fonte oficial. _(POST /api/pref_mg_uberlandia_cnd/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `im` | string | Não | Parâmetro de consulta "im". |
| `inscricao_imovel` | string | Não | Parâmetro de consulta "inscricao_imovel". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_pref_mg_uberlandia_cnd` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
