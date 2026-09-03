# Reorganização da trajetória de Backend — Implementation Plan

**Estado vigente — escopo revisado:** tarefas 1–3 implementadas e revisadas. As antigas tarefas 4–7 abaixo foram adiadas, não concluídas, e não devem ser executadas automaticamente. Somente a semana 1 está ativa; material posterior existente é referência preliminar preservada. Prepare apenas a próxima semana após revisar tentativas, evidências, dificuldades e ponto de parada, mantendo lore da Frota Aurora e autoria. O mapa geral permanece estimativo. Esta manutenção termina com o registro da regra, verificação e merge local na main autorizado pelo usuário, sem push. O restante deste plano é histórico subordinado a esta revisão.

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Reorganizar o repositório em uma trajetória essencial até janeiro de 2027 e uma continuação de longo prazo, com primeira semana detalhada, exercícios temáticos e tutoria que preserve autoria.

**Architecture:** Preservar os diretórios `00`–`15` e transformar documentos centrais em uma camada de navegação por marcos. Os módulos continuam como fontes do conteúdo; recortes essenciais apontam para atividades obrigatórias e o restante permanece como reforço ou continuação, sem renomear caminhos nem alterar tentativas.

**Tech Stack:** Markdown, Git, PowerShell e validação local de links/carga por scripts somente leitura.

**Spec:** `docs/superpowers/specs/2026-09-03-trajetoria-essencial-design.md`

## Global Constraints

- Planejamento-base de 8 horas semanais; horas 9–15 são margem opcional, nunca conteúdo obrigatório.
- A trajetória essencial ocupa 16 semanas estimadas mais uma semana de margem; evidências, não datas, autorizam avanço.
- Todo exercício existente ou futuro contém lore curta de ficção científica, mechas, anime, exploração espacial ou tecnologia futurista; setup puramente mecânico é a única exceção.
- O universo original se chama `Frota Aurora` e não exige conhecimento de franquias.
- Nenhum enunciado fornece solução, algoritmo, pseudocódigo resolutivo, arquitetura, modelagem ou estratégia de testes.
- Preservar tentativas, código, notas preenchidas, evidências, retrospectivas e histórico; não marcar progresso não demonstrado.
- Não fazer push, merge, publicação externa ou iniciar a primeira atividade.
- O primeiro projeto é uma API pequena de registros de expedições; autenticação, ORM, Docker, filas, webhooks, n8n e observabilidade aprofundada ficam fora da primeira versão.

---

### Task 1: Criar a navegação canônica dos dois horizontes

**Files:**
- Create: `docs/trajetoria-essencial.md`
- Create: `docs/continuacao-longo-prazo.md`
- Modify: `README.md`
- Modify: `docs/diario-de-estudo.md`

**Interfaces:**
- Consumes: fases, marcos, carga e limites definidos na especificação.
- Produces: nomes canônicos dos marcos A–E, semanas 1–17 e links usados pelos READMEs de módulos.

- [ ] **Step 1: Registrar a linha de base de integridade**

Run:

```powershell
git status --short --branch
Get-FileHash -Algorithm SHA256 '.\00-logica-javascript\exercicios\pratica\primeiro-programa.mjs'
Get-ChildItem -Recurse -File | Where-Object { $_.FullName -match '\\(evidencias|exercicios\\pratica)\\' } | Sort-Object FullName | Get-FileHash -Algorithm SHA256
```

Expected: branch `codex/reorganizar-trilha-essencial`, árvore limpa antes das edições e hashes disponíveis para comparação final.

- [ ] **Step 2: Criar o documento da trajetória essencial**

Escrever `docs/trajetoria-essencial.md` com: regra de 8 h base e margem opcional; tabela das seis fases e semana 17 de margem; marcos A–E; portões de explicação, modificação, investigação e evidência; redução de escopo quando o calendário não comportar o projeto; e mapa `marco → módulos → missões essenciais → entrega`. Marcar exercícios não essenciais como reforço, sem excluí-los.

