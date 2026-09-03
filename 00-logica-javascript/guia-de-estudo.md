# Guia de estudo — Lógica e JavaScript

**Preparação sob demanda:** somente a semana 1 é o roteiro ativo. Os blocos posteriores são referência preliminar preservada, não agenda obrigatória. Antes de preparar a próxima semana, o tutor deve revisar suas tentativas, evidências, dificuldades e ponto de parada e detalhar somente essa semana, com lore da Frota Aurora e sem soluções prontas.

O objetivo é voltar a escrever programas pequenos e ganhar familiaridade com JavaScript. Não precisa lembrar toda a sintaxe de Python nem estudar duas linguagens em paralelo.

## Como usar o material

Leia o conceito da missão atual, pratique uma atividade por vez e registre o que aconteceu. Os enunciados não são roteiros de implementação: você escolhe dados, organização e verificações. Antes de executar, anote sua previsão; depois compare com a saída real. Tentativa incompleta registrada ajuda a escolher a retomada.

Na prática assistida, documentação e ajuda pontual são permitidas. Nas etapas sem IA ou sem consulta, encerre a tentativa antes de pedir revisão. Não preencha notas, evidências ou diário como se as sessões abaixo já tivessem ocorrido.

## Marco A — três semanas estimadas

A carga-base é de 8 horas semanais, em quatro sessões de até duas horas. Até 7 horas adicionais são margem opcional de recuperação ou repetição, sem conteúdo obrigatório novo. As três semanas somam 24 horas estimadas; lacunas deslocam o calendário.

O **núcleo essencial** é composto pelas missões **1, 3, 4, 6, 7, 12, 13, 14 e 15**. As missões **2, 5, 8–11 e 16–18** são **reforço recomendado**, disponível conforme a necessidade e obrigatório apenas na conclusão integral posterior do módulo. Não tente concluir as 18 missões no prazo do Marco A.

| Semana | Foco | Retomada orientada por evidências |
|---|---|---|
| Semana 1 | Sessões 1–4 abaixo; missões 1 e 3; missão 2 como reforço conforme o ritmo | Valores, operações e conversão explicados; variação e registros reais |
| Semana 2 | Decisões, repetições, funções e coleções; missões 4, 6, 7 e 12 | Regras, término, retorno e representação explicados e modificados |
| Semana 3 | JSON, módulos e callback; missões 13–15, POC e portão | Integração, explicação, modificação e investigação independentes |

