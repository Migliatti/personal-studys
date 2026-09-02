# 01-http-rest

**Alvo:** Ambos
**Pré-requisito:** nenhum além de lógica básica
**Tempo estimado:** 3 semanas a 8h/semana

## Objetivo

Construir e diagnosticar uma conversa HTTP, distinguindo método, recurso, representação, status e cabeçalhos.

## Conteúdo

- Request, response, URL, método, cabeçalhos e corpo.
- DNS, TCP e TLS no nível necessário para diagnosticar uma API.
- Safety, idempotência, status `2xx`, `4xx` e `5xx`.
- JSON, negociação de conteúdo, recursos, filtros, paginação e versionamento.
- Diferença entre REST, RPC e HTTP com JSON.
- `curl`, DevTools e cliente HTTP.

## Entregável no repo

- `notas.md` com anatomia de três requisições.
- Exercícios com `curl` contra API pública.
- `poc/servidor-http/` usando `node:http`, sem framework.
- `evidencias/contrato-http.md` com requests, responses e erros.
- IA aceitável: flags do `curl` e sintaxe de `node:http`.
- IA proibida: escolher rotas, status ou semântica de idempotência.

## Projeto-portfólio

Nenhum. A POC permanece neste repositório.

## Critério de verificação binário

Em 40 minutos e sem consulta, criar `GET /health`, `GET /incidents/:id` e `POST /incidents`, retornando pelo menos quatro erros HTTP corretos.

## Checklist

- [ ] Exercícios e POC executáveis.
- [ ] Defeito introduzido e diagnosticado sem IA.
- [ ] Verificação binária registrada em `evidencias/`.
- [ ] Retrospectiva preenchida.

## Recursos gratuitos

- [MDN — Overview of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Overview)
- [RFC 9110 — HTTP Semantics](https://www.rfc-editor.org/rfc/rfc9110)
- [Microsoft REST API Guidelines](https://github.com/microsoft/api-guidelines)