- [ ] **Step 3: Criar o documento da continuação**

Escrever `docs/continuacao-longo-prazo.md` com a ordem de dependência: camadas/validação, segurança, ORM/transações, testes e CI adicionais, Docker, APIs/webhooks, filas/confiabilidade, operação, n8n/ETL e empregabilidade contínua. Explicar que o segundo projeto é opcional e só começa após o primeiro estar demonstrável.

- [ ] **Step 4: Transformar a abertura do README em painel de retomada**

Colocar antes das explicações gerais: `Onde estou` = módulo 00, semana 1, sessão 1, sem atividade concluída; `Abra agora` = `00-logica-javascript/guia-de-estudo.md#sessão-1--ambiente-e-primeiro-arquivo-duas-horas`; `Próxima entrega` = primeira tentativa da missão 1 mais registro real; modelo de pedido de ajuda com atividade, entendimento, tentativa, evidência e dúvida; e critérios do Marco A. Substituir o cronograma padrão de 69 semanas por links para os dois horizontes.

- [ ] **Step 5: Ajustar o diário sem inventar progresso**

Manter semana 1 com `0` horas e entrega `—`. Atualizar somente o próximo passo para apontar à sessão 1 e acrescentar instrução para registrar fatos após cada semana, inclusive semanas sem estudo.

- [ ] **Step 6: Verificar navegação e carga**

Run:

```powershell
rg -n "Onde estou|Abra agora|Próxima entrega|Como pedir ajuda|Marco A|16 semanas|semana 17|8 horas|15 horas" README.md docs/trajetoria-essencial.md docs/continuacao-longo-prazo.md
git diff --check
```

Expected: os cinco elementos de retomada aparecem; a trajetória mostra 128 h obrigatórias em 16 semanas e trata a semana 17 apenas como margem.

- [ ] **Step 7: Commit da navegação**

```powershell
git add README.md docs/trajetoria-essencial.md docs/continuacao-longo-prazo.md docs/diario-de-estudo.md
git commit -m "docs: split learning path into essential and long-term horizons"
```

### Task 2: Alinhar o protocolo de tutoria e autonomia

**Files:**
- Modify: `AGENTS.md`
- Modify: `docs/regras-de-uso-de-ia.md`
- Modify: `docs/configuracao-da-ia.md`

**Interfaces:**
- Consumes: protocolo de oito etapas da especificação.
- Produces: regras únicas aplicáveis a todos os módulos, exercícios, POCs e verificações.

- [ ] **Step 1: Atualizar o fluxo operacional do tutor**

No `AGENTS.md`, exigir leitura da atividade atual, evidências e ponto de parada; uma atividade pequena por vez; explicação direta de conceito novo com exemplo independente; tentativa antes de ajuda específica; uma pista por interação; revisão separando acertos verificáveis e lacunas; explicação e pequena alteração autoral; encerramento com próximo passo e registro factual.

- [ ] **Step 2: Tornar explícitos os limites humanos e pedagógicos**

Adicionar que dificuldade, demora e desânimo não autorizam interpretação psicológica. O tutor deve investigar compreensão, tamanho da tarefa e condições de execução. Manter integralmente as restrições de atividades `sem IA` e `sem consulta`.

- [ ] **Step 3: Sincronizar regras e configuração**

Em `docs/regras-de-uso-de-ia.md`, distinguir explicação direta permitida de ajuda específica condicionada a tentativa. Em `docs/configuracao-da-ia.md`, atualizar o roteiro de verificação do comportamento para testar objetivo pequeno, pista única, ausência de gabarito e fechamento factual. Não alterar ou inventar configuração de modelo.

- [ ] **Step 4: Verificar consistência textual**

Run:

