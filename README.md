# Backend e Integrações — Laboratório de Estudo AI-native

Laboratório público para aprender fundamentos reais de Ciência da Computação e
construir software profissional com agentes de IA, começando por backend e
integrações. O percurso combina prática manual, aprendizagem assistida e projetos
AI-native com evidências de compreensão e funcionamento.

Este repositório contém anotações, exercícios e provas de conceito. Projetos finalizados de portfólio são promovidos para repositórios próprios.

## Sobre este percurso

Este é o registro de estudos do autor, não um curso completo nem uma garantia de preparação para uma vaga. Outras pessoas podem usar o percurso como referência e adaptar ritmo, datas e recortes à própria experiência. O painel e os registros de progresso abaixo se referem ao autor, não a quem visita o repositório.

Repositório em evolução: materiais futuros podem estar incompletos e serão revisados conforme o avanço do autor. A Frota Aurora é o universo fictício dos exercícios; sua lore dá contexto às missões, enquanto os conceitos e critérios de aprendizagem descrevem as competências reais praticadas.

### Motivação do autor

Minha especialidade em construção é software. No longo prazo, quero conectar programação, IA, eletrônica e robótica para desenvolver projetos multidisciplinares. Este repositório registra essa aprendizagem, começando pelos fundamentos de desenvolvimento backend.

> Software é minha especialidade. Engenharia é meu playground. Construir coisas é o objetivo.

## Modelo de aprendizagem

> Código que o estudante não consegue explicar, modificar e depurar não conta como aprendizado, mesmo que funcione.

| Modo | Quando usar | Papel da IA |
|---|---|---|
| `[MANUAL-CORE]` | Lógica, algoritmos, estruturas de dados, SQL, debugging, concorrência e fundamentos | Ensinar conceitos, fazer perguntas, dar pistas graduais e revisar depois da tentativa |
| `[AI-ASSISTED]` | Bibliotecas, padrões, APIs e técnicas novas | Consultar documentação, criar testes, oferecer pistas e revisar código depois da abordagem inicial |
| `[AI-NATIVE]` | Projetos reais, portfólio, integrações, automações e produtos | Implementar amplamente depois que problema, requisitos, arquitetura e validação forem definidos |

AI-native não significa abandonar a escrita manual de código. O nível de IA
muda conforme a competência avaliada: fundamentos continuam autorais; projetos
de entrega usam agentes como multiplicadores de capacidade.

Leia o [modelo completo e os critérios de escolha](./docs/LEARNING-MODEL.md).

## Painel de retomada

**Material sob demanda:** somente a semana 1 está ativa. As próximas semanas serão preparadas uma por vez, após revisar suas tentativas, evidências, dificuldades e ponto de parada. Material posterior já existente fica como referência preliminar, não agenda obrigatória. Os módulos futuros ainda não foram adaptados ao recorte essencial; não é necessário segui-los integralmente por antecipação.

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

O caminho padrão é a [trajetória essencial até janeiro de 2027](./docs/trajetoria-essencial.md): estimativa de 16 semanas e 128 horas de carga-base, com a semana 17 reservada apenas como margem. Os aprofundamentos permanecem na [continuação de longo prazo](./docs/continuacao-longo-prazo.md). A numeração física dos módulos não muda; a ordem dos recortes essenciais é `00 → 01 → 03 → 02 → 07 → 12`.

## Por onde começar

1. Leia o [modelo de aprendizagem](./docs/LEARNING-MODEL.md).
2. Abra a atividade atual indicada no [painel de retomada](#painel-de-retomada).
3. Identifique o marcador e o nível de IA permitido.
4. Registre a hipótese, previsão ou abordagem inicial antes de executar.
5. Trabalhe, teste, explique, modifique, depure e guarde evidências reais.
6. Preencha a retrospectiva e o registro de uso da IA somente depois do trabalho.

O percurso começa pelo [módulo 00 — Lógica e JavaScript](./00-logica-javascript/README.md), preparado para quem já teve contato com lógica e programas pequenos em Python, está retomando a prática e ainda não escreve JavaScript. Não é necessário dominar Python antes.

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

Cada atividade declara `[MANUAL-CORE]`, `[AI-ASSISTED]` ou `[AI-NATIVE]`.
O marcador determina se a IA atua como tutora socrática, assistente técnico ou
agente de construção. Atividades ainda sem marcador usam `[MANUAL-CORE]` por
segurança; restrições **sem IA** e **sem consulta** sempre prevalecem.

Em todos os modos, o estudante continua responsável por compreender, validar e
manter o resultado. O uso relevante da IA deve distinguir trabalho próprio,
partes auxiliadas, sugestões aceitas ou rejeitadas e, em projetos AI-native,
falhas da IA e correções humanas. Consulte [as regras detalhadas](./docs/regras-de-uso-de-ia.md).

O Codex recebe as [instruções de tutoria do projeto](./AGENTS.md), que aplicam o
comportamento adequado a cada marcador. O modelo padrão e as instruções de
ativação estão em [configuração da IA](./docs/configuracao-da-ia.md).

Essa combinação conecta três objetivos: fundamentos manuais sustentam a formação
em Ciência da Computação; prática assistida acelera o domínio da stack exigida
no trabalho; projetos AI-native geram portfólio e experiência de construção de
produtos próprios.

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

No módulo 00, use a prática incremental e consulte a [trajetória essencial](./docs/trajetoria-essencial.md) para avançar conforme as evidências de compreensão e a demanda atual.

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
