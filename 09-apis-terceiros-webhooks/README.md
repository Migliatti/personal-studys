# 09-apis-terceiros-webhooks

**Alvo:** Analista de Sistemas/Integrações
**Pré-requisito:** `08-docker-ambiente-local`
**Tempo estimado:** 5 semanas a 8h/semana

## Objetivo

Consumir APIs externas e receber webhooks tratando contratos, limites, autenticação e duplicidade.

## Conteúdo

- Cliente HTTP com timeout e cancelamento.
- API key, bearer token, paginação e rate limit.
- Mapeamento de modelo externo para interno.
- Recebimento, validação e processamento de webhook.
- HMAC, replay, idempotency key e inbox persistente.
- Contract tests e fornecedor simulado.

## Entregável no repo

- Mock de fornecedor de tickets/implantações.
- Consumidor paginado e receptor assinado.
- Tabela de mapeamento de campos.
- Casos duplicado, fora de ordem, assinatura inválida e timeout.
- IA aceitável: sintaxe de `fetch` e boilerplate do mock.
- IA proibida: mapping, idempotência, autenticação ou investigação de falha.

## Projeto-portfólio

Início do Relay confiável de webhooks. Ainda permanece neste repo.

## Critério de verificação binário

Receber o mesmo evento cinco vezes, inclusive em concorrência, e provar que o efeito de negócio ocorreu uma única vez.

## Checklist

- [ ] Contrato externo mapeado.
- [ ] Assinatura e replay tratados.
- [ ] Duplicidade testada em concorrência.
- [ ] Prova binária e retrospectiva concluídas.

## Recursos gratuitos

- [MDN — Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [GitHub REST API](https://docs.github.com/en/rest)
- [Standard Webhooks](https://github.com/standard-webhooks/standard-webhooks)