```powershell
rg -n "uma atividade por vez|conceitos novos|uma pista|acertos verificáveis|pequena alteração|próximo passo|psicológ|sem IA|sem consulta" AGENTS.md docs/regras-de-uso-de-ia.md docs/configuracao-da-ia.md
git diff --check
```

Expected: os três documentos concordam sobre ajuda direta, tentativa, pistas graduais e avaliações sem assistência.

- [ ] **Step 5: Commit das regras de tutoria**

```powershell
git add AGENTS.md docs/regras-de-uso-de-ia.md docs/configuracao-da-ia.md
git commit -m "docs: align tutoring protocol with evidence-based progression"
```

### Task 3: Reorganizar o Marco A e tematizar todo o módulo 00

**Files:**
- Modify: `00-logica-javascript/README.md`
- Modify: `00-logica-javascript/guia-de-estudo.md`
- Modify: `00-logica-javascript/exercicios/README.md`
- Modify: `00-logica-javascript/poc/README.md`
- Modify: `00-logica-javascript/verificacao-final.md`
- Preserve: `00-logica-javascript/exercicios/pratica/primeiro-programa.mjs`
- Preserve: `00-logica-javascript/evidencias/**`
- Preserve: `00-logica-javascript/retrospectiva.md`

**Interfaces:**
- Consumes: definição do Marco A e regra global da Frota Aurora.
- Produces: primeira semana completa, missões essenciais/revisão e evidências necessárias antes de HTTP.

- [ ] **Step 1: Separar núcleo essencial de reforço**

No README e no guia, definir três semanas estimadas do Marco A sem exigir as 18 atividades no mesmo período. Marcar as missões 1, 3, 4, 6, 7, 12, 13, 14 e 15 como núcleo para cobrir valores/conversão, condição, repetição, função, coleção de objetos, JSON, módulos e reconhecimento de callback. Manter as missões 2, 5, 8–11 e 16–18 como reforço recomendado e como parte da conclusão integral posterior do módulo. A aprovação do Marco A exige evidência dos conceitos, inclusive explicação, modificação e investigação, não contagem cega de exercícios.

- [ ] **Step 2: Detalhar as quatro sessões da semana 1**

Para cada sessão, escrever objetivo, preparação, conceito, missão, entrega, evidência de compreensão e próximo passo. Sessão 1 confere Node e Git, executa o arquivo existente e inicia a missão 1; sessão 2 trabalha operações e conversão; sessão 3 faz variação e explicação; sessão 4 consolida evidências, commit e diário. Não registrar que qualquer etapa ocorreu.

- [ ] **Step 3: Converter os 18 exercícios em missões com lore**

Para cada exercício, preservar o conceito original e adicionar: título temático; duas ou três frases da Frota Aurora; comportamento e restrições; entrega e explicação; variação posterior. Distribuir temas entre energia/temperatura de mechas, inventário de nave, tripulação, expedições, telemetria, registros de missão e biblioteca de anime da tripulação. Não fornecer valores finais, estruturas de dados, nomes de funções, condições, laços ou resultados esperados.

- [ ] **Step 4: Tematizar POC e verificação sem transformá-las em gabarito**

Renomear narrativamente a POC como painel ou registro de bordo, mantendo o estudante responsável por organização e verificações. Ambientar a verificação final no universo Frota Aurora e preservar funções, coleção de objetos, condição, mudança e diagnóstico como critérios, sem copiar as missões essenciais.

- [ ] **Step 5: Confirmar que a tentativa existente não mudou**

Run:

```powershell
Get-FileHash -Algorithm SHA256 '.\00-logica-javascript\exercicios\pratica\primeiro-programa.mjs'
git diff -- '00-logica-javascript/exercicios/pratica/primeiro-programa.mjs' '00-logica-javascript/evidencias' '00-logica-javascript/retrospectiva.md'
```

Expected: hash idêntico à linha de base e nenhum diff nos arquivos preservados.

- [ ] **Step 6: Verificar cobertura e ausência de respostas**

Run:

