# AI-Native Learning Model Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Document three learning modes, provide a reusable activity template, and apply the model to three representative activities without altering existing student code or the repository's progression.

**Architecture:** Keep the model centralized in `docs/LEARNING-MODEL.md`, with `README.md` acting as the entry point and `AGENTS.md` plus `docs/regras-de-uso-de-ia.md` enforcing mode-specific behavior. Activities declare one visual marker and use the reusable contract in `templates/atividade.md`; only three existing examples are expanded in place.

**Tech Stack:** Markdown, Git, Node.js only for executing the existing `.mjs` evidence files, and shell-based repository checks with no new dependencies.

**Spec:** `docs/superpowers/specs/2026-09-04-ai-native-learning-model-design.md`

## Global Constraints

- Do not delete, rename, or move existing content.
- Do not modify the student's existing `.mjs` solutions or invent learning evidence.
- Do not add dependencies, CI, or unrelated refactors.
- Preserve the current module order, active-week policy, Frota Aurora themes, and portfolio promotion model.
- Unmarked activities default to `[MANUAL-CORE]` until classified deliberately.
- Keep the central rule visible verbatim: “Código que o estudante não consegue explicar, modificar e depurar não conta como aprendizado, mesmo que funcione.”
- Apply the full activity contract to exactly three existing examples, one per mode.

---

### Task 1: Central learning model and reusable template

**Files:**
- Create: `docs/LEARNING-MODEL.md`
- Create: `templates/atividade.md`
- Modify: `templates/modulo/README.md`

**Interfaces:**
- Consumes: the approved design in `docs/superpowers/specs/2026-09-04-ai-native-learning-model-design.md` and existing retrospective fields in `templates/modulo/retrospectiva.md`.
- Produces: canonical definitions and relative links used by the root README, AI instructions, and three example activities.

- [ ] **Step 1: Create the canonical model**

Write `docs/LEARNING-MODEL.md` with these concrete sections:

1. `# Modelo de aprendizagem AI-native` and the central rule as a blockquote immediately after the introduction.
2. `## Os três modos`, with a comparison table containing marker, best use, student responsibility, allowed AI, and minimum evidence.
3. One subsection for each marker, preserving all rules from the approved spec.
4. `## Como escolher o modo`, using this decision sequence: implementation is the concept → manual; new tool/technique is the concept → assisted; usable delivery is the goal → native; hybrid stages use separate markers or the stricter mode.
5. `## Ciclo de uma atividade`: identify marker, write hypothesis/approach, attempt/build, test, explain/modify/debug, record AI contribution, record evidence and next variation.
6. `## Como registrar a IA`, explicitly separating own work, assisted work, accepted/rejected suggestions, AI failures, human corrections, and understanding validation.
7. `## Relação com a trajetória`, connecting foundations to CS, assisted tool learning to employability, and native projects to solo products.
8. Links to `../templates/atividade.md`, `./regras-de-uso-de-ia.md`, and `../AGENTS.md`.

- [ ] **Step 2: Create the activity contract**

Write `templates/atividade.md` with editable placeholders and exactly these headings:

```markdown
# [MARCADOR] Título

**Temática:**
**Modo de aprendizagem:**
**Conceito treinado:**
**Pré-requisitos:**

## Desafio
## Hipótese ou previsão inicial
## Nível de IA permitido
## Entregável
## Critérios objetivos de conclusão
## Testes ou evidências
## Reflexão posterior
## Contribuições da IA
## Sugestões da IA aceitas ou rejeitadas
## Variação ou desafio seguinte
```

Under the reflection and evidence fields, state that the student fills them only after real work; the IA must not invent content. Under AI level, instruct the author to list permitted and prohibited actions rather than only repeating the marker.

- [ ] **Step 3: Connect the module template**

In `templates/modulo/README.md`, add a `**Modo predominante:**` field below the time estimate. Replace the generic `## Uso de IA` bullets with instructions to classify each exercise or project using the three markers and link to `../../docs/LEARNING-MODEL.md` and `../atividade.md`. Keep the existing checklist and all unrelated fields unchanged.

- [ ] **Step 4: Verify model/template completeness**

Run:

```bash
for marker in MANUAL-CORE AI-ASSISTED AI-NATIVE; do
  rg -q "\\[$marker\\]" docs/LEARNING-MODEL.md || exit 1
done
for heading in \
  'Temática' 'Modo de aprendizagem' 'Conceito treinado' 'Pré-requisitos' \
  'Desafio' 'Hipótese ou previsão inicial' 'Nível de IA permitido' \
  'Entregável' 'Critérios objetivos de conclusão' 'Testes ou evidências' \
  'Reflexão posterior' 'Contribuições da IA' \
  'Sugestões da IA aceitas ou rejeitadas' 'Variação ou desafio seguinte'; do
  rg -q "$heading" templates/atividade.md || exit 1
done
git diff --check
```

