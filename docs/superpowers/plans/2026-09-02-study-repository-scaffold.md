# Study Repository Scaffold Implementation Plan

> Registro histórico da criação dos módulos 01–15. A inclusão posterior do módulo 00 ampliou a trilha para 16 módulos e 69 semanas; o cronograma vigente está no [README principal](../../../README.md). Os resultados abaixo se referem à estrutura original.

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Configurar o repositório Git existente como laboratório sequencial de backend, infraestrutura e integrações.

**Architecture:** O README raiz concentra regras e progresso. Cada módulo é autocontido e usa a mesma estrutura; `docs/` mantém regras transversais e o mapa de promoção para portfólio.

**Tech Stack:** Markdown, Git e a trilha futura de Node.js/TypeScript, PostgreSQL, Docker, Redis/BullMQ, GitHub Actions e n8n.

**Spec:** `docs/superpowers/specs/2026-09-02-backend-integracoes-study-repository-design.md`

## Global Constraints

- Dedicação máxima de 8 horas por semana.
- Horizonte total de 12–18 meses.
- Nenhum requisito pago, trial com cobrança ou cartão de crédito.
- IA somente para fricção mecânica; arquitetura e debugging devem ser autorais.
- Projetos de portfólio concluídos devem sair para repositórios próprios.

## Task 1: Estrutura transversal do repositório

- [x] Substituir o README mínimo pela apresentação, regras e tabela dos 15 módulos.
- [x] Adicionar `.gitignore` para Node/TypeScript, segredos, builds, logs e bancos locais.
- [x] Criar documentos transversais e template copiável de módulo.
- [x] Verificar que o README referencia todos os diretórios numerados.

## Task 2: Conteúdo dos 15 módulos

- [x] Criar os módulos na ordem de dependência aprovada.
- [x] Registrar em cada README alvo, objetivo, conteúdo, entregável, uso de IA, prova binária, tempo e recursos.
- [x] Criar notas, retrospectiva e diretórios versionáveis para exercícios, POC e evidências.
- [x] Confirmar que os tempos somam 63 semanas.

## Task 3: Validação do scaffold

- [x] Listar a árvore versionável com `rg --files`.
- [x] Procurar placeholders proibidos e links locais quebrados.
- [x] Confirmar que não existem segredos ou artefatos gerados.
- [x] Revisar o diff sem realizar commit ou push não solicitado.

## Resultado da validação

- 15 módulos, 15 READMEs, 15 arquivos de notas e 15 retrospectivas.
- Subdiretórios `exercicios/`, `poc/` e `evidencias/` presentes em todos os módulos.
- Soma dos tempos: 63 semanas.
- Links locais: válidos.
- Placeholders proibidos: nenhum.
- `git diff --check`: sem erros; apenas aviso de normalização LF/CRLF no Windows.
