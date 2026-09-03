# Backend e Integrações — Laboratório de Estudo

Trilha prática para transição de suporte técnico para **Backend Júnior** ou **Analista de Sistemas/Integrações**.

Este repositório contém anotações, exercícios e provas de conceito. Projetos finalizados de portfólio são promovidos para repositórios próprios.
## Painel de retomada

### Onde estou

Você está no **módulo 00**, **semana 1**, **sessão 1**. Nenhuma atividade está marcada como concluída.

### Abra agora

Abra a [sessão 1 — ambiente e primeiro arquivo](./00-logica-javascript/guia-de-estudo.md#sessão-1--ambiente-e-primeiro-arquivo-duas-horas).

### Próxima entrega

Faça a primeira tentativa autoral da missão 1 e registre o comando real, a saída observada e o ponto em que parou. O registro deve refletir o que aconteceu, inclusive se a tentativa ficou incompleta.

### Como pedir ajuda

Use este formato curto: **atividade**, **o que entendi**, **minha tentativa**, **evidência** (comando, saída ou mensagem) e **dúvida específica**. Durante uma atividade, peça uma pista pequena por vez; nas etapas sem IA ou sem consulta, encerre a tentativa antes de pedir revisão.

### Como avançar

O **Marco A — fundamentos** exige executar, explicar e modificar JavaScript com valores, decisões, repetições, funções, arrays, objetos, módulos e JSON, além de registrar sessões coerentes com Git. Para avançar, apresente explicação, modificação, investigação e evidências reais; leitura ou código copiado não comprovam domínio.

## Dois horizontes

O caminho padrão é a [trajetória essencial até janeiro de 2027](./docs/trajetoria-essencial.md): 16 semanas e 128 horas obrigatórias, com a semana 17 reservada apenas como margem. Os aprofundamentos permanecem na [continuação de longo prazo](./docs/continuacao-longo-prazo.md). A numeração física dos módulos não muda; a ordem dos recortes essenciais é `00 → 01 → 03 → 02 → 07 → 12`.

## Por onde começar

Comece pelo [módulo 00 — Lógica e JavaScript](./00-logica-javascript/README.md), preparado para quem já teve contato com lógica e programas pequenos em Python, está retomando a prática e ainda não escreve JavaScript. Não é necessário dominar Python antes.

O módulo 00 constrói a base para programar; o 01 aplica essa base a HTTP. Node.js será inicialmente apenas o programa que executa seus arquivos JavaScript. TypeScript e ferramentas de API entram no módulo 03.

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

O Codex recebe as instruções de [tutoria do projeto](./AGENTS.md): uma pista por vez, perguntas orientadoras e revisão das minhas tentativas, sem gabarito. O modelo padrão e as instruções de ativação estão em [configuração da IA](./docs/configuracao-da-ia.md).

## Progresso

| Módulo | Alvo | Status | Conclusão | Projeto/saída |
|---|---|---|---|---|
| [00-logica-javascript](./00-logica-javascript/) | Ambos | Não iniciado | — | — |
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
| API de registros de expedições | Trajetória essencial: recortes 03 → 02 → 07 → 12 | Após atingir o Marco E, com demonstração reproduzível | — | Gratuito sem cartão, quando viável; senão demonstração local |
| API de operações e SLA (opcional posterior) | Aprofundamentos de backend | Somente após o primeiro projeto estar demonstrável | — | — |
| Relay confiável de webhooks (opcional posterior) | Aprofundamentos de integrações | Somente após o primeiro projeto estar demonstrável | — | — |
| Pipeline de conciliação de implantações (opcional posterior) | Aprofundamentos de integrações | Somente após o primeiro projeto estar demonstrável | — | — |

Consulte o [mapa de promoção](./docs/portfolio-map.md).

## Ritmo

Carga-base: **8 horas por semana**. As horas **9–15** são apenas margem opcional para repetição, recuperação, leitura complementar, correção autoral e prática; elas não adicionam conteúdo obrigatório novo.

- 2 horas: teoria aplicada e notas.
- 2 horas: exercícios.
- 3 horas: POC ou projeto.
- 1 hora: debugging, revisão e commit.

No módulo 00, as três horas destinadas à POC são de prática incremental nas primeiras quatro semanas. A POC integradora começa na quinta semana.

Se uma semana for perdida, o cronograma é deslocado. O conteúdo não é comprimido.

## Planejamento

Consulte a [trajetória essencial](./docs/trajetoria-essencial.md) para as fases, marcos, carga e regra de redução de escopo do primeiro horizonte. Consulte a [continuação de longo prazo](./docs/continuacao-longo-prazo.md) para os aprofundamentos posteriores. Avance pelas evidências de compreensão e amplie o prazo quando necessário.

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

Acesse a [sessão 1 do guia do módulo 00](./00-logica-javascript/guia-de-estudo.md#sessão-1--ambiente-e-primeiro-arquivo-duas-horas). Registre a execução e as dúvidas reais antes de seguir para a próxima sessão. As atividades de HTTP começam depois da base do módulo 00.