```powershell
rg -n "^### (Missão )?[0-9]+|Conceito técnico|Lore|Entrega|Explique|Variação" '00-logica-javascript/exercicios/README.md'
rg -n "Semana 1|Sessão 1|Sessão 2|Sessão 3|Sessão 4|Marco A|núcleo essencial|reforço" '00-logica-javascript/README.md' '00-logica-javascript/guia-de-estudo.md'
git diff --check
```

Expected: 18 missões tematizadas; quatro sessões completas; nenhum arquivo de tentativa ou evidência alterado.

- [ ] **Step 7: Commit do Marco A**

```powershell
git add 00-logica-javascript/README.md 00-logica-javascript/guia-de-estudo.md 00-logica-javascript/exercicios/README.md 00-logica-javascript/poc/README.md 00-logica-javascript/verificacao-final.md
git commit -m "docs: turn JavaScript foundation into Frota Aurora missions"
```

### Task 4: Reorganizar o Marco B e tematizar todo o módulo 01

**Files:**
- Modify: `01-http-rest/README.md`
- Modify: `01-http-rest/guia-de-estudo.md`
- Modify: `01-http-rest/exercicios/README.md`
- Modify: `01-http-rest/poc/README.md`
- Preserve: `01-http-rest/evidencias/**`
- Preserve: `01-http-rest/retrospectiva.md`

**Interfaces:**
- Consumes: evidências do Marco A e conceitos de funções, objetos, módulos e callbacks.
- Produces: evidências do Marco B usadas pela API TypeScript do Marco C.

- [ ] **Step 1: Criar o recorte de duas semanas**

Definir missões 1, 3, 4 e 6 como núcleo essencial; manter missões 2 e 5 como reforço. Distribuir 16 horas entre observação HTTP, contrato, servidor pequeno, explicação e registros. Reduzir a prova inicial a uma modificação e explicação sem consulta, mantendo a verificação completa do módulo como aprofundamento posterior.

- [ ] **Step 2: Aplicar lore a todos os seis exercícios**

Ambientar cada exercício como comunicação entre naves, estações ou equipes da Frota Aurora. Preservar respectivamente os conceitos de URL/mensagem, navegador como cliente, métodos/repetição, contrato, evolução do contrato e diagnóstico. Cada missão deve conter conceito, lore, comportamento/restrições, entrega/explicação e variação posterior.

- [ ] **Step 3: Tematizar a POC sem escolher contrato pelo estudante**

Trocar incidentes por um contexto de comunicação ou registros de missão, mantendo `node:http` e o objetivo de observar rotas, corpo, status e erros. O estudante continua escolhendo contrato detalhado, status e verificações. Não fornecer handler, roteamento ou resposta pronta.

- [ ] **Step 4: Verificar cobertura e preservação**

Run:

```powershell
rg -n "Missão 1|Missão 2|Missão 3|Missão 4|Missão 5|Missão 6|Conceito técnico|Lore|Variação" '01-http-rest/exercicios/README.md'
rg -n "duas semanas|núcleo essencial|reforço|Marco B" '01-http-rest/README.md' '01-http-rest/guia-de-estudo.md'
git diff -- '01-http-rest/evidencias' '01-http-rest/retrospectiva.md'
git diff --check
```

Expected: seis missões tematizadas, recorte essencial identificável e nenhum registro anterior alterado.

- [ ] **Step 5: Commit do Marco B**

```powershell
git add 01-http-rest/README.md 01-http-rest/guia-de-estudo.md 01-http-rest/exercicios/README.md 01-http-rest/poc/README.md
git commit -m "docs: frame HTTP practice as Frota Aurora communications"
```

### Task 5: Conectar Node/TypeScript, SQL, testes e publicação ao projeto essencial

**Files:**
- Modify: `02-modelagem-sql/README.md`
- Modify: `03-node-typescript-api/README.md`
- Modify: `07-testes-automatizados/README.md`
- Modify: `12-logs-monitoramento-deploy/README.md`
- Modify: `docs/portfolio-map.md`

