# Guia de estudo — Lógica e JavaScript

O objetivo é voltar a escrever programas pequenos e ganhar familiaridade com JavaScript. Não precisa lembrar toda a sintaxe de Python nem estudar duas linguagens em paralelo.

## Como usar o material

Leia apenas o bloco da semana, pratique e registre o que aconteceu. Na prática assistida, documentação e ajuda pontual são permitidas. Durante atividades explicitamente sem IA ou sem consulta, encerre a tentativa antes de pedir revisão.

Os exercícios são enunciados, não roteiros de implementação. Escolha seus dados, suas verificações e como dividir o problema. Antes de executar, anote o que espera; depois compare com a saída real. Uma tentativa incompleta registrada vale mais para orientar o estudo do que uma solução copiada.

## Sessão 1 — ambiente e primeiro arquivo (duas horas)

### Preparar — 20 minutos

Abra o repositório no editor. No PowerShell, execute:

```powershell
Set-Location -LiteralPath 'C:\Users\Gabriel Speedpro\Music\projetos\personal-studys\00-logica-javascript'
node --version
```

Na preparação deste módulo, em 02/09/2026, o comando retornou `v24.20.0`. Registre a versão que aparecer na sua sessão. Se o comando não for reconhecido, peça ajuda de setup antes de continuar. Não é necessário instalar pacotes npm.

JavaScript é a linguagem; Node.js executa seus arquivos fora do navegador. O PowerShell recebe o comando que inicia esse programa. Uma instrução JavaScript escrita diretamente no PowerShell não é executada automaticamente como JavaScript.

### Primeiro contato — 20 minutos

No editor, crie `exercicios/pratica/primeiro-programa.mjs` com este conteúdo de preparação:

```javascript
console.log("Comecei minha prática de JavaScript.");
```

Execute a partir da pasta do módulo:

```powershell
node ./exercicios/pratica/primeiro-programa.mjs
```

