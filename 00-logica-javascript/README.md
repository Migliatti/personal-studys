# 00 — Revisão de lógica e fundamentos de JavaScript

**Alvo:** Ambos
**Pré-requisito:** contato anterior com lógica de programação; não exige fluência em Python ou JavaScript.
**Horizonte:** [trajetória essencial](../docs/trajetoria-essencial.md), Marco A; conclusão integral posterior com reforço.
**Tempo estimado do Marco A:** 3 semanas a 8h/semana (24 horas), condicionado às evidências.
**Status:** Não iniciado.

## Objetivo

Escrever, explicar, modificar e investigar programas pequenos em JavaScript com autonomia suficiente para começar o módulo de HTTP.

Seu contato anterior com lógica e programas pequenos em Python é um ponto de partida, não comprovação de domínio. As tentativas vão mostrar o que precisa de revisão.

## Comece aqui

Abra a [sessão 1 — ambiente e primeiro arquivo](./guia-de-estudo.md#sessão-1--ambiente-e-primeiro-arquivo-duas-horas). Confira Node e Git, execute o arquivo de preparação existente e inicie sua tentativa da missão 1. Isso é um próximo passo, não registro de atividade realizada.

| Material | Finalidade |
|---|---|
| [Guia de estudo](./guia-de-estudo.md) | Primeira semana detalhada e três semanas estimadas do Marco A |
| [Exercícios](./exercicios/README.md) | 18 missões da Frota Aurora: núcleo essencial e reforço, sem gabarito |
| [Pasta de prática](./exercicios/pratica/) | Seus arquivos de exercícios |
| [POC](./poc/README.md) | Painel de leituras de bordo no terminal |
| [Pasta da POC](./poc/organizador-leituras/) | Sua implementação; caminho preservado |
| [Verificação final](./verificacao-final.md) | Avaliação individual da conclusão integral, separada do Marco A |
| [Notas](./notas.md) | Explicações e dúvidas autorais |
| [Evidências](./evidencias/README.md) | Registros reais de execução, mudança e diagnóstico |
| [Retrospectiva](./retrospectiva.md) | Revisão após a prática |

## Conteúdo

- Algoritmo, entrada, processamento e saída.
- JavaScript, Node.js e terminal; executar arquivos e registrar sessões com Git.
- Valores, tipos básicos, variáveis, operadores, strings e conversões.
- Comparações, booleanos, condições e repetições.
- Funções, parâmetros, retorno e escopo.
- Arrays, objetos, acesso e alteração de dados.
- JSON, módulos e reconhecimento de callbacks.
- Leitura de erros e investigação orientada por hipóteses.

Node.js será usado desde o começo apenas para executar JavaScript no terminal. HTML, DOM, frameworks, banco de dados e TypeScript não são necessários. Promises, event loop e `async/await` serão aprofundados no módulo 03; aqui basta reconhecer a diferença entre chamar uma função e entregá-la para outra operação chamar.

## Núcleo essencial e reforço

O **núcleo essencial** contém as missões **1, 3, 4, 6, 7, 12, 13, 14 e 15**: valores e conversão, condição, repetição, função, coleção de objetos, JSON, módulos e reconhecimento de callback. Siga essa ordem, uma missão por vez. A missão 7 é autossuficiente: não exige realizar a missão 2 antes.

As missões **2, 5, 8–11 e 16–18** são **reforço recomendado** e integram a conclusão integral posterior. Use-as conforme as lacunas; não é necessário encaixar as 18 atividades nas três semanas. O reforço não desaparece nem se torna requisito oculto do Marco A.

## Entregas do Marco A

- Tentativas autorais do núcleo em `exercicios/pratica/`, com comandos e observações reais.
- POC em `poc/organizador-leituras/`, com instrução de execução e evidências dos comportamentos definidos no enunciado.
- Explicação, modificação e investigação próprias, conforme o portão abaixo.
- Registros factuais em notas, evidências e diário; commits coerentes com o trabalho realizado.

## Entregas para a conclusão integral posterior

- Arquivos autorais dos 18 exercícios em `exercicios/pratica/`.
- Painel de leituras de bordo em `poc/organizador-leituras/`, com instrução de execução.
- Programa da verificação final em `evidencias/verificacao/`.
- Notas, registros de execução e retrospectiva preenchidos depois das atividades.
- Nenhuma solução, resposta esperada ou teste de exercício vem preenchido.

## Ritmo e progressão

Quatro sessões de até duas horas por semana, com base de 8 horas. Até 7 horas adicionais são margem opcional para repetição e recuperação, não conteúdo obrigatório novo.

| Semana estimada | Foco do Marco A | Evidência a construir |
|---|---|---|
| Semana 1 | Ambiente, Git, valores e conversão; missões 1 e 3 | Tentativa, previsão, saída real, variação explicada e commit |
| Semana 2 | Condições, repetição, funções e coleções; missões 4, 6, 7 e 12 | Regras, término, parâmetros, retorno e representação explicados |
| Semana 3 | JSON, módulos e callback; missões 13–15, POC e portão | Execução, explicação, modificação e investigação registradas |

O prazo é estimativa, não limite para aprender. Se não conseguir escrever, explicar, modificar ou investigar, acrescente sessões e desloque os marcos seguintes. Não comprima conteúdo para cumprir o calendário. O reforço e a avaliação integral têm ritmo posterior próprio.

## Uso de IA

Valem as [regras do repositório](../docs/regras-de-uso-de-ia.md) e a [tutoria](../AGENTS.md).

Na prática assistida, apresente sua tentativa para receber uma pista de cada vez. Setup e dúvidas conceituais gerais ou de sintaxe podem receber ajuda direta. Raciocínio, organização, verificações e alterações são seus. A IA não escreve programas, corrige arquivos avaliados nem fornece resultados esperados.

As etapas independentes do Marco A, a missão 17 e a verificação final têm restrições próprias. Nenhuma pista ou correção durante etapas sem IA ou sem consulta; declare a tentativa encerrada antes de pedir revisão.

## Projeto-portfólio

Nenhum. Esta POC é de aprendizagem e permanece no repositório.

## Portão do Marco A — antes de HTTP

**Lore:** na Frota Aurora, a equipe precisa confiar que você entende os pequenos programas do painel de bordo. Antes da próxima expedição, apresente suas próprias tentativas e investigue uma ocorrência de treinamento.

**Conceito técnico:** integração dos fundamentos, Git e investigação por hipóteses. **Entrega:** registros reais ligados aos arquivos e versões usados; não é uma nova implementação nem uma contagem de exercícios.

Use suas tentativas essenciais e a POC para demonstrar todos os itens:

- [ ] Executo os programas a partir dos comandos registrados e explico entrada, processamento e saída.
- [ ] Explico valores e conversões, condições, término de repetições, funções, parâmetros, retorno, arrays e objetos a partir do que escrevi.
- [ ] Explico e demonstro a diferença entre JSON e objeto em memória, importação/exportação e função, chamada e callback.
- [ ] POC atende ao seu enunciado com verificações escolhidas e justificadas por mim.
- [ ] Escolho uma pequena modificação de comportamento em uma tentativa ou na POC, faço-a sem IA e registro previsão, execução e explicação do efeito; documentação é permitida.
- [ ] Em cópia de um programa meu já verificado, investigo sem IA um defeito pequeno introduzido por mim; registro sintoma, hipóteses, evidências, correção e observação posterior. Preservo o original, não releio a anotação separada da alteração durante a investigação e não deixo a versão defeituosa na `main`. Documentação é permitida; esta prática não comprova diagnóstico de defeito desconhecido.
- [ ] Apresento commits coerentes e registros factuais de progresso, incluindo lacunas existentes.

**Explique:** relacione o comportamento observado às decisões que tomou, sem copiar explicações. **Variação posterior:** a pequena mudança autoral acima deve mostrar compreensão além da execução original; você escolhe a mudança e como verificá-la.

Registre o resultado do **Marco A**, separado do resultado da verificação final, em [execucoes.md](./evidencias/execucoes.md), incluindo links para explicação, mudança, investigação e commits. Se algum item não estiver demonstrado, registre a lacuna e retome o conceito antes de HTTP. Nas etapas sem IA, declare a tentativa encerrada antes de pedir revisão; a IA não escolhe defeito, causa, correção ou verificações.

## Critério de conclusão integral do módulo

Cumprir integralmente os critérios de [verificacao-final.md](./verificacao-final.md), incluindo programa autoral, explicação, mudança e diagnóstico independente. Tempo decorrido, por si só, não aprova nem reprova.

## Checklist da conclusão integral — não é o portão essencial

- [ ] Executei e registrei os 18 exercícios.
- [ ] Consigo explicar valores, condições, repetições, funções, arrays e objetos.
- [ ] Consigo executar um módulo e diferenciar uma função de sua chamada.
- [ ] POC executável e explicada por mim.
- [ ] Modificação independente registrada.
- [ ] Defeito introduzido, investigado e corrigido sem IA.
- [ ] Verificação final executada e evidências registradas.
- [ ] Retrospectiva preenchida.
- [ ] Progresso da trilha atualizado somente após cumprir os critérios.

## Registro

- Início:
- Conclusão:
- Tempo efetivamente gasto:
- Commit/tag de conclusão:

## Recursos gratuitos

Use os capítulos indicados no guia; não tente ler toda a documentação de uma vez.

- [MDN — Guia JavaScript em português](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide)
- [Node.js — Executar scripts no terminal](https://nodejs.org/en/learn/command-line/run-nodejs-scripts-from-the-command-line)
- [MDN — Módulos JavaScript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Modules)

## Próximo módulo

Após demonstrar o **Marco A**, avance para [01 — HTTP e REST](../01-http-rest/README.md) pela trajetória essencial, mesmo que o reforço permaneça pendente. Isso não autoriza marcar o módulo 00 como concluído: a conclusão integral exige os 18 exercícios, a POC e todos os critérios da verificação final.
