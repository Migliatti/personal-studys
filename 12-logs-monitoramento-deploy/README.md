# 12-logs-monitoramento-deploy

**Alvo:** Ambos
**Pré-requisito:** `11-configuracao-ci-cd`
**Tempo estimado:** 4 semanas a 8h/semana

## Objetivo

Publicar uma API e operá-la com logs estruturados, health checks, métricas básicas e procedimento de incidente.

## Conteúdo

- Logs JSON, níveis e request ID.
- Redação de senha, token e PII.
- Health, readiness e liveness.
- Métricas RED: rate, errors e duration.
- Conceitos de tracing e OpenTelemetry.
- Deploy por Git ou container, TLS e cold start.
- Runbook, rollback e post-mortem.
- Limites reais do free tier.

## Entregável no repo

- POC instrumentada e cinco consultas de logs.
- Health e readiness.
- `runbook.md`, `incident-template.md` e `postmortem-exemplo.md`.
- URL pública e commit implantado em `evidencias/deploy.md`.
- IA aceitável: configuração inicial do logger e deploy.
- IA proibida: escolher sinais, diagnosticar incidente ou redigir causa-raiz.

## Ambiente gratuito

- Aplicação Node no Render Free.
- PostgreSQL no Neon Free; não usar Render Postgres, que expira.
- GitHub Actions em repositório público.
- Não cadastrar método de pagamento.

O ambiente é produção de portfólio sem SLA. Se algum cadastro passar a exigir cartão, interrompa e use execução local demonstrável até existir alternativa documentada.

## Projeto-portfólio

Publicar o Projeto 1 ou o Projeto 2.

## Critério de verificação binário

Com apenas um request ID, identificar rota, status, duração, versão e erro; depois fazer rollback documentado para o commit anterior.

## Checklist

- [ ] Logs não expõem segredos.
- [ ] Health/readiness refletem dependências.
- [ ] Deploy usa somente recursos gratuitos e sem cartão.
- [ ] Rollback e prova binária demonstrados.

## Recursos gratuitos

- [Pino](https://getpino.io/)
- [OpenTelemetry JavaScript](https://opentelemetry.io/docs/languages/js/)
- [Render Free](https://render.com/docs/free)
- [Neon Free](https://neon.com/pricing)
