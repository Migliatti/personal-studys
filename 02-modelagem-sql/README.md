# 02-modelagem-sql

**Alvo:** Ambos
**Pré-requisito:** `01-http-rest`
**Tempo estimado:** 5 semanas a 8h/semana

## Objetivo

Modelar dados operacionais e consultar PostgreSQL sem depender de ORM.

## Conteúdo

- Entidade, atributo, relacionamento e cardinalidade.
- Chaves primária, estrangeira, natural e substituta.
- Normalização até 3FN aplicada sem dogmatismo.
- DDL, DML, filtros, agregações, `JOIN`, subqueries e CTE.
- Constraints, índices, `EXPLAIN`, transações e isolamento introdutório.
- Migrações como histórico versionado.

## Entregável no repo

- Modelo de clientes, implantações, incidentes e eventos de auditoria.
- `schema.sql`, `seed.sql` e dez consultas em `exercicios/`.
- Versão inicial e versão corrigida do modelo.
- `evidencias/explain.md` comparando consulta antes/depois de um índice.
- IA aceitável: consulta de sintaxe DDL e geração de seed fictício.
- IA proibida: decidir entidades, cardinalidades, índices ou consultas finais.

## Projeto-portfólio

Nenhum. O modelo será reutilizado no Projeto 1.

## Critério de verificação binário

Em 60 minutos, transformar uma planilha desnormalizada em esquema 3FN, importá-la e consultar implantações fora do SLA com `JOIN`.

## Checklist

- [ ] Schema e seed reproduzíveis.
- [ ] Dez consultas executadas.
- [ ] Índice medido com `EXPLAIN`.
- [ ] Prova binária e retrospectiva concluídas.

## Recursos gratuitos

- [PostgreSQL Tutorial](https://www.postgresql.org/docs/current/tutorial.html)
- [PostgreSQL — Indexes](https://www.postgresql.org/docs/current/indexes.html)
- [SQLBolt](https://sqlbolt.com/)
