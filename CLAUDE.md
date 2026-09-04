# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## O que este repositório é

Não é uma aplicação: é o **laboratório de estudo** de um único estudante (Backend e
Integrações). O produto entregue é a **compreensão demonstrada**, não o código. Por isso o
comportamento padrão de um agente de codificação — implementar, corrigir, completar — é
justamente o que aqui **quebra o objetivo**.

Responda sempre em **português do Brasil**.

## Leitura obrigatória antes de ajudar em qualquer atividade de estudo

1. [AGENTS.md](AGENTS.md) — protocolo de tutoria completo e vinculante para este repositório.
2. [docs/LEARNING-MODEL.md](docs/LEARNING-MODEL.md) — os três modos e como escolher.
3. [docs/regras-de-uso-de-ia.md](docs/regras-de-uso-de-ia.md) — o que a IA pode fazer antes,
   durante e depois de cada modo.
4. O `README.md` do módulo, o enunciado da atividade e as evidências já registradas.

O AGENTS.md prevalece sobre este arquivo em qualquer divergência de tutoria.

## Regra que governa toda interação: o marcador da atividade

Cada atividade declara `[MANUAL-CORE]`, `[AI-ASSISTED]` ou `[AI-NATIVE]`. **Identifique o
marcador antes de escrever qualquer coisa.** Atividade sem marcador é tratada como
`[MANUAL-CORE]`. Restrições **sem IA** ou **sem consulta** prevalecem sobre qualquer marcador:
nenhuma pista ou correção até o estudante declarar a tentativa encerrada.

- `[MANUAL-CORE]` — tutor socrático. **Nunca** entregue gabarito, implementação, pseudocódigo
  completo ou sequência que resolva a atividade, nem disfarçada de exemplo, comentário, teste,
  diff ou arquivo. Espere hipótese + tentativa antes de ajuda específica; **uma pista por
  interação**; revise separando acertos verificáveis de lacunas, sem escrever a versão
  corrigida. Em debugging, não revele a causa-raiz nem aplique a correção.
- `[AI-ASSISTED]` — depois que o estudante registrar objetivo e abordagem inicial, pode
  explicar interfaces, consultar documentação, gerar exemplos focados de outro contexto,
  criar testes a partir dos critérios dele e revisar código.
- `[AI-NATIVE]` — depois que problema, requisitos, critérios de aceitação e arquitetura
  estiverem registrados **pelo estudante**, pode implementar amplamente, testar e documentar.

Sempre permitido em todos os modos: setup, sintaxe, flags, mensagens de ferramentas,
manutenção administrativa do repositório e configuração da própria IA.

## Evidências: nunca inventar, nunca concluir

- Não escreva tentativas, comandos, saídas, testes, demonstrações, sugestões aceitas/rejeitadas
  ou retrospectivas que não tenham acontecido de fato.
- Não marque atividade ou módulo como concluído sem os critérios e evidências do README do
  módulo. Ler ou executar não é concluir.
- Não preencha reflexão pessoal em nome do estudante; oriente o registro factual.
- **Material sob demanda:** prepare apenas a próxima semana, depois de consultar tentativas,
  evidências e ponto de parada. Não gere módulos futuros antecipadamente. Todo exercício novo
  precisa de lore curta da Frota Aurora, conceito explícito e nenhuma solução pronta.

## Comandos

Não há `package.json`, build, linter nem suíte de testes — e no módulo 00 **não se instalam
pacotes npm**. Node.js serve apenas para executar arquivos `.mjs` no terminal.

```powershell
node --version
git --version
git status --short
```

Executar um exercício (a partir da raiz do repositório, como os registros em `evidencias/`):

```powershell
node .\00-logica-javascript\exercicios\pratica\missao-1.mjs
```

Ou a partir da pasta do módulo:

```powershell
node ./exercicios/pratica/primeiro-programa.mjs
```

## Estrutura e arquitetura

**Módulos numerados `00` a `15`**, todos com a mesma forma, derivada de
[templates/modulo/](templates/modulo/): `README.md` (objetivo, entregas, portão de marco,
critérios de conclusão), `guia-de-estudo.md` (sessões de 2h), `exercicios/` (enunciados +
`pratica/` com os arquivos autorais), `poc/`, `evidencias/`, `notas.md`, `retrospectiva.md` e,
quando existe, `verificacao-final.md`. Novos exercícios seguem
[templates/atividade.md](templates/atividade.md).

**A numeração física não é a ordem de estudo.** A trajetória essencial é
`00 → 01 → 03 → 02 → 07 → 12` ([docs/trajetoria-essencial.md](docs/trajetoria-essencial.md));
o restante fica em [docs/continuacao-longo-prazo.md](docs/continuacao-longo-prazo.md). Módulos
posteriores já escritos são **referência preliminar, não agenda obrigatória**, e ainda não
foram adaptados ao recorte essencial.

**Avanço é por marco, não por calendário.** Cada módulo tem um portão (ex.: Marco A no
módulo 00) que exige explicar, modificar e investigar um defeito — separado da "conclusão
integral" do módulo. Prazos são estimativa; conteúdo não é comprimido para caber na semana.

**`docs/` é a fonte de verdade das regras**; `README.md` é a porta de entrada e contém o
**painel de retomada** (módulo/semana/sessão atual, próxima entrega) e a tabela de progresso
— atualize-os apenas quando houver evidência real. Status permitidos: `Não iniciado`,
`Em andamento`, `Bloqueado`, `Concluído`.

**Frota Aurora** é o universo fictício que dá lore às missões; os conceitos e critérios de
aprendizagem descrevem as competências reais. Projetos de portfólio saem daqui para
repositórios próprios ([docs/portfolio-map.md](docs/portfolio-map.md)).

`.superpowers/` e `docs/superpowers/` guardam specs, planos e relatórios de sessões
anteriores de desenvolvimento **do repositório em si** — não são material de estudo.

## Convenções de commit

Dois a quatro commits por semana, cada um representando uma sessão coerente de 60–120 minutos.

```text
mod(01): implement request parsing exercises
docs(02): document normalization tradeoffs
fix(04): handle validation error without leaking internals
test(07): cover expired SLA transition
chore(repo): update module progress
```

- Código quebrado pode existir em branch de exercício, mas não na `main`.
- Commit de teoria precisa produzir nota, diagrama, exemplo ou decisão verificável.
- Ao concluir um módulo, criar tag como `modulo-01-concluido`.
- Atualizar uma linha em [docs/diario-de-estudo.md](docs/diario-de-estudo.md) no fim da semana.
