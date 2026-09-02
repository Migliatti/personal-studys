# Mapa de promoção para portfólio

POCs ficam neste repositório. Um projeto só sai para repo próprio quando passa pelo portão de domínio: explicar, modificar e depurar sem IA.

## Saída 1 — API de operações e SLA

- Promoção: após `07-testes-automatizados`.
- Núcleo: máquina de estados, prazo de SLA, auditoria, autenticação, PostgreSQL e testes.
- Não promover se for apenas CRUD ou se migrations/testes não reconstruírem o ambiente.

## Saída 2 — Relay confiável de webhooks

- Promoção: após `10-filas-eventos-confiabilidade`.
- Núcleo: HMAC, inbox, fila, retry limitado, dead-letter, idempotência e replay.
- Não promover se duplicatas ainda produzirem efeitos repetidos.

## Saída 3 — Pipeline de conciliação de implantações

- Promoção: após `14-etl-integracoes-documentacao`.
- Núcleo: validação, normalização, quarentena, carga incremental, reconciliação, n8n e runbook.
- Não promover se reprocessar o mesmo lote alterar indevidamente o resultado.

## Checklist de promoção

- [ ] Problema e público explicados no README.
- [ ] Ambiente sobe por instruções reproduzíveis.
- [ ] Testes cobrem os principais riscos.
- [ ] Arquitetura e trade-offs estão documentados.
- [ ] Segredos estão ausentes do histórico.
- [ ] Existe runbook de falha e recuperação.
- [ ] Consigo demonstrar o projeto em cinco minutos.