**Interfaces:**
- Consumes: Marcos B–D e escopo máximo da API de registros de expedições.
- Produces: projeto do Marco E com limite claro e aplicação profissional explícita.

- [ ] **Step 1: Definir o recorte SQL essencial**

No módulo 02, reservar três semanas para entidades/atributos, chaves, constraints fundamentais, DDL/DML, filtros, agregação, `JOIN` e migrations simples. Mover 3FN aprofundada, índices/`EXPLAIN`, subqueries/CTEs e isolamento para a continuação. Ambientar todos os exercícios descritos no README como dados de expedições, sem fornecer entidades, cardinalidades, consultas ou índices.

- [ ] **Step 2: Definir o recorte Node/TypeScript essencial**

No módulo 03, reservar três semanas para `package.json`, ESM, TypeScript estrito, narrowing básico, promises/`async`/`await`, Fastify e scripts reproduzíveis. Adiar fronteiras arquiteturais aprofundadas. Ambientar as atividades como API de expedições, deixando rotas detalhadas, tipos e divisão interna para o estudante.

- [ ] **Step 3: Delimitar as quatro semanas de integração e testes**

No módulo 07, criar um recorte essencial que integra a API ao PostgreSQL sem exigir ORM, autenticação ou camadas avançadas. Exigir que o estudante identifique riscos e escolha testes essenciais; o material não fornece asserções. Distribuir o trabalho entre persistência, comportamento de erro básico, testes, README e demonstração.

- [ ] **Step 4: Delimitar a semana de publicação**

No módulo 12, criar um recorte essencial de uma semana para documentação de execução e publicação gratuita sem cartão. Se não houver opção gratuita adequada, aceitar demonstração local reproduzível como entrega menor. Logs, métricas, tracing, runbook completo e rollback permanecem no estudo integral posterior.

- [ ] **Step 5: Reescrever o mapa de portfólio**

Colocar a API de registros de expedições como Saída Essencial após o Marco E. Documentar aplicação profissional: contrato HTTP, TypeScript, persistência, consultas, testes, documentação e operação básica. Manter relay de webhooks e pipeline de conciliação como projetos opcionais posteriores; não exigir três projetos.

- [ ] **Step 6: Verificar pré-requisitos e escopo**

Run:

```powershell
rg -n "Marco [CDE]|três semanas|quatro semanas|uma semana|expedições|aplicação profissional|sem ORM|sem autenticação|demonstração local" 02-modelagem-sql/README.md 03-node-typescript-api/README.md 07-testes-automatizados/README.md 12-logs-monitoramento-deploy/README.md docs/portfolio-map.md
git diff --check
```

Expected: ordem HTTP → Node/TypeScript → SQL → integração/testes → documentação/publicação; primeiro projeto limitado a uma API e projetos posteriores opcionais.

- [ ] **Step 7: Commit dos Marcos C–E**

```powershell
git add 02-modelagem-sql/README.md 03-node-typescript-api/README.md 07-testes-automatizados/README.md 12-logs-monitoramento-deploy/README.md docs/portfolio-map.md
git commit -m "docs: connect essential milestones to a demonstrable API"
```

### Task 6: Identificar e preservar a continuação de longo prazo

**Files:**
- Modify: `04-camadas-validacao-erros/README.md`
- Modify: `05-autenticacao-seguranca/README.md`
- Modify: `06-postgres-orm/README.md`
- Modify: `08-docker-ambiente-local/README.md`
- Modify: `09-apis-terceiros-webhooks/README.md`
- Modify: `10-filas-eventos-confiabilidade/README.md`
- Modify: `11-configuracao-ci-cd/README.md`
- Modify: `13-n8n-make-com-codigo/README.md`
- Modify: `14-etl-integracoes-documentacao/README.md`
- Modify: `15-empregabilidade/README.md`

