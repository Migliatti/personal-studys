# Modelo de aprendizagem AI-native

Este repositório combina duas competências que precisam crescer juntas:
compreender fundamentos de Ciência da Computação e usar agentes de IA para
construir software profissional. Cada atividade declara o tipo de aprendizagem
que está avaliando e, portanto, quanto auxílio da IA é adequado.

> Código que o estudante não consegue explicar, modificar e depurar não conta como aprendizado, mesmo que funcione.

AI-native não significa abandonar a escrita manual de código. Significa usar a
IA deliberadamente: pouca geração quando o raciocínio é o objeto de estudo e
mais geração quando o objetivo é entregar, validar e manter um sistema real.

## Os três modos

| Marcador | Melhor uso | Responsabilidade do estudante | IA permitida | Evidência mínima |
|---|---|---|---|---|
| `[MANUAL-CORE]` | Lógica, algoritmos, estruturas de dados, SQL, debugging, concorrência e fundamentos | Prever, tentar, decidir, explicar, modificar e reconstruir | Conceitos, perguntas orientadoras, pistas graduais e revisão após a tentativa | Hipótese, tentativa própria, execução real, erros, explicação e variação |
| `[AI-ASSISTED]` | Bibliotecas, padrões, APIs e técnicas novas | Definir objetivo e abordagem inicial, compreender e alterar a solução | Documentação, pistas, exemplos focados, testes e revisão de código | Separação entre autoria e auxílio, testes, explicação e modificação autoral |
| `[AI-NATIVE]` | Projetos reais, portfólio, integrações, automações e produtos | Definir problema, requisitos, arquitetura, validação e manutenção | Implementação ampla a partir de decisões registradas | Testes, observabilidade, erros tratados, documentação, prova funcional e correções humanas |

### `[MANUAL-CORE]`

Use quando escrever ou depurar o código é parte central da competência
avaliada. Antes de executar, registre uma hipótese ou previsão. Antes de pedir
geração de código, faça uma tentativa própria.

A IA pode ensinar um conceito com exemplo de outro contexto, fazer perguntas
orientadoras e oferecer uma pista por vez. A revisão completa acontece somente
depois da tentativa. Durante a revisão, registre erros encontrados e quais
sugestões foram aceitas ou rejeitadas.

A atividade só conta quando o estudante consegue explicar ou reconstruir a
solução, modificá-la e investigar um defeito relacionado. Código gerado pela IA
não substitui esse portão.

### `[AI-ASSISTED]`

Use quando o objetivo principal é aprender uma biblioteca, padrão, API ou
técnica nova sem terceirizar toda a compreensão. Antes da ajuda, registre o
objetivo e uma abordagem inicial, mesmo que incompleta.

A IA pode consultar documentação, explicar interfaces, fornecer pistas, criar
testes a partir de critérios definidos pelo estudante e revisar código. A
solução final precisa ser explicada e modificada pelo estudante. O registro deve
distinguir o que foi feito por ele do que foi sugerido ou produzido pela IA.

### `[AI-NATIVE]`

Use quando o objetivo é entregar uma solução funcional: projeto real,
portfólio, integração, automação ou experimento de produto. Depois que problema,
requisitos, critérios de aceitação e arquitetura estiverem registrados, a IA
pode produzir grande parte da implementação.

O estudante continua responsável pelas decisões, pela validação do resultado e
pela manutenção. Concluir exige testes, observabilidade, tratamento de erros,
documentação e evidência funcional, como demonstração, execução reproduzível ou
uso real. Registre falhas da IA, correções humanas e decisões importantes.

## Como escolher o modo

1. Se implementar, raciocinar ou depurar é o conceito avaliado, use
   `[MANUAL-CORE]`.
2. Se o conceito avaliado é uma ferramenta ou técnica nova, use
   `[AI-ASSISTED]`.
3. Se o objetivo principal é entregar e operar algo utilizável, use
   `[AI-NATIVE]`.
4. Se uma atividade mistura objetivos, marque cada etapa separadamente. Enquanto
   um fundamento estiver sendo avaliado, prevalece o modo mais restritivo.

O modo depende da competência avaliada, não da tecnologia nem do tamanho do
arquivo. Uma API pode conter uma etapa manual de modelagem, uma etapa assistida
de aprendizagem de framework e uma etapa AI-native de entrega.

Atividades ainda sem marcador são tratadas como `[MANUAL-CORE]` até que sejam
classificadas deliberadamente.

## Ciclo de uma atividade

1. Leia o desafio e identifique o marcador.
2. Registre a hipótese, previsão ou abordagem inicial solicitada.
3. Faça a tentativa própria ou defina requisitos e arquitetura, conforme o modo.
4. Use a IA somente dentro do nível declarado.
5. Execute testes e guarde evidências reais, inclusive falhas.
6. Explique, modifique e depure o resultado.
7. Registre contribuições da IA e sugestões aceitas ou rejeitadas.
8. Faça a reflexão posterior e uma variação apenas depois do trabalho real.

Use o [template de atividade](../templates/atividade.md) para criar novos
exercícios e projetos.

## Como registrar a IA

O registro precisa permitir distinguir capacidade própria de capacidade
ampliada pela ferramenta. Inclua:

- o que foi planejado, escrito e decidido pelo estudante;
- o que a IA pesquisou, explicou, testou, revisou ou implementou;
- sugestões aceitas e a razão da aceitação;
- sugestões rejeitadas e a razão da rejeição;
- falhas da IA e correções humanas, especialmente em `[AI-NATIVE]`;
- como o estudante validou que consegue explicar, modificar e depurar;
- comandos, saídas, testes, capturas ou demonstrações que sustentam a conclusão.

Não registre uma conversa inteira por obrigação. Registre as contribuições que
alteraram o resultado ou a compreensão. A IA não preenche reflexão pessoal, não
inventa tentativas e não declara evidências que não foram observadas.

Consulte as [regras detalhadas de uso de IA](./regras-de-uso-de-ia.md) e as
[instruções do tutor](../AGENTS.md).

## Relação com a trajetória

- **Ciência da Computação:** `[MANUAL-CORE]` desenvolve modelos mentais,
  raciocínio algorítmico, debugging e capacidade de explicar sistemas.
- **Empregabilidade:** `[AI-ASSISTED]` acelera a aprendizagem responsável de
  ferramentas reais sem esconder lacunas técnicas.
- **Produtos próprios:** `[AI-NATIVE]` treina definição de problema, arquitetura,
  entrega, validação, operação e manutenção com a alavancagem de agentes.

Os três modos formam uma progressão complementar. Fundamentos permitem julgar o
trabalho da IA; assistência acelera a aquisição de repertório; construção
AI-native transforma esse repertório em software demonstrável e útil.
