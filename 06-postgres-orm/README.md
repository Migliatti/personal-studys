# 06-postgres-orm

**Alvo:** Backend Júnior
**Pré-requisito:** `05-autenticacao-seguranca`
**Tempo estimado:** 5 semanas a 8h/semana

## Objetivo

Persistir a aplicação em PostgreSQL com migrations e ORM sem perder a capacidade de raciocinar em SQL.

## Conteúdo

- Conexão, pool, migrations e seed.
- Prisma como ORM principal.
- Relações, constraints e transações.
- Problema N+1.
- Paginação por offset e cursor.
- SQL cru e erros de unicidade, concorrência e conexão.

## Entregável no repo

- Troca do repositório em memória por PostgreSQL.
- Migrations reproduzíveis do zero.
- Cinco consultas equivalentes em Prisma e SQL.
- Medição do N+1 e correção.
- `evidencias/reset-local-db.md`.
- IA aceitável: CLI, tipos gerados e boilerplate de migration.
- IA proibida: modelagem, transação ou diagnóstico de consulta lenta.

## Projeto-portfólio

Continuação do Projeto 1.

## Critério de verificação binário

Apagar e reconstruir o banco apenas pelas migrations e provar que uma transação não deixa dados parciais quando a segunda operação falha.

## Checklist

- [ ] Banco reconstruído pelas migrations.
- [ ] Prisma comparado com SQL cru.
- [ ] N+1 identificado e corrigido.
- [ ] Prova binária e retrospectiva concluídas.

## Recursos gratuitos

- [Prisma ORM](https://www.prisma.io/docs/orm)
- [PostgreSQL — Transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html)
- [PostgreSQL — EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html)
