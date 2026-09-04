# Registro de execuções

Copie esta ficha para cada atividade ou execução relevante. Não confunda preparação do módulo com execução dos exercícios.

## Missão 1 — apresentação na ponte de comando

- Atividade: missão 1.
- Data e tempo real: 03/09/2026; tempo não informado.
- Arquivo/versão: `exercicios/pratica/missao-1.mjs`; arquivo de trabalho sem versão de commit informada.
- Regra ou objetivo definido por mim: motivo das escolhas não informado pelo estudante.
- Dados escolhidos e motivo: `pessoa` recebeu `"Ana"` na variação e `aprendizado` permaneceu `"Biologia"`; motivo não informado.
- Minha previsão antes de executar: ao alterar `pessoa`, as duas mensagens usariam o novo nome.
- Comando e diretório: `node .\00-logica-javascript\exercicios\pratica\missao-1.mjs`, executado a partir da raiz do repositório durante a revisão com IA.
- Saída observada: `Acaba de chegar: Ana` e `O(a) Ana quer aprender: Biologia`.
- O que essa evidência demonstra: a execução observada usou o valor de `pessoa` nas duas mensagens e preservou o valor de `aprendizado`.
- Limite da verificação: foi observada somente a variação com `Ana` e `Biologia` nesta execução final.
- Alteração realizada, se houver: `pessoa` foi alterada de `"Gustavo"` para `"Ana"`.
- Resultado depois da alteração: `Ana` apareceu nas duas mensagens.
- Ajuda utilizada durante a prática, se houver: revisão com IA, com perguntas sobre a relação entre variáveis e saída e solicitação de variação autoral.

## Missão 2 — tempo de manutenção do mecha

- Atividade: missão 2.
- Data e tempo real: 03/09/2026; tempo não informado.
- Arquivo/versão: `exercicios/pratica/missao-2.mjs`; arquivo de trabalho sem versão de commit informada.
- Regra ou objetivo definido por mim: motivo da escolha não informado pelo estudante.
- Dados escolhidos e motivo: `7.75` horas, descritas pelo estudante como 7h45min; motivo não informado.
- Minha previsão antes de executar: não foi registrada antes da execução da variação.
- Comando e diretório: `node .\00-logica-javascript\exercicios\pratica\missao-2.mjs`, executado a partir da raiz do repositório durante a revisão com IA.
- Saída observada: `Calculando minutos para o conserto...` e `A máquina demorará cerca de 465 minutos para ser consertada`.
- O que essa evidência demonstra: para a entrada observada, a operação `horas * 60` produziu `465`, apresentado com a unidade minutos.
- Limite da verificação: esta execução final verificou somente a entrada `7.75` horas; não existe previsão anterior registrada para essa variação.
- Alteração realizada, se houver: a entrada passou de `1.5` para `7.75`; a unidade foi adicionada à saída; os textos e o nome `tempo_conserto` foram corrigidos durante a revisão.
- Resultado depois da alteração: a execução apresentou `465 minutos` e terminou com código de saída `0`.
- Ajuda utilizada durante a prática, se houver: revisão com IA sobre unidade, escrita das mensagens, nome da variável e tipo `number`; as alterações foram realizadas pelo estudante.

## Missão 3 — telemetria recebida como texto

- Atividade: missão 3.
- Data e tempo real: 03/09/2026; tempo não informado.
- Arquivo/versão: `exercicios/pratica/missao-3.mjs`; arquivo de trabalho sem versão de commit informada.
- Regra ou objetivo definido por mim: motivo das escolhas não informado pelo estudante.
- Dados escolhidos e motivo: texto numérico `"192"` na primeira comparação, texto `"teste"` para a conversão inválida e texto numérico `"80"` na variação; motivos não informados.
- Minha previsão antes de executar: para `8 + "192"`, concatenação em `8192`; para `8 + 192`, soma em `200`; para `Number("teste")`, `NaN`. Na variação, a previsão inicial da concatenação foi `808` e foi corrigida para `880` antes da execução; a soma prevista foi `88`.
- Comando e diretório: `node .\00-logica-javascript\exercicios\pratica\missao-3.mjs`, executado a partir da raiz do repositório durante a revisão com IA.
- Saída observada: na primeira comparação, `8192` e `200`; na conversão inválida, `NaN` com `typeof` igual a `number`; na execução final da variação, `880` e `88`.
- O que essa evidência demonstra: com o operador `+`, o texto participou de concatenação e o valor convertido participou de soma; `Number("teste")` não produziu número válido.
- Limite da verificação: a execução final contém `"80"` e `"teste"`; os resultados de `"192"` pertencem a uma execução anterior observada durante a revisão.
- Alteração realizada, se houver: a entrada textual válida passou de `"192"` para `"80"`; os casos válido e inválido foram preservados juntos; a concordância de “espécimes diferentes” foi corrigida.
- Resultado depois da alteração: a execução final apresentou `NaN`, os tipos `number`, `string` e `number`, os resultados `880` e `88`, e terminou com código de saída `0`.
- Ajuda utilizada durante a prática, se houver: revisão com IA sobre tipos, conversão com `Number`, `NaN`, concatenação, soma, preservação dos dois casos e concordância textual; as alterações foram realizadas pelo estudante.
