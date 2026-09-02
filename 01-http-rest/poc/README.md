# POC — servidor HTTP de incidentes

Comece na sessão 3. Uma prova de conceito é um programa pequeno para praticar o protocolo. Ela permanece neste repositório.

## Escopo já definido pelo módulo

Use `node:http`, sem framework, para construir:

- `GET /health`.
- `GET /incidents/:id`.
- `POST /incidents`.
- Pelo menos quatro situações de erro com status HTTP corretos e justificados por você.

Crie o código dentro de `poc/servidor-http/`. Registre nessa pasta as instruções reais de execução. As rotas vêm do módulo original; o contrato detalhado será seu exercício.

## Sequência de trabalho

1. Escreva o que cada rota deve fazer no [contrato](../evidencias/contrato-http.md).
2. Consulte a sintaxe mínima para abrir um servidor e receber uma requisição.
3. Implemente as duas rotas GET e observe suas próprias requisições.
4. Introduza e investigue um erro de status, registrando seu raciocínio.
5. Trabalhe na rota POST, no corpo recebido e nos erros que escolheu.
6. Compare contrato e execução, registrando divergências reais.
7. Pratique explicar e modificar o código até conseguir reconstruí-lo.

A [documentação de node:http](https://nodejs.org/api/http.html) é referência de sintaxe para `http.createServer`, `IncomingMessage`, `ServerResponse` e `server.listen`. Essa API é de baixo nível: receber uma mensagem não significa que o Node interpretou seu JSON ou escolheu suas rotas. Consulte também os eventos de leitura do corpo.

## Prova de encerramento

Critério original: **em 40 minutos e sem consulta, criar as três rotas acima, retornando pelo menos quatro erros HTTP corretos**.

Faça a tentativa numa pasta nova dentro de `poc/servidor-http/`, preservando o trabalho anterior. Durante a prova, feche código anterior, notas, documentação e ajuda de IA. Registre duração, resultado, código produzido e evidências reais. Se não atingir o critério, anote as lacunas e repita após estudar.

A conclusão também exige explicar decisões, modificar o comportamento, diagnosticar um defeito e preencher a [retrospectiva](../retrospectiva.md).
