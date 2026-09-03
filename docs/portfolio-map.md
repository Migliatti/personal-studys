# Mapa de promoção para portfólio

POCs ficam neste repositório. Um projeto só sai para repo próprio quando passa pelo portão de domínio: explicar, modificar e depurar sem IA.

## Primeiro projeto — API de registros de expedições

- Referência: [trajetória essencial](./trajetoria-essencial.md), recortes 03 → 02 → 07 → 12.
- Contexto fictício: registros de expedições da Frota Aurora.
- Promoção: após atingir o Marco E, com demonstração reproduzível.
- Escopo: um recurso principal, persistência, testes essenciais escolhidos pelo estudante e README técnico.
- Evidências: reconstruir o ambiente, executar os testes, explicar decisões e demonstrar a API em cinco minutos.
- Publicação: gratuita e sem cartão quando viável; caso contrário, demonstração local reproduzível.
- Uma API pequena pode ser promovida quando esses critérios forem demonstrados. Autenticação, máquina de estados, SLA e runbook operacional avançado não são requisitos deste primeiro horizonte.

## Opções posteriores — aprofundamentos

Os projetos abaixo são referências preliminares, não uma fila obrigatória. Só serão considerados após o primeiro projeto estar demonstrável, conforme o avanço e o interesse do estudante. Seus detalhes serão revisados no momento de uso, mantendo a lore da Frota Aurora, a autoria e as regras de tutoria.

### API de operações e SLA

- Promoção: após `07-testes-automatizados`.
- Núcleo: máquina de estados, prazo de SLA, auditoria, autenticação, PostgreSQL e testes.
- Não promover se for apenas CRUD ou se migrations/testes não reconstruírem o ambiente.

### Relay confiável de webhooks

- Promoção: após `10-filas-eventos-confiabilidade`.
- Núcleo: HMAC, inbox, fila, retry limitado, dead-letter, idempotência e replay.
- Não promover se duplicatas ainda produzirem efeitos repetidos.

### Pipeline de conciliação de implantações

- Promoção: após `14-etl-integracoes-documentacao`.
- Núcleo: validação, normalização, quarentena, carga incremental, reconciliação, n8n e runbook.
- Não promover se reprocessar o mesmo lote alterar indevidamente o resultado.

## Checklist de promoção

Este checklist não marca progresso automaticamente. No primeiro projeto, aplique os critérios do Marco E; exigências operacionais dos aprofundamentos ficam para o respectivo projeto.

- [ ] Problema e público explicados no README.
- [ ] Ambiente sobe por instruções reproduzíveis.
- [ ] Testes cobrem os principais riscos.
- [ ] Arquitetura e trade-offs estão documentados.
- [ ] Segredos estão ausentes do histórico.
- [ ] Nos aprofundamentos operacionais, existe runbook de falha e recuperação.
- [ ] Consigo demonstrar o projeto em cinco minutos.
