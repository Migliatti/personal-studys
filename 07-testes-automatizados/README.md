# 07-testes-automatizados

**Alvo:** Backend Júnior
**Pré-requisito:** `06-postgres-orm`
**Tempo estimado:** 4 semanas a 8h/semana

## Objetivo

Proteger regras importantes com testes unitários, de integração e HTTP que falham pelos motivos certos.

## Conteúdo

- Pirâmide de testes e Arrange, Act, Assert.
- Teste unitário de serviço e HTTP com `inject`.
- Teste de integração com banco separado.
- Fakes, mocks, cobertura e determinismo.
- Testes de autenticação, transação e erro.

## Entregável no repo

- Suíte Vitest com 8 testes de domínio, 6 HTTP e 4 de persistência.
- `test-plan.md` mapeando risco para teste.
- Um teste frágil corrigido e explicado.
- IA aceitável: configuração do runner e casos repetitivos depois do primeiro manual.
- IA proibida: decidir o que testar, asserções-chave ou causa de falha.

## Projeto-portfólio — saída 1

Promover a **API de operações e SLA** para repo próprio: máquina de estados, prazos, auditoria, autenticação, PostgreSQL, migrations, testes e OpenAPI. Não promover se for CRUD puro.

## Critério de verificação binário

Adicionar regra de escalonamento por SLA usando TDD e corrigir sem IA um defeito proposital que cause falso positivo.

## Checklist

- [ ] Riscos mapeados para testes.
- [ ] Suíte determinística.
- [ ] Projeto 1 passou pelo portão de domínio.
- [ ] Repo próprio criado e linkado no README raiz.

## Recursos gratuitos

- [Vitest Guide](https://vitest.dev/guide/)
- [Fastify — Testing](https://fastify.dev/docs/latest/Guides/Testing/)
- [Node.js Test Runner](https://nodejs.org/api/test.html)