Expected: exit status `0` and no `git diff --check` output.

- [ ] **Step 5: Commit the central model**

```bash
git add docs/LEARNING-MODEL.md templates/atividade.md templates/modulo/README.md
git commit -m "docs: define AI-native learning modes"
```

### Task 2: Mode-aware AI instructions

**Files:**
- Modify: `AGENTS.md`
- Modify: `docs/regras-de-uso-de-ia.md`

**Interfaces:**
- Consumes: markers and permissions defined in `docs/LEARNING-MODEL.md`.
- Produces: repository-level tutor behavior and the student's detailed operating rules.

- [ ] **Step 1: Make mode detection mandatory in `AGENTS.md`**

Add near `## Contexto obrigatório`:

- read `docs/LEARNING-MODEL.md` and `docs/regras-de-uso-de-ia.md`;
- identify the activity marker before helping;
- treat an unmarked activity as `[MANUAL-CORE]`;
- never invent attempts, evidence, test results, AI contribution logs, or personal reflections.

Keep the existing Socratic sequence, but label it as the behavior for `[MANUAL-CORE]`. Add concise behavior sections for `[AI-ASSISTED]` and `[AI-NATIVE]` matching the spec. State that mode controls implementation help, while the student always owns explanation, modification, debugging, validation, and factual records.

- [ ] **Step 2: Scope the current global prohibitions by mode**

In `AGENTS.md`, replace the global `## Limites durante exercícios, POCs e projetos de aprendizagem` with mode-specific limits:

- Manual: no solution, complete pseudocode, disguised diff, architecture choice, test strategy, root-cause revelation, or evaluated-file edits before the attempt and review gate.
- Assisted: code generation only after objective and initial approach; documentation lookup, focused examples, test generation from the student's criteria, and review are allowed; final code must be explained and changed by the student.
- Native: large implementation contributions are allowed after requirements and architecture are recorded; require tests, observability, error handling, documentation, functional evidence, and maintenance ownership; do not invent product decisions or evidence.
- `sem IA` and `sem consulta` restrictions override every marker.

- [ ] **Step 3: Rewrite detailed student-facing rules**

Organize `docs/regras-de-uso-de-ia.md` into:

1. central rule;
2. rules common to all modes;
3. one section per mode with before/during/after workflow;
4. precedence for `sem IA` and `sem consulta`;
5. minimum record table with own work, IA contribution, accepted/rejected suggestions, AI failures/human corrections where applicable, validation, and evidence;
6. links to `./LEARNING-MODEL.md` and `../templates/atividade.md`.

Preserve the prior attempt → gradual hint → later review method under `[MANUAL-CORE]`.

- [ ] **Step 4: Verify instruction alignment**

Run:

```bash
for file in AGENTS.md docs/regras-de-uso-de-ia.md; do
  for marker in MANUAL-CORE AI-ASSISTED AI-NATIVE; do
    rg -q "\\[$marker\\]" "$file" || exit 1
  done
done
rg -q 'sem IA.*sem consulta|sem consulta.*sem IA' AGENTS.md docs/regras-de-uso-de-ia.md
git diff --check
```

Expected: all searches succeed, exit status `0`, and no whitespace errors.

- [ ] **Step 5: Commit mode-aware instructions**

```bash
git add AGENTS.md docs/regras-de-uso-de-ia.md
git commit -m "docs: make AI guidance mode-aware"
```

### Task 3: Root README entry path

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: `docs/LEARNING-MODEL.md`, `docs/regras-de-uso-de-ia.md`, existing panel and trajectory links.
- Produces: one unambiguous starting path for students and visitors.

- [ ] **Step 1: Reframe the repository purpose**

Update the opening paragraphs to state that the repository develops real CS foundations and professional software delivery with agents. Preserve the public-study disclaimer, Frota Aurora explanation, motivation quote, active-week policy, module table, and portfolio model.

- [ ] **Step 2: Add a visible mode summary**

Before `## Painel de retomada`, add:

- the central rule as a blockquote;
- a three-row table for `[MANUAL-CORE]`, `[AI-ASSISTED]`, and `[AI-NATIVE]`;
- a direct link to `./docs/LEARNING-MODEL.md`;
- an explicit warning that AI-native does not mean abandoning manual code.

- [ ] **Step 3: Make the start path executable**

Rewrite `## Por onde começar` so its first numbered list is:

1. read the learning model;
2. open the current activity from the resume panel;
3. identify its marker and allowed AI;
4. record hypothesis or initial approach;
5. work, test, explain, modify, debug, and save real evidence;
6. fill the retrospective and AI-use record afterward.