**Interfaces:**
- Consumes: ordem publicada em `docs/continuacao-longo-prazo.md`.
- Produces: aprofundamentos navegáveis sem bloquear o primeiro projeto.

- [ ] **Step 1: Marcar o horizonte e os pré-requisitos conceituais**

Adicionar em cada README o campo `Horizonte: continuação de longo prazo`, link para o documento canônico e pré-requisito real. Remover a impressão de que todos os módulos são obrigatórios antes de buscar estágio ou apresentar o primeiro projeto. Manter tempos atuais como estimativas do estudo integral.

- [ ] **Step 2: Aplicar a regra de lore aos exercícios descritos**

Ambientar exercícios, POCs e defeitos propostos em operações da Frota Aurora: telemetria, hangares de mechas, comunicação entre estações, suprimentos, webhooks de sondas, filas de eventos, deploy de sistemas de bordo e conciliação de expedições. Preservar o conceito técnico e não escolher arquitetura, autenticação, retry, idempotência, mapping, observabilidade ou estratégia de testes.

- [ ] **Step 3: Manter aplicação profissional explícita**

Em cada projeto posterior, explicar em uma frase a competência profissional demonstrada, separando a lore da descrição técnica. Manter Projeto 2 e Projeto 3 opcionais e posteriores à API essencial.

- [ ] **Step 4: Verificar os dez módulos**

Run:

```powershell
rg -l "Horizonte: continuação de longo prazo" 04-camadas-validacao-erros/README.md 05-autenticacao-seguranca/README.md 06-postgres-orm/README.md 08-docker-ambiente-local/README.md 09-apis-terceiros-webhooks/README.md 10-filas-eventos-confiabilidade/README.md 11-configuracao-ci-cd/README.md 13-n8n-make-com-codigo/README.md 14-etl-integracoes-documentacao/README.md 15-empregabilidade/README.md
rg -n "Frota Aurora|mecha|estação|expedição|sonda|telemetria" 04-camadas-validacao-erros/README.md 05-autenticacao-seguranca/README.md 06-postgres-orm/README.md 08-docker-ambiente-local/README.md 09-apis-terceiros-webhooks/README.md 10-filas-eventos-confiabilidade/README.md 11-configuracao-ci-cd/README.md 13-n8n-make-com-codigo/README.md 14-etl-integracoes-documentacao/README.md 15-empregabilidade/README.md
git diff --check
```

Expected: os dez READMEs identificam o horizonte, possuem ambientação e continuam tecnicamente reconhecíveis.

- [ ] **Step 5: Commit da continuação**

```powershell
git add 04-camadas-validacao-erros/README.md 05-autenticacao-seguranca/README.md 06-postgres-orm/README.md 08-docker-ambiente-local/README.md 09-apis-terceiros-webhooks/README.md 10-filas-eventos-confiabilidade/README.md 11-configuracao-ci-cd/README.md 13-n8n-make-com-codigo/README.md 14-etl-integracoes-documentacao/README.md 15-empregabilidade/README.md
git commit -m "docs: move advanced backend topics to long-term continuation"
```

### Task 7: Atualizar templates e executar a auditoria final

**Files:**
- Modify: `templates/modulo/README.md`
- Modify: `templates/modulo/retrospectiva.md`
- Verify: all Markdown files and all preserved learner artifacts

**Interfaces:**
- Consumes: regras canônicas dos dois horizontes e da tutoria.
- Produces: padrão para novos módulos e evidência de que a reorganização é íntegra.

- [ ] **Step 1: Atualizar o template de módulo**

Adicionar campos para horizonte, marco, pré-requisitos verificáveis, conceito técnico, lore Frota Aurora, comportamento/restrições, entrega/explicação, variação posterior, evidências e próximo passo. Declarar que setup mecânico é a única atividade que pode ficar sem lore. Manter IA permitida apenas para fricção mecânica e exemplos independentes.

