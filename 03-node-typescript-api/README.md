# 03-node-typescript-api

**Alvo:** Backend Júnior
**Pré-requisito:** `02-modelagem-sql`
**Tempo estimado:** 5 semanas a 8h/semana

## Objetivo

Implementar uma API TypeScript com tipos úteis, rotas assíncronas e configuração reproduzível.

## Conteúdo

- `package.json`, scripts, dependências e módulos ESM.
- TypeScript estrito, interfaces, unions e narrowing.
- Event loop, promises e `async/await`.
- Fastify como adaptador HTTP.
- Lint, formatação, build e configuração.
- Tipos de domínio versus tipos de transporte.

## Entregável no repo

- `poc/api-operacoes/` com repositório em memória.
- Rotas de incidentes e implantações.
- `tsconfig.json` estrito e scripts `dev`, `build`, `start` e `typecheck`.
- Diagrama request → handler → serviço → repositório.
- IA aceitável: configuração inicial e boilerplate de ferramenta.
- IA proibida: desenhar domínio ou limites de funções/camadas.

## Projeto-portfólio

Início da API de operações e SLA. Ainda permanece como POC neste repo.

## Critério de verificação binário

Reconstruir o esqueleto tipado em 45 minutos e explicar o que o compilador impede em cada fronteira.

## Checklist

- [ ] Typecheck estrito sem erros.
- [ ] API executável e documentada.
- [ ] Bug assíncrono diagnosticado sem IA.
- [ ] Prova binária e retrospectiva concluídas.

## Recursos gratuitos

- [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)
- [Node.js — Learn](https://nodejs.org/en/learn)
- [Fastify — Getting Started](https://fastify.dev/docs/latest/Guides/Getting-Started/)