Then retain the current module-00 guidance. Update `## Uso de IA` to explain the mode-based policy and link to the detailed rules, without keeping global prohibitions that contradict assisted/native modes.

- [ ] **Step 4: Verify entry-point copy and links**

Run:

```bash
for text in 'MANUAL-CORE' 'AI-ASSISTED' 'AI-NATIVE' \
  'Código que o estudante não consegue explicar, modificar e depurar não conta como aprendizado'; do
  rg -q "$text" README.md || exit 1
done
test -f docs/LEARNING-MODEL.md
test -f docs/regras-de-uso-de-ia.md
git diff --check
```

Expected: exit status `0` with no whitespace errors.

- [ ] **Step 5: Commit the README path**

```bash
git add README.md
git commit -m "docs: clarify AI-native study entry path"
```

### Task 4: `[MANUAL-CORE]` representative exercise

**Files:**
- Modify: `00-logica-javascript/exercicios/README.md`

**Interfaces:**
- Consumes: the activity fields and manual permissions from the canonical model.
- Produces: a fully classified version of the existing Mission 3 without changing `exercicios/pratica/missao-3.mjs`.

- [ ] **Step 1: Expand Mission 3 in place**

Change its heading to `### [MANUAL-CORE] Missão 3 — Telemetria recebida como texto` and reorganize only that mission with every activity-template field. Preserve its lore, explicit conversion investigation, invalid-number experiment, author-chosen operation/data, and subsequent variation.

Set the AI level to: concepts and one guiding question at a time are allowed; no generated solution code before the student's attempt; complete review only after the attempt. Criteria must require prediction, own attempt, real output, type explanation, a student-chosen modification, and reconstruction or explanation without reading.

- [ ] **Step 2: Preserve existing student code**

Run:

```bash
git diff --exit-code HEAD -- 00-logica-javascript/exercicios/pratica/missao-3.mjs
```

Expected: exit status `0` and no output.

- [ ] **Step 3: Verify the exercise contract**

Run:

```bash
rg -q '^### \[MANUAL-CORE\] Missão 3' 00-logica-javascript/exercicios/README.md
for heading in 'Temática' 'Modo de aprendizagem' 'Conceito treinado' \
  'Pré-requisitos' 'Desafio' 'Hipótese ou previsão inicial' \
  'Nível de IA permitido' 'Entregável' 'Critérios objetivos de conclusão' \
  'Testes ou evidências' 'Reflexão posterior' 'Contribuições da IA' \
  'Sugestões da IA aceitas ou rejeitadas' 'Variação ou desafio seguinte'; do
  rg -q "$heading" 00-logica-javascript/exercicios/README.md || exit 1
done
git diff --check
```

Expected: exit status `0` and no whitespace errors.

- [ ] **Step 4: Commit the manual example**

```bash
git add 00-logica-javascript/exercicios/README.md
git commit -m "docs(00): classify telemetry mission as manual core"
```

### Task 5: `[AI-ASSISTED]` representative POC

**Files:**
- Modify: `01-http-rest/poc/README.md`

**Interfaces:**
- Consumes: the activity fields and assisted permissions from the canonical model, plus the existing HTTP contract file.
- Produces: a fully classified POC that preserves student ownership of HTTP decisions.

- [ ] **Step 1: Expand the POC in place**

Change the heading to `# [AI-ASSISTED] POC — servidor HTTP de incidentes`. Add every activity-template field while preserving the three routes, four student-justified errors, `node:http`, existing sequence, documentation link, and unaided 40-minute final proof.

Set the AI level to allow documentation lookup, syntax help, focused examples from another context, tests generated from the student's recorded contract, and code review. Require the student to record objective and initial approach before generated code, explain the final flow, make one independent modification, and distinguish own/assisted parts. The unaided final proof remains `sem IA` and `sem consulta`, overriding the POC marker for that stage.

- [ ] **Step 2: Verify the assisted contract**

Run:

```bash
rg -q '^# \[AI-ASSISTED\] POC' 01-http-rest/poc/README.md
rg -q 'node:http' 01-http-rest/poc/README.md
rg -q '40 minutos' 01-http-rest/poc/README.md
rg -q 'sem IA' 01-http-rest/poc/README.md
rg -q 'sem consulta' 01-http-rest/poc/README.md
git diff --check
```

Expected: all searches succeed and no whitespace errors appear.

- [ ] **Step 3: Commit the assisted example**

```bash
git add 01-http-rest/poc/README.md
git commit -m "docs(01): classify HTTP POC as AI-assisted"
```

### Task 6: `[AI-NATIVE]` representative project

**Files:**
- Modify: `13-n8n-make-com-codigo/README.md`

**Interfaces:**
- Consumes: the activity fields and native permissions from the canonical model.
- Produces: a fully classified portfolio-oriented pipeline brief within the existing module.

