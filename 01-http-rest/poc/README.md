# [AI-ASSISTED] POC — servidor HTTP de incidentes

Comece na sessão 3. Uma prova de conceito é um programa pequeno para praticar o protocolo. Ela permanece neste repositório.

**Temática:** central de incidentes da Frota Aurora.
**Modo de aprendizagem:** `[AI-ASSISTED]`, porque a prática combina decisões
próprias de HTTP com a aprendizagem da API de baixo nível `node:http`.
**Conceito treinado:** contrato HTTP, métodos, rotas, status, cabeçalhos, corpo,
erros e implementação de servidor sem framework.
**Pré-requisitos:** módulo 00 concluído, sessões 1 e 2 do módulo 01 e decisões
iniciais registradas no [contrato](../evidencias/contrato-http.md).

## Desafio

Construa um servidor HTTP de incidentes e compare continuamente o contrato
previsto com as respostas observadas. Uma prova de conceito é um programa
pequeno para praticar o protocolo; ela permanece neste repositório.

### Escopo já definido pelo módulo

Use `node:http`, sem framework, para construir:

- `GET /health`.
- `GET /incidents/:id`.
- `POST /incidents`.
- Pelo menos quatro situações de erro com status HTTP corretos e justificados por você.

Crie o código dentro de `poc/servidor-http/`. Registre nessa pasta as instruções reais de execução. As rotas vêm do módulo original; o contrato detalhado será seu exercício.

## Hipótese ou previsão inicial

Antes de gerar ou implementar código, registre o objetivo e uma abordagem
inicial: como pretende reconhecer cada rota, receber o corpo, representar os
dados e transformar cada situação prevista em uma resposta HTTP. Registre no
contrato entrada, sucesso, cabeçalhos e pelo menos quatro erros justificados.

## Nível de IA permitido

A IA pode consultar documentação, explicar assinaturas de `node:http`, oferecer
pistas, mostrar exemplos focados de outro contexto, gerar testes a partir do
contrato que você definiu e revisar sua tentativa.

Antes de sugerir código específico, ela deve esperar seu objetivo e abordagem
inicial. Você continua responsável pelo contrato, pelas decisões HTTP e pelos
critérios de teste. A versão final precisa ser explicada e modificada por você.

## Entregável

- Código autoral e assistido em `poc/servidor-http/`.
- Contrato previsto e resultados observados registrados separadamente.
- Instruções reais de execução e requisições reproduzíveis.
- Registro das partes próprias e das partes auxiliadas pela IA.

## Sequência de trabalho

1. Escreva o que cada rota deve fazer no [contrato](../evidencias/contrato-http.md).
2. Consulte a sintaxe mínima para abrir um servidor e receber uma requisição.
3. Implemente as duas rotas GET e observe suas próprias requisições.
4. Introduza e investigue um erro de status, registrando seu raciocínio.
5. Trabalhe na rota POST, no corpo recebido e nos erros que escolheu.
6. Compare contrato e execução, registrando divergências reais.
7. Pratique explicar e modificar o código até conseguir reconstruí-lo.

A [documentação de node:http](https://nodejs.org/api/http.html) é referência de sintaxe para `http.createServer`, `IncomingMessage`, `ServerResponse` e `server.listen`. Essa API é de baixo nível: receber uma mensagem não significa que o Node interpretou seu JSON ou escolheu suas rotas. Consulte também os eventos de leitura do corpo.

## Critérios objetivos de conclusão

- [ ] As três rotas respondem de acordo com o contrato registrado.
- [ ] Pelo menos quatro situações de erro possuem status justificados e
  evidências de execução.
- [ ] Os testes ou requisições reproduzíveis cobrem sucesso e erro.
- [ ] Consigo explicar o fluxo da requisição até a resposta.
- [ ] Fiz uma modificação própria e demonstrei seu efeito.
- [ ] Diferenciei o que escrevi e decidi do que foi auxiliado pela IA.
- [ ] Concluí a prova de encerramento nas condições declaradas abaixo.

## Testes ou evidências

Registre comandos de inicialização, requisições, status, cabeçalhos, corpos e
saídas reais no [contrato](../evidencias/contrato-http.md) ou na pasta da POC.
Testes sugeridos pela IA devem derivar de critérios que você registrou e precisam
ser executados; texto de teste sem resultado não é evidência.

### Prova de encerramento — sem IA e sem consulta

Critério original: **em 40 minutos e sem consulta, criar as três rotas acima, retornando pelo menos quatro erros HTTP corretos**.

Faça a tentativa numa pasta nova dentro de `poc/servidor-http/`, preservando o trabalho anterior. Durante a prova, feche código anterior, notas, documentação e ajuda de IA. Registre duração, resultado, código produzido e evidências reais. Se não atingir o critério, anote as lacunas e repita após estudar.

A conclusão também exige explicar decisões, modificar o comportamento, diagnosticar um defeito e preencher a [retrospectiva](../retrospectiva.md).

## Reflexão posterior

Depois da execução, explique quais decisões pertencem ao protocolo HTTP, quais
pertencem à API `node:http` e onde sua abordagem inicial mudou. Não antecipe a
reflexão antes da experiência real.

## Contribuições da IA

Separe consultas de documentação, explicações, testes gerados, trechos sugeridos
e revisão das decisões e implementações feitas por você.

## Sugestões da IA aceitas ou rejeitadas

Registre sugestões relevantes, sua decisão e o motivo. Inclua correções feitas
quando a saída gerada não correspondia ao contrato.

## Variação ou desafio seguinte

Depois da conclusão, escolha uma pequena alteração de contrato, preveja quais
requisições e testes serão afetados, implemente-a e compare a previsão com as
respostas observadas.
