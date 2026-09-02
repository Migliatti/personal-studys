# Backend e Integrações — Laboratório de Estudo

Trilha prática para transição de suporte técnico para **Backend Júnior** ou **Analista de Sistemas/Integrações**.

Este repositório contém anotações, exercícios e provas de conceito. Projetos finalizados de portfólio são promovidos para repositórios próprios.

## Regras de conclusão

Um módulo só pode ser marcado como concluído quando eu consigo:

1. Explicar as decisões sem ler o código.
2. Modificar o comportamento sem copiar uma solução.
3. Localizar e corrigir um defeito introduzido propositalmente.
4. Executar o critério de verificação descrito no módulo.
5. Registrar evidências em `evidencias/`.
6. Preencher `retrospectiva.md`.

Assistir ou ler conteúdo não significa concluir um módulo.

## Uso de IA

IA pode ser usada para setup, sintaxe, boilerplate revisável, explicação de ferramentas e formatação de texto autoral.

IA não pode decidir arquitetura, modelagem, estratégia de testes, causa-raiz, tratamento de falhas, idempotência ou retry.

Se eu não consigo explicar uma sugestão da IA, ela não entra no repositório. Consulte [as regras detalhadas](./docs/regras-de-uso-de-ia.md).

## Progresso

| Módulo | Alvo | Status | Conclusão | Projeto/saída |
|---|---|---|---|---|
| [01-http-rest](./01-http-rest/) | Ambos | Não iniciado | — | — |
| [02-modelagem-sql](./02-modelagem-sql/) | Ambos | Não iniciado | — | — |
| [03-node-typescript-api](./03-node-typescript-api/) | Backend Júnior | Não iniciado | — | Em construção |
| [04-camadas-validacao-erros](./04-camadas-validacao-erros/) | Ambos | Não iniciado | — | Em construção |
| [05-autenticacao-seguranca](./05-autenticacao-seguranca/) | Ambos | Não iniciado | — | Em construção |
| [06-postgres-orm](./06-postgres-orm/) | Backend Júnior | Não iniciado | — | Em construção |
| [07-testes-automatizados](./07-testes-automatizados/) | Backend Júnior | Não iniciado | — | Link após promoção |
| [08-docker-ambiente-local](./08-docker-ambiente-local/) | Ambos | Não iniciado | — | — |
| [09-apis-terceiros-webhooks](./09-apis-terceiros-webhooks/) | Analista de Sistemas/Integrações | Não iniciado | — | Em construção |
| [10-filas-eventos-confiabilidade](./10-filas-eventos-confiabilidade/) | Ambos | Não iniciado | — | Link após promoção |
| [11-configuracao-ci-cd](./11-configuracao-ci-cd/) | Ambos | Não iniciado | — | — |
| [12-logs-monitoramento-deploy](./12-logs-monitoramento-deploy/) | Ambos | Não iniciado | — | Projeto 1 ou 2 publicado |
| [13-n8n-make-com-codigo](./13-n8n-make-com-codigo/) | Analista de Sistemas/Integrações | Não iniciado | — | Em construção |
| [14-etl-integracoes-documentacao](./14-etl-integracoes-documentacao/) | Analista de Sistemas/Integrações | Não iniciado | — | Link após promoção |
| [15-empregabilidade](./15-empregabilidade/) | Ambos | Não iniciado | — | Portfólio revisado |

Status permitidos: `Não iniciado`, `Em andamento`, `Bloqueado` ou `Concluído`.

## Projetos de portfólio

| Projeto | Origem | Momento da promoção | Repositório | Deploy |
|---|---|---|---|---|
| API de operações e SLA | Módulos 03–07 | Ao concluir o módulo 07 | — | — |
| Relay confiável de webhooks | Módulos 09–10 | Ao concluir o módulo 10 | — | — |
| Pipeline de conciliação de implantações | Módulos 13–14 | Ao concluir o módulo 14 | — | — |

Consulte o [mapa de promoção](./docs/portfolio-map.md).

## Ritmo

Carga máxima: **8 horas semanais**.

- 2 horas: teoria aplicada e notas.
- 2 horas: exercícios.
- 3 horas: POC ou projeto.
- 1 hora: debugging, revisão e commit.

Se uma semana for perdida, o cronograma é deslocado. O conteúdo não é comprimido.

## Cronograma

| Fase | Módulos | Semanas |
|---|---|---:|
| Protocolos e dados | 01–02 | 8 |
| Node/TypeScript aplicado | 03–07 | 22 |
| Integrações confiáveis | 08–10 | 13 |
| Deploy e operação | 11–12 | 8 |
| Automação profissional | 13–14 | 9 |
| Empregabilidade | 15 | 3 |
| **Total** | **15 módulos** | **63** |

São aproximadamente 504 horas ou 14,5 meses a 8 horas por semana, dentro do horizonte de 12–18 meses.

## Disciplina de commits

Faça de dois a quatro commits por semana. Cada commit representa uma sessão coerente de 60–120 minutos.

```text
mod(01): implement request parsing exercises
docs(02): document normalization tradeoffs
fix(04): handle validation error without leaking internals
test(07): cover expired SLA transition
chore(repo): update module progress
```

- Código quebrado pode existir em branch de exercício, mas não na `main`.
- Todo commit de teoria precisa produzir uma nota, diagrama, exemplo ou decisão verificável.
- Nunca commitar `.env`, tokens ou senhas.
- Ao concluir um módulo, criar uma tag como `modulo-01-concluido`.
- Atualizar uma linha em `docs/diario-de-estudo.md` no fim da semana.

## Primeira semana

1. Executar três requisições com `curl -v` e documentar sua anatomia.
2. Criar `GET /health` e `GET /incidents/:id` usando apenas `node:http`.
3. Introduzir um erro de status, diagnosticá-lo sem IA e registrar a causa.