- [ ] **Step 1: Add the project contract under the existing portfolio section**

Keep the module heading and curriculum intact. Expand `## Projeto-portfólio` with a subsection named `### [AI-NATIVE] Pipeline de conciliação de implantações` and all activity-template fields.

Preserve the existing n8n/TypeScript boundary ADR, three exported workflows, local `compose.yml`, comparison with Make, and reconstruction criterion. Define the functional challenge as accepting fictional deployment records, normalizing them through a documented n8n/API boundary, and producing a reproducible reconciliation result. Do not prescribe the architecture.

Set the AI level to allow broad implementation after the student records problem, requirements, acceptance criteria, and architecture. Criteria must require automated tests for code-owned transformations, repeatable workflow evidence, error handling, structured logs or equivalent observability, secret-safe documentation, demonstration or reproducible result, AI failure/human correction log, and a student-performed change and debugging explanation.

- [ ] **Step 2: Remove the conflicting module-wide AI prohibition**

Replace the two `IA aceitável`/`IA proibida` bullets in `## Entregável no repo` with a reference to the activity's `[AI-NATIVE]` rules. Keep the student responsible for deciding the flow/code boundary and for validation.

- [ ] **Step 3: Verify the native contract**

Run:

```bash
rg -q '^### \[AI-NATIVE\] Pipeline de conciliação' 13-n8n-make-com-codigo/README.md
for text in 'testes' 'logs' 'tratamento de falhas' 'documentação' \
  'evidência' 'falhas da IA' 'correções humanas'; do
  rg -qi "$text" 13-n8n-make-com-codigo/README.md || exit 1
done
git diff --check
```

Expected: exit status `0` and no whitespace errors.

- [ ] **Step 4: Commit the native example**

```bash
git add 13-n8n-make-com-codigo/README.md
git commit -m "docs(13): define AI-native reconciliation project"
```

### Task 7: Repository-wide verification and handoff

**Files:**
- Verify only; modify a scoped file only if a check reveals an error introduced by Tasks 1–6.

**Interfaces:**
- Consumes: every artifact produced by Tasks 1–6.
- Produces: evidence that links, commands, examples, and the Git diff satisfy the approved scope.

- [ ] **Step 1: Execute existing JavaScript practice files**

Run:

```bash
for file in 00-logica-javascript/exercicios/pratica/*.mjs; do
  node "$file" >/dev/null || exit 1
done
```

Expected: exit status `0`. Output is intentionally discarded because success is process completion, not invented learning evidence.

- [ ] **Step 2: Validate relative Markdown links in changed Markdown files**

Run this read-only Python snippet without creating files:

```bash
python3 - <<'PY'
import pathlib
import re
import subprocess
import sys

root = pathlib.Path.cwd()
changed = subprocess.check_output(
    ["git", "diff", "origin/main...HEAD", "--name-only", "--", "*.md"],
    text=True,
).splitlines()
pattern = re.compile(r"\[[^\]]*\]\(([^)]+)\)")
errors = []
for name in changed:
    path = root / name
    if not path.exists():
        errors.append(f"missing changed file: {name}")
        continue
    for target in pattern.findall(path.read_text(encoding="utf-8")):
        target = target.strip().split("#", 1)[0]
        if not target or "://" in target or target.startswith("mailto:"):
            continue
        resolved = (path.parent / target).resolve()
        if not resolved.exists():
            errors.append(f"{name}: broken link {target}")
if errors:
    print("\n".join(errors))
    sys.exit(1)
print(f"validated {len(changed)} changed Markdown files")
PY
```

Expected: `validated N changed Markdown files` and exit status `0`.

- [ ] **Step 3: Verify scope and formatting**

Run:

```bash
git diff --check origin/main...HEAD
git status --short
git diff --stat origin/main...HEAD
git diff --name-only origin/main...HEAD
```

Expected: no whitespace errors; clean status; only the approved spec, plan, central docs/templates, instruction files, root README, and three example files are listed.

- [ ] **Step 4: Inspect the final diff**

Run:

```bash
git diff --word-diff=plain origin/main...HEAD -- \
  README.md AGENTS.md docs/LEARNING-MODEL.md docs/regras-de-uso-de-ia.md \
  templates/atividade.md templates/modulo/README.md \
  00-logica-javascript/exercicios/README.md \
  01-http-rest/poc/README.md 13-n8n-make-com-codigo/README.md
```

Expected: no unrelated module rewrites, no student-code changes, no invented evidence, and exactly three fully expanded examples.

- [ ] **Step 5: Report the handoff**

Report created and modified files, decisions, the three classified examples, every verification command and result, and any remaining limitations. Do not claim the remote repository was updated unless commits were pushed successfully.
