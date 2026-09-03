# Trajetória essencial até janeiro de 2027

Esta é a navegação canônica para o primeiro horizonte: fundamentos e uma API pequena, completa e demonstrável. Ela não renumera pastas nem substitui a conclusão integral dos módulos; cada **portão essencial** confirma o domínio necessário para seguir neste horizonte. Os exercícios que não pertencem ao recorte continuam disponíveis como reforço e para a conclusão integral posterior.

## Ritmo, calendário e ordem canônica

A carga-base é de **8 horas por semana**. Até 7 horas adicionais podem ser usadas como margem opcional para repetição, recuperação, leitura complementar, correção autoral e prática; elas não criam conteúdo obrigatório novo. Assim, o limite semanal total é de **15 horas**.

O percurso obrigatório soma **16 semanas e 128 horas**. A **semana 17** é somente uma margem de calendário, de até 8 horas base: ela não integra as 16 semanas nem acrescenta uma fase obrigatória. Se uma evidência não for atingida, o prazo se desloca; o conteúdo não é comprimido.

A numeração física das pastas é preservada. A ordem canônica dos recortes essenciais é:

`00 → 01 → 03 → 02 → 07 → 12`

| Fase | Semanas | Carga-base | Recorte canônico | Resultado observável |
|---|---:|---:|---|---|
| 1. Retomada de JavaScript e Git | 1–3 | 24 h | [00 — Lógica e JavaScript](../00-logica-javascript/README.md) | Programas pequenos explicados, modificados e versionados em commits coerentes |
| 2. HTTP aplicado | 4–5 | 16 h | [01 — HTTP e REST](../01-http-rest/README.md) | Requisições analisadas e servidor HTTP pequeno explicado pelo estudante |
| 3. Node.js e TypeScript | 6–8 | 24 h | [03 — Node e TypeScript](../03-node-typescript-api/README.md) | API em memória com TypeScript estrito, execução reproduzível e comportamento assíncrono compreendido |
| 4. SQL e PostgreSQL essencial | 9–11 | 24 h | [02 — Modelagem SQL](../02-modelagem-sql/README.md) | Esquema autoral pequeno, migrations simples e consultas com filtros, agregação e `JOIN` |
| 5. Projeto integrado, testes e documentação | 12–15 | 32 h | [07 — Testes automatizados](../07-testes-automatizados/README.md) | API persistida com testes essenciais, README técnico e demonstração reproduzível |
| 6. Publicação e apresentação | 16 | 8 h | [12 — Logs, monitoramento e deploy](../12-logs-monitoramento-deploy/README.md) | API publicada quando houver opção gratuita adequada, ou demonstração local reproduzível se a publicação bloquear |
| **Total obrigatório** | **16 semanas** | **128 h** |  |  |

## Marcos e portões de domínio

O avanço depende de evidências, não de calendário, leitura, uso de IA ou de o programa funcionar isoladamente. Antes de atravessar cada portão, o estudante deve explicar o que fez, modificar um comportamento, investigar uma situação preparada para estudo e registrar evidências reais. O registro não precisa fingir perfeição: uma tentativa e uma lacuna factual ajudam a escolher a retomada.

| Marco | Domínio observado |
|---|---|
| **Marco A — fundamentos** | Executar, explicar e modificar JavaScript com valores, decisões, repetições, funções, arrays, objetos, módulos e JSON; usar Git para registrar sessões coerentes. |
| **Marco B — protocolo** | Explicar request e response, método, URL, cabeçalhos, corpo e status; observar e modificar um servidor HTTP pequeno. |
| **Marco C — API tipada** | Executar uma API TypeScript, explicar tipos relevantes e o fluxo assíncrono, e modificar um comportamento sem copiar solução. |
| **Marco D — persistência** | Propor e justificar um modelo pequeno, recriar o banco e escrever consultas fundamentais sem depender de ORM. |
| **Marco E — projeto demonstrável** | Executar testes escolhidos pelo estudante, reconstruir o ambiente, explicar decisões e apresentar a API em cinco minutos. |

## Mapa de avanço essencial

As missões abaixo são recortes de aprendizagem, não gabaritos nem uma substituição dos enunciados dos módulos. Concluir o recorte e atravessar seu portão não marca automaticamente o módulo físico como concluído.

| Marco | Módulos | Missões essenciais | Entrega |
|---|---|---|---|
| A — fundamentos | [00](../00-logica-javascript/README.md) | Na Frota Aurora, use pequenas leituras do painel de bordo como contexto para retomar valores, decisões, repetições, funções, coleções, módulos e JSON; registre sessões coerentes com Git. Atividades além do recorte servem como reforço. | Tentativas autorais de programas pequenos, explicação e modificação registradas. |
| B — protocolo | [01](../01-http-rest/README.md) | Na Frota Aurora, observe mensagens entre a central e uma nave durante a expedição, trabalhando com um servidor HTTP pequeno e foco em request e response. Atividades adicionais permanecem como reforço. | Requisições analisadas, servidor explicado e mudança autoral documentada. |
| C — API tipada | [03](../03-node-typescript-api/README.md) | Na Frota Aurora, acompanhe a telemetria de uma expedição ao executar uma API em memória, estudar TypeScript estrito e observar o fluxo assíncrono. Atividades além do recorte ficam para aprofundamento. | API em memória reproduzível, com tipos e comportamento assíncrono explicados. |
| D — persistência | [02](../02-modelagem-sql/README.md) | Na Frota Aurora, trate os registros de expedição como dados a organizar ao criar um esquema pequeno, migrations simples e consultas de filtro, agregação e `JOIN`, sem ORM. Exercícios adicionais continuam como reforço. | Banco recriável e consultas fundamentais explicadas pelo estudante. |
| E — projeto demonstrável | [07](../07-testes-automatizados/README.md) e [12](../12-logs-monitoramento-deploy/README.md) | Na Frota Aurora, prepare a demonstração de uma API de registros de expedições com persistência, testes essenciais e README; publique apenas quando houver opção gratuita adequada. O restante dos módulos é continuação. | Demonstração reproduzível de uma API com um recurso principal, ou publicação gratuita sem cartão quando viável. |

## Quando o calendário não comportar tudo

Se o Marco A exigir mais de três semanas, os marcos seguintes são deslocados. Para preservar uma entrega até janeiro, reduza o escopo do projeto para um único recurso principal, mantendo persistência, testes e documentação. Não elimine explicação, modificação, investigação ou evidências para cumprir uma data. Esta trajetória não promete empregabilidade; ela organiza uma base demonstrável para continuar aprendendo.

Depois do Marco E, use a [continuação de longo prazo](./continuacao-longo-prazo.md) para retomar os aprofundamentos e concluir os módulos físicos integralmente.