# 14-etl-integracoes-documentacao

**Alvo:** Analista de Sistemas/Integrações
**Pré-requisito:** `13-n8n-make-com-codigo`
**Tempo estimado:** 5 semanas a 8h/semana

## Objetivo

Entregar uma integração auditável que extrai, valida, transforma, carrega e reconcilia dados.

## Conteúdo

- ETL versus ELT em escala pequena.
- CSV/JSON, encoding, datas, moeda e timezone.
- Schema, mapping e tabela de domínio.
- Chave de negócio, deduplicação e watermark.
- Reconciliação e quarentena.
- Reprocessamento seguro.
- OpenAPI, catálogo de campos, runbook, SLA/SLO e diagrama de sequência.

## Entregável no repo

- CSV de fornecedor → validação TypeScript → API → PostgreSQL.
- n8n apenas para orquestração e notificação.
- Datasets normal, duplicado, corrompido e fora de ordem.
- Relatório de reconciliação, OpenAPI, mapping, runbook e diagrama.
- IA aceitável: massa fictícia e formatação de documentação já definida.
- IA proibida: mapping, chave, qualidade, retry ou análise de divergência.

## Projeto-portfólio — saída 3

Promover o **Pipeline de conciliação de implantações**: validação, normalização, quarentena, idempotência, reconciliação, n8n, TypeScript, Postgres e runbook.

## Critério de verificação binário

Processar duas vezes um lote com duplicados, registro inválido e falha intermediária; totais finais e relatório devem permanecer corretos.

## Checklist

- [ ] Dados inválidos vão para quarentena.
- [ ] Reprocessamento é seguro.
- [ ] Projeto 3 passou pelo portão de domínio.
- [ ] Repo próprio criado e linkado no README raiz.

## Recursos gratuitos

- [JSON Schema](https://json-schema.org/learn/getting-started-step-by-step)
- [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [n8n — Error handling](https://docs.n8n.io/flow-logic/error-handling/)
- [Mermaid — Sequence diagrams](https://mermaid.js.org/syntax/sequenceDiagram.html)
