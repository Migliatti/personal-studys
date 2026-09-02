# 11-configuracao-ci-cd

**Alvo:** Ambos
**Pré-requisito:** `10-filas-eventos-confiabilidade`
**Tempo estimado:** 4 semanas a 8h/semana

## Objetivo

Validar cada mudança automaticamente e separar configuração de código.

## Conteúdo

- Ambientes local, teste e produção.
- Variáveis, validação no startup e segredos.
- Build reproduzível.
- Pipeline com lint, typecheck, teste e build.
- GitHub Actions.
- Migration, compatibilidade e rollback.
- Branch curta e pull request próprio.

## Entregável no repo

- `.env.example` e schema de ambiente.
- Workflow GitHub Actions.
- Pipeline falhando para três erros introduzidos.
- `deploy-checklist.md` e `rollback.md`.
- IA aceitável: boilerplate YAML.
- IA proibida: decidir gates, migrations ou investigar falha.

## Projeto-portfólio

Adicionar CI aos Projetos 1 e 2 em seus repos próprios.

## Critério de verificação binário

Quebrar typecheck, teste e build separadamente e provar que cada erro bloqueia o estágio correto.

## Checklist

- [ ] Segredos ausentes do repositório.
- [ ] Pipeline verde no commit válido.
- [ ] Três falhas bloqueadas no estágio correto.
- [ ] Prova binária e retrospectiva concluídas.

## Recursos gratuitos

- [GitHub Actions — Node.js](https://docs.github.com/en/actions/use-cases-and-examples/building-and-testing/building-and-testing-nodejs)
- [GitHub Actions — Billing and usage](https://docs.github.com/en/actions/concepts/billing-and-usage)
- [The Twelve-Factor App — Config](https://12factor.net/config)