Essa linha apenas confirma que você consegue salvar e executar um arquivo; não é solução de um exercício. Compare editar o arquivo, salvar e executar novamente. A extensão `.mjs` identifica um módulo JavaScript no Node e será usada neste módulo para manter a configuração simples. Consulte [executar scripts com Node](https://nodejs.org/en/learn/command-line/run-nodejs-scripts-from-the-command-line) e [módulos JavaScript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Modules).

### Valores e variáveis — 30 minutos

Leia o bloco da semana 1 abaixo e o início de “Sintaxe e tipos” no [Guia JavaScript da MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide). Foque em declarações e valores básicos; hoisting e detalhes avançados podem esperar.

### Primeira tentativa — 35 minutos

Leia o exercício 1 e faça uma tentativa na pasta de prática. Se travar, anote o ponto exato. Não precisa terminar os três exercícios da semana nesta sessão.

### Encerrar — 15 minutos

Registre o comando real, o que ele exibiu e uma dúvida em [notas.md](./notas.md). Anote onde parou para retomar na sessão 2. A preparação do ambiente não representa conclusão da semana.

## Semana 1 — valores, variáveis e operações

Um algoritmo descreve como transformar uma entrada em uma saída. Escrever o programa exige tornar explícitas as operações que na explicação verbal podem ficar implícitas.

Em JavaScript, `let` declara uma variável que pode receber outro valor; `const` impede reatribuir aquela variável. Strings representam texto, numbers representam números e booleans representam verdadeiro ou falso. `typeof` permite observar o tipo de um valor. Você também encontrará `undefined` e `null`; registre como aparecem na sua prática.

Exemplo isolado de declaração, sem relação com as atividades:

```javascript
const idioma = "português";
let paginaAtual = 4;
```

Estude operadores aritméticos, precedência, parênteses e conversão explícita com `Number`. Texto contendo dígitos continua sendo texto até uma conversão. Não suponha que todos os operadores tratam texto da mesma maneira. Aprenda também concatenação e template literals para compor mensagens.

**Leitura:** capítulos “Sintaxe e tipos”, “Expressões e operadores” e “Formatação de texto” do [guia MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide), apenas os tópicos acima.

**Prática:** exercícios 1–3. Nesta semana, entradas podem ser valores escritos no próprio arquivo; ler pelo teclado não é um pré-requisito.

**Antes de avançar:** consiga alterar um valor, executar novamente e explicar a operação realizada e o tipo dos valores usados.

## Semana 2 — decisões e repetições

Uma condição produz um valor booleano; `if` e `else` permitem escolher um caminho. Estude comparações, igualdade estrita (`===`), diferença (`!==`), `&&`, `||` e `!`. A atribuição `=` tem outra finalidade. JavaScript usa chaves para delimitar blocos; a indentação ajuda a leitura.

Repetir uma ação exige entender quando continuar e quando terminar. Estude `for` e `while`. Antes de executar um laço, explique por que ele termina. Se um programa ficar executando sem parar, `Ctrl+C` interrompe a execução no terminal.

**Leitura:** “Controle de fluxo” (condicionais) e “Laços e iteração” do [guia MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide).

**Prática:** exercícios 4–6. Não é necessário usar arrays ainda.

**Antes de avançar:** explique qual regra seu programa representa e como uma repetição altera o estado do programa.

## Semana 3 — funções e escopo

Uma função agrupa um comportamento que pode receber argumentos e retornar um valor. Parâmetros são os nomes usados na definição; argumentos são os valores fornecidos na chamada. `return` devolve um resultado para quem chamou. Mostrar algo com `console.log` e retornar um valor cumprem papéis diferentes.

Estude declaração com `function`, chamada, retorno e escopo de bloco/função. Observe quais variáveis cada trecho pode acessar. Quando a declaração tradicional estiver clara, reconheça a sintaxe de arrow functions (`=>`); não precisa reescrever tudo com ela.

**Leitura:** “Funções”, com foco em definição, chamada, parâmetros, retorno e escopo, no [guia MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide). Closures avançadas e recursão não são exigidas.

**Prática:** exercícios 7–9. Você decide os nomes, os parâmetros e a divisão em funções.

**Antes de avançar:** consiga explicar o que entra, o que sai e quando a função é executada.

## Semana 4 — listas e objetos

Arrays guardam uma sequência de valores, com posições iniciando em zero. Objetos relacionam propriedades a valores. Compare representar uma informação isolada e várias informações relacionadas, sem assumir que existe uma estrutura universal para todo problema.

Estude acesso por índice, `length`, inclusão com `push`, percurso com `for...of`, leitura e alteração de propriedades. Um array pode conter objetos. Duas variáveis podem apontar para o mesmo objeto; observe a diferença entre alterar esse objeto e reatribuir uma variável declarada com `const`.

**Leitura:** “Coleções indexadas” (arrays) e “Trabalhando com objetos” do [guia MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide).

**Prática:** exercícios 10–12. Métodos como `map` e `filter` são aprofundamento opcional; não são requisito para resolver as atividades.

**Antes de avançar:** consiga percorrer uma coleção, acessar propriedades e explicar suas escolhas de representação.

## Semana 5 — JSON, módulos e callbacks

JSON é uma representação textual de dados, não um objeto JavaScript em memória. Estude `JSON.stringify` e `JSON.parse` e observe o tipo do valor antes e depois de cada operação. Nem todo valor JavaScript tem representação em JSON.

Módulos permitem exportar e importar valores e funções. Use arquivos `.mjs`, caminhos relativos e extensão explícita ao importar um arquivo local. O que pertence a cada arquivo continua sendo sua decisão.

Uma função também é um valor: ela pode ser passada como argumento para outra função. Uma função recebida para ser chamada é frequentemente chamada de callback. Callback não significa, por si só, execução assíncrona. Compare entregar uma função com chamá-la imediatamente.

Faça um contato inicial com `setTimeout` para observar uma chamada agendada. O atraso solicitado não garante um instante exato de execução. Você não precisa implementar HTTP, promises ou `async/await` aqui.

**Leitura:** “Funções” do [guia MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide), [módulos](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Modules), [JSON](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/JSON) e [timers do Node](https://nodejs.org/api/timers.html).

**Prática:** exercícios 13–15. Comece a POC depois dessas atividades; callbacks são praticados nos exercícios e não são uma exigência artificial da POC.

**Antes de avançar:** consiga executar arquivos com importação e explicar função, chamada e callback.

## Semana 6 — integração e autonomia

Retome o enunciado da POC. Concluir não é só ver uma mensagem no terminal: você precisa explicar o comportamento e sustentar sua conclusão com verificações escolhidas por você.

Leia erros identificando mensagem, arquivo e linha. Diferencie falha de sintaxe, falha durante a execução e resultado que não atende à regra que você definiu. Registre uma hipótese antes de mudar o programa e relacione a mudança à evidência observada. Durante a investigação independente do exercício 17, não use IA.

**Prática:** exercícios 16–18, encerramento da POC e [verificação final](./verificacao-final.md).

**Antes de seguir para HTTP:** cumpra os critérios do módulo. Se a dificuldade for de sintaxe ou raciocínio básico, retome o bloco correspondente.

## Roteiro de 24 sessões

Cada sessão dura até duas horas. Nas semanas 1–5, a sessão final combina uma hora de prática e uma de revisão. Na semana 6, a sessão 24 reserva uma hora para o fechamento da verificação e uma para os registros.

| Semana | Sessão | Foco | Registro esperado |
|---|---:|---|---|
| 1 | 1 | Ambiente, valores e primeira tentativa | Comando real e dúvida inicial |
| 1 | 2 | Exercícios 1–3 | Tentativas autorais |
| 1 | 3 | Continuar exercícios e variar dados | Previsões e observações |
| 1 | 4 | Consolidar tipos e revisar | Notas e diário |
| 2 | 5 | Condicionais e laços | Explicações próprias |
| 2 | 6 | Exercícios 4–6 | Tentativas autorais |
| 2 | 7 | Continuar e modificar regras | Mudança explicada |
| 2 | 8 | Revisar término dos laços | Notas e diário |
| 3 | 9 | Funções, retorno e escopo | Explicações próprias |
| 3 | 10 | Exercícios 7–9 | Tentativas autorais |
| 3 | 11 | Continuar e variar chamadas | Observações reais |
| 3 | 12 | Revisar entradas e retornos | Notas e diário |
| 4 | 13 | Arrays e objetos | Comparações próprias |
| 4 | 14 | Exercícios 10–12 | Tentativas autorais |
| 4 | 15 | Continuar e modificar dados | Comportamento explicado |
| 4 | 16 | Consolidar coleções | Notas e diário |
| 5 | 17 | JSON, módulos e callbacks | Explicações e dúvidas |
| 5 | 18 | Exercícios 13–15 | Tentativas autorais |
| 5 | 19 | Ler a POC e iniciar construção | Decisões e código próprios |
| 5 | 20 | Continuar POC e revisar | Evidências e diário |
| 6 | 21 | Revisão dos conceitos e exercício 16 | Explicação do programa |
| 6 | 22 | Exercícios 17–18 | Diagnóstico e mudança autorais |
| 6 | 23 | Concluir POC (30 min); iniciar prova (90 min) | Código e registro da tentativa |
| 6 | 24 | Encerrar prova, explicar e revisar (1h); registros (1h) | Evidências, retrospectiva e diário |

Se faltar tempo, acrescente sessões em outra semana. Não reduza a prática para caber na tabela. Os 90 minutos são uma janela inicial de trabalho, não uma prova de velocidade.

## Como pedir ajuda

Na prática assistida, apresente: atividade, o que entendeu, sua tentativa e dúvida. Peça uma pista pequena por vez. Se a dúvida for de ferramenta ou sintaxe, identifique-a claramente.

Em debugging orientado, traga suas hipóteses e evidências; a IA não entrega a causa nem aplica a correção. Nas etapas sem IA ou sem consulta, nenhuma pista ou correção é permitida durante a execução. Declare a tentativa encerrada antes da revisão posterior.
