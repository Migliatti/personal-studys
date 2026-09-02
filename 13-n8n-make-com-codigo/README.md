# 13-n8n-make-com-codigo

**Alvo:** Analista de Sistemas/Integrações
**Pré-requisito:** `12-logs-monitoramento-deploy`
**Tempo estimado:** 4 semanas a 8h/semana

## Objetivo

Decidir conscientemente o que fica no fluxo visual e o que deve virar código testável.

## Conteúdo

- n8n Community Edition local via Docker.
- Trigger, webhook, schedule e HTTP Request.
- Credenciais, variáveis, expressões e branching.
- Tratamento de falha, execução manual e subworkflow.
- Code node com limites claros.
- Make: cenários, módulos e cotas.
- Critério low-code versus código.
- Exportação e versionamento de workflow.

## Entregável no repo

- `compose.yml` do n8n local.
- Três workflows exportados em JSON.
- Integração dividida entre n8n e API TypeScript.
- ADR sobre o limite entre fluxo visual e código.
- Comparação documentada com Make.
- IA aceitável: localizar node, expressão e configuração mecânica.
- IA proibida: desenhar fluxo, decidir limites ou depurar execução.

## Projeto-portfólio

Início do Pipeline de conciliação de implantações.

## Critério de verificação binário

Reconstruir um workflow sem importar JSON, explicar cada transformação e corrigir uma execução quebrada apenas pelo histórico e logs.

## Checklist

- [ ] n8n executa localmente.
- [ ] Workflows estão exportados e versionados.
- [ ] Limite low-code/código está justificado.
- [ ] Prova binária e retrospectiva concluídas.

## Recursos gratuitos

- [n8n — Docker](https://docs.n8n.io/hosting/installation/docker/)
- [n8n — Community Edition](https://docs.n8n.io/hosting/community-edition-features/)
- [n8n — Sustainable Use License](https://docs.n8n.io/sustainable-use-license/)
- [Make — plano gratuito](https://www.make.com/en/pricing)