Na semana 2, distribua leitura e tentativas pelas quatro sessões, reservando tempo para revisão e registros. Na semana 3, leia a POC após as missões 13–15 e use sessões adicionais se a construção e o portão não couberem. O [portão do Marco A](./README.md#portão-do-marco-a--antes-de-http) é a condição de avanço para HTTP, não a passagem de três semanas.

## Semana 1 — valores, variáveis e operações

A primeira semana tem quatro sessões completas abaixo. Na Frota Aurora, você começa preparando o terminal de bordo e pequenas experiências de telemetria. As missões não exigem conhecimento de franquias ou ficção científica.

### Conceitos de apoio

Um algoritmo descreve como transformar uma entrada em uma saída. Escrever o programa exige tornar explícitas as operações que na explicação verbal podem ficar implícitas.

Em JavaScript, `let` declara uma variável que pode receber outro valor; `const` impede reatribuir aquela variável. Strings representam texto, numbers representam números e booleans representam verdadeiro ou falso. `typeof` permite observar o tipo de um valor. Você também encontrará `undefined` e `null`; registre como aparecem na sua prática.

Exemplo isolado, de outro contexto e sem resolver as missões:

```javascript
const idioma = "português";
let paginaAtual = 4;
```

Estude operadores aritméticos, precedência, parênteses e conversão explícita com `Number`. Texto contendo dígitos continua sendo texto até uma conversão. Não suponha que todos os operadores tratam texto da mesma maneira. Aprenda concatenação e template literals para compor mensagens.

**Leitura:** tópicos indicados de “Sintaxe e tipos”, “Expressões e operadores” e “Formatação de texto” no [guia MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide). Hoisting e detalhes avançados podem esperar. Entradas podem ser valores escritos no arquivo; teclado não é pré-requisito.

## Sessão 1 — ambiente e primeiro arquivo (duas horas)

**Objetivo:** conferir o ambiente, executar o arquivo de preparação existente e começar a missão 1, sem exigir sua conclusão.

**Preparação:** abra o repositório no editor e confira Node e Git no PowerShell:

```powershell
Set-Location -LiteralPath 'C:\Users\Gabriel Speedpro\Music\projetos\personal-studys\00-logica-javascript'
node --version
git --version
git status --short
```

Na preparação de 02/09/2026 foi registrado Node `v24.20.0`; isso não substitui a versão observada na sua sessão. Se um comando não for reconhecido, peça ajuda de setup. Não instale pacotes npm para este módulo. Confira alterações existentes antes de trabalhar; não as descarte.

**Conceito técnico:** JavaScript é a linguagem; Node.js executa arquivos fora do navegador; PowerShell recebe o comando que inicia o programa. Código JavaScript escrito no PowerShell não se torna automaticamente JavaScript executado. Git registra versões; consultar o estado não cria um commit.

**Missão:** a Frota Aurora abre um terminal para receber uma pessoa em treinamento. Execute o arquivo de preparação já existente, sem recriá-lo ou substituí-lo, e depois leia a missão 1 em [exercicios/README.md](./exercicios/README.md).

```powershell
node ./exercicios/pratica/primeiro-programa.mjs
```

A extensão `.mjs` identifica um módulo JavaScript no Node. A execução acima é só setup; não resolve a missão 1. Leia valores e variáveis no bloco de apoio e inicie a missão em outro arquivo autoral na pasta de prática. Sugestão de tempo: 20 minutos para ambiente, 20 para execução, 30 para conceitos, 35 para tentativa e 15 para registro.

**Entrega:** tentativa autoral da missão 1, mesmo incompleta, e registro das versões, comando, diretório, saída real e ponto de parada em [notas.md](./notas.md).

**Evidência de compreensão:** explique a diferença entre editar, salvar e executar, e identifique o papel dos valores e variáveis que usou. Setup sozinho não comprova domínio de JavaScript.

**Próximo passo:** anote a primeira ação concreta para retomar a missão 1 na sessão 2.

## Sessão 2 — operações e conversões (duas horas)

**Objetivo:** trabalhar operações e conversão explícita sem supor que texto e número se comportam da mesma forma.

**Preparação:** releia sua tentativa e ponto de parada; revise apenas operadores e conversão nos conceitos de apoio.

**Conceito técnico:** tipos, operações, precedência e conversão; diferença entre prever um comportamento e observar uma execução.

**Missão:** a equipe de telemetria da Frota Aurora recebeu quantidades como texto e precisa entender seu uso no programa. Retome a missão 1 e avance para a missão 3; a missão 2 oferece reforço de operações conforme o ritmo, mas não é bloqueio obrigatório. Trabalhe em uma missão por vez.

**Entrega:** tentativa da missão em que conseguiu trabalhar, previsão anterior à execução, comando e saída real em [execucoes.md](./evidencias/execucoes.md). Não registre as missões 2 ou 3 como realizadas se não chegou a elas.

**Evidência de compreensão:** explique os tipos envolvidos e compare sua previsão com o que de fato ocorreu, incluindo dúvidas sobre conversão inválida quando chegar a essa parte da missão 3.

**Próximo passo:** escolha na própria tentativa o dado ou a regra pequena que pretende variar na sessão 3; se ainda houver bloqueio, registre-o antes de avançar.

## Sessão 3 — variação e explicação (duas horas)

**Objetivo:** demonstrar compreensão além da primeira execução, com uma pequena alteração autoral.

**Preparação:** abra a tentativa e as previsões registradas nas sessões anteriores. Preserve a versão anterior para poder comparar.

**Conceito técnico:** entrada, processamento, saída e tipos; relação entre mudança no programa e mudança observada.

**Missão:** o painel da Frota Aurora recebe uma atualização de treinamento. Escolha uma pequena variação de dados ou regra na missão 1 ou 3 em que já trabalhou, registre sua previsão e execute novamente. A escolha da variação e das verificações é sua.

**Entrega:** registro do que mudou, da previsão e da execução posterior, ligado ao arquivo da tentativa.

**Evidência de compreensão:** explique com suas palavras o caminho dos dados, os tipos e o efeito da alteração; indique uma lacuna se não conseguir justificar o observado.

**Próximo passo:** leve essa lacuna e os registros reais para a revisão da sessão 4, sem substituir a explicação por texto gerado.

## Sessão 4 — consolidação e Git (duas horas)

**Objetivo:** revisar lacunas, reunir evidências e registrar uma versão coerente da prática realizada.

**Preparação:** leia notas, tentativas e evidências da semana; confira `git status --short` e `git diff` a partir do repositório.

**Conceito técnico:** diferença entre arquivo de trabalho, alteração selecionada para commit e histórico; evidência é o que foi observado, não o plano da semana.

**Missão:** a Frota Aurora fecha o diário do turno e precisa conseguir retomar o trabalho. Revise uma lacuna por vez, organize os registros e produza um commit coerente apenas com o que você realizou e revisou. Escolha os arquivos e a mensagem; ajuda mecânica com Git é permitida, sem descarte de alterações existentes.

**Entrega:** referências às execuções e à variação, commit do trabalho revisado e linha factual no [diário de estudo](../docs/diario-de-estudo.md), com horas reais e próximo passo.

**Evidência de compreensão:** explique o que entrou no commit e por quê, e quais conceitos a semana demonstrou ou deixou pendentes. Não conclua o Marco A apenas por completar quatro sessões.

**Próximo passo:** se valores e conversão ainda não estiverem claros, acrescente uma sessão de retomada; caso contrário, inicie a missão 4 com o bloco de decisões abaixo.

## Conceitos para a semana 2 — decisões e repetições

Uma condição produz um valor booleano; `if` e `else` permitem escolher um caminho. Estude comparações, igualdade estrita (`===`), diferença (`!==`), `&&`, `||` e `!`. A atribuição `=` tem outra finalidade. Chaves delimitam blocos; indentação ajuda a leitura.

Repetir exige entender quando continuar e quando terminar. Estude `for` e `while` e explique por que sua repetição termina antes de executar. `Ctrl+C` interrompe um programa que não termina no terminal.

**Leitura:** “Controle de fluxo” e “Laços e iteração” do [guia MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide).

**Missões essenciais:** 4 e 6. **Reforço:** 5. Não é necessário usar arrays nessas missões. Antes de seguir, explique a regra e a alteração de estado durante a repetição.

## Conceitos para a semana 2 — funções e escopo

Uma função agrupa um comportamento que pode receber argumentos e retornar um valor. Parâmetros são os nomes na definição; argumentos são os valores fornecidos na chamada. `return` devolve um resultado para quem chamou; exibir com `console.log` tem outro papel.

Estude `function`, chamada, retorno e escopo de bloco/função. Observe quais variáveis cada trecho pode acessar. Depois reconheça arrow functions (`=>`), sem precisar reescrever tudo. Closures avançadas e recursão não são exigidas.

**Leitura:** “Funções” do [guia MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide).

**Missão essencial:** 7, que contém seu próprio pedido de conversão de duração. **Reforço:** 8 e 9. Você decide nomes, parâmetros e divisão. Antes de seguir, explique entrada, retorno e momento da chamada.

## Conceitos para a semana 2 — arrays e objetos

Arrays guardam sequências de valores, com posições iniciando em zero. Objetos relacionam propriedades a valores. Compare uma informação isolada e várias relacionadas, sem supor uma representação universal.

Estude índice, `length`, `push`, `for...of`, leitura e alteração de propriedades. Um array pode conter objetos. Duas variáveis podem apontar para o mesmo objeto; alterar esse objeto não é reatribuir uma variável declarada com `const`.

**Leitura:** “Coleções indexadas” e “Trabalhando com objetos” do [guia MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide).

**Missão essencial:** 12. **Reforço:** 10 e 11, caso precise separar coleção e objeto em práticas menores. `map` e `filter` são aprofundamento opcional. Antes de seguir, explique percurso, acesso a propriedades e suas escolhas de representação.

## Conceitos para a semana 3 — JSON, módulos e callbacks

JSON é representação textual de dados, não um objeto JavaScript em memória. Estude `JSON.stringify` e `JSON.parse`, observando os tipos antes e depois. Nem todo valor JavaScript tem representação em JSON.

Módulos permitem exportar e importar valores e funções. Use `.mjs`, caminhos relativos e extensão explícita em arquivos locais. A divisão entre arquivos é sua decisão.

Uma função também é um valor e pode ser passada como argumento. Uma função recebida para ser chamada é frequentemente chamada de callback; isso não significa, por si só, execução assíncrona. Compare entregar uma função e chamá-la imediatamente.

Faça contato com `setTimeout` para observar uma chamada agendada. O atraso solicitado não garante instante exato de execução. Não precisa implementar HTTP, promises ou `async/await`.

**Leitura:** “Funções” do [guia MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide), [módulos](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Modules), [JSON](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/JSON) e [timers do Node](https://nodejs.org/api/timers.html).

**Missões essenciais:** 13–15. Depois inicie a [POC](./poc/README.md). Callback é praticado na missão 15, não exigência artificial da POC. Antes do portão, execute importações e explique função, chamada, callback e conversão JSON.

## Integração, investigação e conclusão posterior

Retome a POC e sustente seu funcionamento com verificações escolhidas por você. Leia erros identificando mensagem, arquivo e linha; diferencie falha de sintaxe, falha de execução e resultado contrário à regra. Registre hipóteses antes de modificar e relacione mudanças às evidências.

Para seguir a HTTP, cumpra o [portão do Marco A](./README.md#portão-do-marco-a--antes-de-http), usando tentativas essenciais e POC para explicação, mudança e investigação; as etapas sem IA não recebem pistas durante a execução. O portão não exige concluir o reforço nem a avaliação integral.

Para concluir integralmente o módulo depois, retome as missões de reforço pendentes, incluindo 16–18, e a [verificação final](./verificacao-final.md). A missão 17 é sem IA; a verificação final é sem IA e sem consulta. Reserve sessões próprias e registre o tempo real, sem comprimir esse trabalho nas três semanas estimadas do núcleo.

## Como pedir ajuda

Na prática assistida, apresente atividade, entendimento, tentativa, evidência, ponto de parada e dúvida. Peça uma pista pequena por vez. Dúvidas gerais de conceito, ferramenta e sintaxe podem receber explicação direta de outro contexto.

Em debugging orientado, traga hipóteses e evidências: a IA não entrega a causa nem aplica a correção. Nas etapas sem IA ou sem consulta, nenhuma pista ou correção durante a execução. Declare a tentativa encerrada antes da revisão posterior.
