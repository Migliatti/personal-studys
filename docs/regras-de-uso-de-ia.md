# Regras de uso de IA

Estas regras valem para módulos, exercícios, POCs e verificações. A atividade
declara `[MANUAL-CORE]`, `[AI-ASSISTED]` ou `[AI-NATIVE]`; quando não houver
marcador, vale `[MANUAL-CORE]`.

> Código que o estudante não consegue explicar, modificar e depurar não conta como aprendizado, mesmo que funcione.

Consulte o [modelo de aprendizagem](./LEARNING-MODEL.md) para escolher o modo e
o [template de atividade](../templates/atividade.md) para criar enunciados.

## Regras comuns

- A IA lê a atividade, as evidências existentes e o ponto de retomada antes de
  oferecer ajuda específica.
- O estudante continua responsável por compreender, validar e manter tudo que
  entra no repositório.
- Setup, sintaxe, flags, assinaturas de bibliotecas, mensagens genéricas de
  ferramentas, massa fictícia e formatação de texto autoral são permitidos desde
  que não resolvam o conceito avaliado.
- A IA não inventa tentativas, resultados, evidências, contribuições ou reflexões.
- Dificuldade, demora ou desânimo não autorizam interpretação psicológica. A IA
  investiga compreensão, tamanho da tarefa e condições de execução.

## `[MANUAL-CORE]`

### Antes

1. Eu registro uma hipótese ou previsão.
2. Faço uma tentativa própria antes de pedir código específico.

### Durante

A IA pode explicar um conceito com exemplo de outro contexto, fazer perguntas
orientadoras e oferecer uma pista por interação. Ela não entrega gabarito,
implementação, pseudocódigo completo, arquitetura, estratégia de testes ou
causa-raiz. Também não disfarça a solução como teste, comentário, diff ou arquivo.

### Depois

A IA revisa a tentativa, separa acertos verificáveis de lacunas e pede a próxima
alteração autoral. Eu registro erros, sugestões aceitas ou rejeitadas e demonstro
que consigo explicar ou reconstruir, modificar e depurar a solução.

## `[AI-ASSISTED]`

### Antes

Eu defino o objetivo e registro uma abordagem inicial, mesmo incompleta.

### Durante

A IA pode consultar documentação, explicar bibliotecas e APIs, oferecer pistas,
gerar testes a partir dos meus critérios e revisar código. Código específico
pode ser sugerido depois da abordagem inicial, sem substituir decisões que a
atividade exige que eu desenvolva.

### Depois

Eu explico o resultado, faço uma modificação própria, executo os testes e separo
o que foi autoral do que foi auxiliado pela IA.

## `[AI-NATIVE]`

### Antes

Eu registro problema, requisitos, critérios de aceitação e arquitetura. A IA
pode ajudar a comparar alternativas, mas as decisões finais são minhas.

### Durante

A IA pode produzir grande parte da implementação, testes e documentação. A
entrega deve incluir tratamento de erros, observabilidade e uma forma de
validação funcional. Eu reviso decisões e não aceito código que não consiga
explicar, modificar e depurar.

### Depois

Eu executo a validação, mantenho a solução e registro falhas da IA, correções
humanas, decisões importantes e evidência funcional, como demonstração,
resultado reproduzível ou usuário real.

## Restrições que prevalecem

Atividades marcadas como **sem IA** ou **sem consulta** não recebem pistas,
geração, testes ou correções durante a execução, independentemente de também
possuírem um dos três marcadores. A revisão começa somente depois que eu declaro
a avaliação encerrada.

## Registro mínimo

| Registro | `[MANUAL-CORE]` | `[AI-ASSISTED]` | `[AI-NATIVE]` |
|---|---|---|---|
| Trabalho próprio | Hipótese, tentativa e decisões | Objetivo, abordagem e partes autorais | Problema, requisitos, arquitetura e validação |
| Contribuição da IA | Conceitos, pistas e revisão | Documentação, testes, sugestões e revisão | Implementação, testes, documentação e debugging |
| Aceito ou rejeitado | Sugestão, decisão e motivo | Sugestão, decisão e motivo | Sugestão, decisão e motivo |
| Falhas e correções | Quando relevantes | Quando relevantes | Falhas da IA e correções humanas obrigatórias |
| Validação | Explicar, modificar e reconstruir ou depurar | Explicar, modificar e testar | Testar, observar, demonstrar, modificar e depurar |
| Evidência | Previsão, comando e saída real | Testes e execução real | Testes, logs e demonstração ou resultado reproduzível |

O registro pode ficar no enunciado preenchido, em `evidencias/` ou no
`retrospectiva.md` do módulo. Ele deve refletir o que realmente aconteceu, não o
que estava planejado.