- [ ] **Step 2: Atualizar o template de retrospectiva**

Adicionar campos factuais para marco, atividade onde parou, evidência vinculada, explicação, modificação, investigação, ajuda usada e próximo passo. Não escrever reflexões ou progresso em nome do estudante.

- [ ] **Step 3: Validar todos os links Markdown relativos**

Run:

```powershell
$falhas = @()
Get-ChildItem -Recurse -Filter '*.md' | ForEach-Object {
  $arquivo = $_
  $texto = Get-Content -Raw -LiteralPath $arquivo.FullName
  [regex]::Matches($texto, '\[[^\]]+\]\(([^)]+)\)') | ForEach-Object {
    $alvo = $_.Groups[1].Value.Split('#')[0]
    if ($alvo -and $alvo -notmatch '^(https?:|mailto:)') {
      $destino = Join-Path $arquivo.DirectoryName ([uri]::UnescapeDataString($alvo).Replace('/', '\'))
      if (-not (Test-Path -LiteralPath $destino)) { $falhas += "$($arquivo.FullName) -> $alvo" }
    }
  }
}
if ($falhas.Count) { $falhas; throw 'Links relativos inválidos.' }
```

Expected: nenhum link relativo aponta para destino ausente.

- [ ] **Step 4: Validar carga, temas e restrições**

Run:

```powershell
rg -n "16 semanas|semana 17|128 h|8 horas|15 horas" README.md docs/trajetoria-essencial.md
rg -n "Frota Aurora|Lore|Variação" 00-logica-javascript/exercicios/README.md 01-http-rest/exercicios/README.md templates/modulo/README.md
rg -n "gabarito|pseudocódigo|arquitetura|modelagem|estratégia de testes|sem IA|sem consulta" AGENTS.md docs/regras-de-uso-de-ia.md
rg -n "Status: Concluído|\| Concluído \|" README.md 00-logica-javascript 01-http-rest 02-modelagem-sql 03-node-typescript-api 04-camadas-validacao-erros 05-autenticacao-seguranca 06-postgres-orm 07-testes-automatizados 08-docker-ambiente-local 09-apis-terceiros-webhooks 10-filas-eventos-confiabilidade 11-configuracao-ci-cd 12-logs-monitoramento-deploy 13-n8n-make-com-codigo 14-etl-integracoes-documentacao 15-empregabilidade
```

Expected: carga-base coerente, regra de lore presente, limites de IA preservados e nenhum módulo marcado como concluído.

- [ ] **Step 5: Comparar artefatos do estudante com a linha de base**

Run:

```powershell
Get-FileHash -Algorithm SHA256 '.\00-logica-javascript\exercicios\pratica\primeiro-programa.mjs'
git diff main...HEAD --name-only | Where-Object { $_ -match '(^|/)(evidencias/|exercicios/pratica/|notas\.md$|retrospectiva\.md$)' }
```

Expected: hash do programa idêntico e nenhuma tentativa, nota, evidência ou retrospectiva aparece na lista modificada.

- [ ] **Step 6: Revisar o diff completo**

Run:

```powershell
git diff --check main...HEAD
git diff --stat main...HEAD
git status --short --branch
```

Expected: somente documentação pedagógica planejada foi alterada; apenas os dois templates desta tarefa permanecem sem commit; branch continua sem push.

- [ ] **Step 7: Commit dos templates**

```powershell
git add templates/modulo/README.md templates/modulo/retrospectiva.md
git commit -m "docs: make lore and evidence explicit in module templates"
```

- [ ] **Step 8: Reexecutar a auditoria após o commit**

Repetir os comandos dos Steps 3–6. Registrar no resumo final apenas resultados efetivamente observados e indicar o caminho exato `00-logica-javascript/guia-de-estudo.md#sessão-1--ambiente-e-primeiro-arquivo-duas-horas` como início, sem executar a sessão.
