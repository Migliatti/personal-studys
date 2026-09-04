# Modelo de aprendizagem AI-native — desenho

## Objetivo

Transformar o repositório em um sistema de aprendizagem que preserve a prática
manual dos fundamentos de Ciência da Computação e, ao mesmo tempo, ensine a
usar agentes de IA para entregar software profissional. O sistema deve deixar
explícito quanto auxílio é permitido em cada atividade e quais evidências
comprovam aprendizagem.

> Código que o estudante não consegue explicar, modificar e depurar não conta
> como aprendizado, mesmo que funcione.

## Escopo

A mudança será documental e pedagógica. Não altera a ordem dos módulos, não
move exercícios, não modifica códigos autorais existentes e não adiciona
dependências.

Serão atualizados:

- `README.md`, como caminho inicial inequívoco;
- `AGENTS.md`, para a tutoria respeitar o modo declarado pela atividade;
- `docs/regras-de-uso-de-ia.md`, com permissões e registros por modo;
- `templates/modulo/README.md`, para módulos apontarem para o modelo;
- até três atividades existentes, uma por modo.

Serão criados:

- `docs/LEARNING-MODEL.md`, fonte central do modelo pedagógico;
- `templates/atividade.md`, template reutilizável para exercícios e projetos.

## Modos de aprendizagem

### `[MANUAL-CORE]`

Destinado a lógica, algoritmos, estruturas de dados, SQL, depuração,
concorrência e fundamentos de computação. Exige hipótese anterior à execução,
tentativa própria antes de geração de código, revisão posterior, registro de
erros e decisões sobre sugestões da IA, além de reconstrução ou explicação da
solução. Antes da tentativa, a IA pode ensinar conceitos em outro contexto e
oferecer perguntas orientadoras, mas não resolver a atividade.

### `[AI-ASSISTED]`

Destinado à aprendizagem de bibliotecas, padrões, APIs e técnicas novas. O
estudante registra objetivo e abordagem inicial. A IA pode consultar
documentação, esclarecer ferramentas, sugerir pistas, criar testes e revisar o
código. O estudante deve explicar e modificar o resultado e distinguir sua
contribuição da contribuição da IA.

### `[AI-NATIVE]`

Destinado a projetos reais, portfólio, integrações e automações. A IA pode
produzir grande parte da implementação, mas o estudante continua responsável
pelo problema, requisitos, arquitetura, validação e manutenção. A conclusão
exige tratamento de erros, testes, observabilidade, documentação, evidência
funcional e registro de falhas da IA, correções humanas e decisões importantes.

## Escolha do modo

O modo é definido pela competência principal que está sendo avaliada, não pela
tecnologia ou pelo tamanho da atividade. Se a implementação é o próprio objeto
de aprendizagem, usa-se `[MANUAL-CORE]`. Se o objetivo é dominar uma ferramenta
ou técnica nova preservando autoria, usa-se `[AI-ASSISTED]`. Se o objetivo é
entregar e operar uma solução real, usa-se `[AI-NATIVE]`.

Em atividades híbridas, cada etapa recebe seu próprio modo ou prevalece o modo
mais restritivo enquanto um fundamento estiver sendo avaliado. A classificação
não transforma conteúdo fundamental em prompt para geração de solução.

## Contrato das atividades

O template reutilizável terá os seguintes campos:

- título e temática;
- modo de aprendizagem;
- conceito treinado e pré-requisitos;
- desafio;
- hipótese ou previsão inicial;
- nível de IA permitido;
- entregável e critérios objetivos de conclusão;
- testes ou evidências;
- reflexão posterior;
- contribuições da IA;
- sugestões da IA aceitas ou rejeitadas;
- variação ou desafio seguinte.

Reflexões pessoais e evidências nunca serão preenchidas antecipadamente pela
IA. Os campos devem registrar fatos observados pelo estudante.

## Exemplos aplicados

### Missão 3 — telemetria recebida como texto

O enunciado em `00-logica-javascript/exercicios/README.md` será reorganizado
como `[MANUAL-CORE]`. A intenção original, a Frota Aurora e a prática de tipos e
conversão serão preservadas. O código existente não será alterado.

### POC — servidor HTTP de incidentes

O enunciado em `01-http-rest/poc/README.md` será reorganizado como
`[AI-ASSISTED]`. O estudante continuará responsável pelo contrato e pelas
decisões HTTP. A IA poderá auxiliar com consulta à documentação de `node:http`,
testes derivados do contrato registrado e revisão, sem substituir a abordagem
inicial nem a explicação e modificação finais.

### Pipeline de conciliação com n8n e TypeScript

O projeto já previsto em `13-n8n-make-com-codigo/README.md` será detalhado como
`[AI-NATIVE]`. A implementação poderá ser amplamente auxiliada por agentes, mas
os requisitos, o limite entre fluxo visual e código, a arquitetura e a
validação permanecerão sob responsabilidade do estudante. O projeto exigirá
testes, logs, tratamento de falhas, documentação e demonstração reproduzível.

## Instruções da IA

`AGENTS.md` continuará exigindo leitura da atividade e das evidências antes de
orientar o estudante. O tutor identificará primeiro o marcador do modo e
aplicará suas permissões. A regra socrática atual continuará como padrão para
`[MANUAL-CORE]`; atividades sem marcador usarão esse modo por segurança.

As proibições atuais que valem para todo o repositório serão delimitadas por
modo. Em `[AI-NATIVE]`, a IA poderá implementar decisões já definidas pelo
estudante, mas não poderá inventar requisitos, declarar evidências ou escrever
reflexões pessoais em nome dele.

## Caminho inicial no README

O README explicará a finalidade do repositório, a combinação entre fundamentos
manuais e construção AI-native, a escolha do modo, a execução de uma atividade,
o registro de IA e a relação com Ciência da Computação, empregabilidade e
produtos próprios. A chamada inicial será:

1. ler `docs/LEARNING-MODEL.md`;
2. abrir a atividade atual;
3. identificar seu marcador;
4. registrar hipótese e abordagem antes da execução;
5. executar, testar e guardar evidências;
6. preencher retrospectiva e uso de IA somente depois.

O painel de retomada e a trajetória atual permanecerão válidos.

## Verificação

Como o repositório não possui gerenciador de dependências ou suíte automatizada,
a validação será composta por:

- execução dos três arquivos `.mjs` autorais existentes;
- verificação de todos os links Markdown relativos nos arquivos modificados e
  criados;
- busca dos três marcadores e dos campos obrigatórios do template;
- revisão de `git diff --check`, `git diff` e `git status --short`;
- confirmação de que nenhum arquivo fora do escopo foi alterado.

## Fora de escopo

- conversão mecânica de todos os módulos e exercícios;
- alteração da ordem da trajetória ou dos marcos;
- criação de soluções, gabaritos ou novos códigos de exercício;
- instalação de dependências, CI ou ferramentas de validação;
- promoção ou publicação de projetos de portfólio.
