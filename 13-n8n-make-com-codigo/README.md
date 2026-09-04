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
- Uso de IA conforme o contrato `[AI-NATIVE]` abaixo; o estudante decide o
  limite entre fluxo visual e código e continua responsável pela validação.

## Projeto-portfólio

### [AI-NATIVE] Pipeline de conciliação de implantações

**Temática:** laboratório de operações da Frota Aurora conciliando registros de
implantações recebidos de sistemas diferentes.
**Modo de aprendizagem:** `[AI-NATIVE]`, porque o objetivo é entregar, demonstrar
e manter uma automação integrada, não memorizar toda a implementação.
**Conceito treinado:** fronteira entre low-code e código, integração por HTTP e
webhook, transformação de dados, versionamento de workflow, confiabilidade e
operação.
**Pré-requisitos:** módulos 00–12, n8n Community Edition local, API TypeScript
testável e fundamentos de logs, testes, Docker e tratamento de falhas.

#### Desafio

Construa um pipeline que receba registros fictícios de implantações, normalize
os dados através de uma fronteira documentada entre n8n e a API TypeScript e
produza um resultado de conciliação reproduzível. Defina o problema exato, as
fontes fictícias, divergências relevantes e arquitetura antes da implementação.

O projeto deve produzir os três workflows exportados, o `compose.yml`, a divisão
entre n8n e código, o ADR dessa fronteira e a comparação com Make já previstos
no módulo. O enunciado não prescreve a arquitetura.

#### Hipótese ou previsão inicial

Antes de pedir implementação à IA, registre:

1. problema e usuário da solução;
2. requisitos e critérios de aceitação;
3. entradas, saídas e falhas esperadas;
4. arquitetura proposta e limite entre fluxo visual e código;
5. evidência que demonstrará funcionamento.

#### Nível de IA permitido

Depois dessas decisões, agentes de IA podem produzir grande parte do código,
workflows, testes e documentação, além de revisar e apoiar o debugging. A IA não
pode inventar requisitos, escolher silenciosamente a arquitetura, declarar
evidências ou escrever decisões e reflexões em nome do estudante.

O estudante aprova as decisões, inspeciona o resultado e continua responsável
por segurança, validação, operação e manutenção.

#### Entregável

- Pipeline executável localmente e três workflows exportados em JSON.
- API TypeScript e transformações próprias de código cobertas por testes.
- `compose.yml`, ADR da fronteira n8n/código e documentação de execução.
- Tratamento de falhas e logs estruturados ou observabilidade equivalente.
- Resultado de conciliação reproduzível ou demonstração funcional.
- Registro das contribuições e falhas da IA, correções humanas e decisões.

#### Critérios objetivos de conclusão

- [ ] Requisitos, critérios de aceitação e arquitetura foram registrados antes
  da geração ampla de implementação.
- [ ] Os três workflows podem ser executados e foram exportados para o Git.
- [ ] Transformações mantidas em código possuem testes automatizados executados.
- [ ] Falhas previstas possuem tratamento verificável e diagnóstico por logs.
- [ ] A documentação permite reproduzir ambiente, execução e demonstração sem
  expor credenciais ou segredos.
- [ ] A evidência funcional mostra entradas fictícias e o resultado conciliado.
- [ ] Falhas da IA e correções humanas relevantes foram registradas.
- [ ] O estudante realizou uma mudança e explicou o debugging correspondente.
- [ ] O critério binário do módulo foi executado.

#### Testes ou evidências

Registre comandos e resultados reais dos testes, histórico de execuções dos
workflows, logs dos caminhos de sucesso e falha, exportações versionadas e uma
demonstração ou roteiro reproduzível da conciliação. Evidência planejada, mas
não executada, não comprova conclusão.

#### Reflexão posterior

Depois da entrega, explique quais partes pertencem ao fluxo visual, quais
pertencem ao código, quais decisões facilitam manutenção e onde a arquitetura
precisou mudar. Não antecipe essa reflexão.

#### Contribuições da IA

Registre pesquisas, código, workflows, testes, documentação e análises produzidos
pela IA. Relacione cada contribuição relevante à validação realizada pelo
estudante.

#### Sugestões da IA aceitas ou rejeitadas

Registre sugestões importantes, aceitação ou rejeição e motivo. Inclua falhas da
IA, efeitos observados e correções humanas aplicadas.

#### Variação ou desafio seguinte

Adicione uma nova divergência fictícia ou condição de falha, preveja seu impacto
na fronteira n8n/código, implemente a mudança com agentes e demonstre que testes,
logs e documentação continuam sustentando o comportamento.

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
