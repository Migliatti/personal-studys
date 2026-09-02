# Exercícios — HTTP e REST

Siga o [guia](../guia-de-estudo.md). Registre respostas em [notas.md](../notas.md) e resultados da API no [contrato](../evidencias/contrato-http.md). Os desafios abaixo devem produzir suas próprias explicações.

## 1. URL e mensagem

Escolha uma requisição da primeira sessão. Separe esquema, host, caminho e query. Altere somente um parâmetro e preveja o resultado antes de executar. Compare as respostas.

Entrega: duas requisições anotadas e sua explicação da diferença entre query, cabeçalho e corpo.

## 2. Navegador como cliente

Abra [httpbin/get](https://httpbin.org/get) no navegador. Abra as ferramentas de desenvolvedor, selecione **Network/Rede** e recarregue a página. Selecione a requisição de `/get` e observe URL, método, status, cabeçalhos de envio, cabeçalhos de retorno e resposta.

Compare com curl. Quais cabeçalhos mudaram? Diferencie o que o cliente enviou do que o servidor devolveu. Se houver outras requisições, explique por que escolheu a de `/get`.

Entrega: comparação textual ou captura anotada sem dados pessoais.

## 3. Método, intenção e repetição

Crie um exemplo fictício para cada método estudado. Descreva a intenção e o efeito de repetir a mesma requisição. Justifique com a documentação. Compare “resposta igual” e “efeito pretendido igual”.

Entrega: tabela autoral de método, intenção, repetição e justificativa. Não use o serviço de eco para concluir que uma operação é idempotente: ele não implementa o domínio da sua API.

## 4. Seu contrato de incidentes

Leia o [enunciado da POC](../poc/README.md). Antes de implementar cada comportamento, registre suas decisões: entrada, resposta de sucesso, cabeçalhos e erros. Selecione e justifique pelo menos quatro situações de erro com os respectivos status.

Entrega: decisões do contrato preenchidas por você. Essa tabela é uma previsão; resultados observados entram depois, separadamente.

## 5. Evolução do contrato

Imagine que sua API precisará listar muitos incidentes. Esboce como comunicaria filtros e paginação. Imagine também uma mudança incompatível na resposta: como o consumidor saberia qual contrato usa?

Compare uma interface organizada por recursos com outra organizada por operações. Justifique suas propostas. Esta atividade é no papel, sem ampliar a implementação obrigatória.

Entrega: três exemplos de requisição propostos por você e uma explicação dos limites das escolhas.

## 6. Explicação e diagnóstico próprios

Explique o caminho entre digitar uma URL HTTPS e receber uma resposta, no cenário HTTP/1.1 estudado. Diferencie falta de resposta HTTP de resposta HTTP de erro.

Retome o defeito de status introduzido na semana 1. Registre sintoma, hipóteses, investigação, causa identificada e correção. Se precisar praticar mais, introduza outro defeito numa cópia de exercício e investigue sozinho.

Entrega: explicação sem consulta e registro factual do diagnóstico. A estratégia de verificação e a causa-raiz devem ser suas.
