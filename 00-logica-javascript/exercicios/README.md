# Exercícios — Lógica e JavaScript

Leia primeiro o [README do módulo](../README.md) e o bloco correspondente do [guia](../guia-de-estudo.md). Faça as atividades na ordem, uma por vez.

Crie seus arquivos `.mjs` em [pratica/](./pratica/). Escolha nomes que identifiquem cada exercício. Você pode consultar documentação e pedir uma pista durante a prática, exceto na atividade 17. Não copie implementações prontas.

Use dados fictícios definidos nos arquivos. Você escolhe os valores, as formas de verificar e os resultados esperados antes de executar. Registre tentativas, comandos reais e conclusões nas [evidências](../evidencias/README.md). As perguntas abaixo não têm respostas preenchidas.

## Semana 1 — valores e operações

### 1. Uma apresentação no terminal

Escreva um programa que mostre um apelido fictício e algo que esse personagem quer aprender. Use variáveis para os dados. Altere um dado e explique o que mudou na execução.

### 2. Duração de uma atividade

Uma oficina informa sua duração em horas e precisa apresentá-la em minutos. Escreva um programa que faça essa transformação para um valor escolhido por você. Explique a relação entre entrada, operação e saída.

### 3. Número recebido como texto

Um arquivo de origem representa uma quantidade numérica como texto. Escreva uma experiência que compare usar esse texto em uma operação e usar sua conversão explícita para número. Registre sua previsão antes da execução e explique a diferença observada, se houver. Investigue também o que ocorre quando a conversão não produz um número válido.

## Semana 2 — condições e repetições

### 4. Decisão por uma regra

Uma competição de jogo concede um selo quando a pontuação alcança um limite. Escolha e documente o limite. Escreva um programa que informe a situação de uma pontuação segundo essa regra. Você decide como verificar que a regra foi representada corretamente.

### 5. Duas condições relacionadas

Uma atividade de um clube só pode acontecer quando há um responsável presente e a sala está disponível. Represente essa decisão e explique como relacionou as duas condições.

### 6. Repetição com término

Um painel precisa exibir uma sequência de números entre um início e um fim escolhidos por você. Defina se os extremos participam da sequência. Escreva o programa e explique por que sua repetição termina.

## Semana 3 — funções

### 7. Um comportamento reutilizável

Retome a transformação de duração do exercício 2 e permita reutilizá-la por meio de uma função. Decida sua interface. Explique a diferença entre o resultado retornado e a mensagem exibida.

### 8. Entradas independentes

Crie uma função que construa uma mensagem a partir de informações recebidas. Escolha um contexto diferente do exercício 1. Demonstre chamadas com dados distintos e explique quais valores pertencem a cada chamada.

### 9. Quem pode acessar a variável?

Crie uma pequena experiência autoral para investigar o acesso a variáveis dentro e fora de funções ou blocos. Registre sua previsão, execute e explique o que observou. Uma falha durante essa experiência é material para investigação, não uma resposta a ser escondida.

## Semana 4 — arrays e objetos

### 10. Uma coleção de palavras

Represente uma coleção de palavras escolhidas por você e produza uma apresentação de todos os itens no terminal. Depois altere a coleção e explique o efeito. Você decide os dados e a forma de verificar o percurso.

### 11. Informações relacionadas

Represente em um objeto as informações de um objeto cotidiano fictício. Escolha quais propriedades fazem sentido. Leia e altere uma propriedade, explicando a diferença entre a propriedade, seu nome e seu valor.

### 12. Consultar vários registros

Escolha um conjunto de itens fictícios, represente suas informações e apresente apenas aqueles que atendem a um critério definido por você. Explique sua representação e a regra aplicada. Não há modelo de dados ou algoritmo fornecido.

## Semana 5 — ponte para Node.js

### 13. Dados e representação textual

Escolha dados simples que possam ser representados em JSON. Escreva uma experiência de conversão para texto e de leitura desse texto. Compare tipos e acesso às informações antes e depois. Explique por que o texto não é o próprio objeto em memória.

### 14. Usar outro arquivo

Escolha um comportamento que você escreveu e utilize-o a partir de outro arquivo por meio de exportação e importação. Decida a divisão entre os arquivos e registre o comando de execução. Use `.mjs` e caminhos locais com extensão.

### 15. Função, chamada e callback

Crie uma experiência pequena que permita comparar passar uma função para outra operação e chamar a função imediatamente. Depois use um agendamento com `setTimeout` e registre sua previsão da ordem das mensagens antes de executar. Explique o que observou. Não é necessário criar uma API nem usar promises.

## Semana 6 — integrar e revisar

### 16. Explicar a POC

Com a sua POC aberta, explique o caminho dos dados e o papel dos trechos que escreveu. Registre onde sua explicação ficou imprecisa. Durante esta atividade, a IA pode fazer uma pergunta por vez sobre sua tentativa, sem escrever a explicação por você.

### 17. Investigar um defeito — sem IA

Em uma cópia de um programa seu já verificado, introduza uma alteração pequena que cause um comportamento incorreto. Anote a alteração separadamente e faça a investigação sem reler essa anotação. Esse diagnóstico de um defeito introduzido por você é uma prática limitada; não comprova diagnóstico de um defeito desconhecido.

Sem IA durante toda a execução: registre o sintoma, suas hipóteses, evidências, alteração e observação posterior. Consulta à documentação da linguagem é permitida; soluções prontas não. Você escolhe como verificar a correção. Preserve a versão funcional original e não deixe a versão com defeito na `main`.

Declare a atividade encerrada antes de solicitar revisão. A IA não escolhe o defeito, sua causa ou a correção.

### 18. Fazer uma mudança própria

Escolha e descreva uma pequena mudança no comportamento da POC. Implemente por conta própria, com consulta à documentação permitida, e registre como verificou o resultado. A escolha da mudança e das verificações é sua; não peça que a IA as determine.

## Encerramento

As atividades 16–18 não substituem a [verificação final](../verificacao-final.md). Complete os registros reais e retome os conceitos que ainda não consegue explicar.
