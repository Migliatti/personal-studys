# POC — Painel de leituras de bordo

## Conceito técnico e objetivo

Integrar funções, condições, arrays, objetos e módulos em um programa JavaScript pequeno que organize leituras fictícias e produza um resumo no terminal.

**Lore:** a tripulação da Frota Aurora mantém uma biblioteca de leituras para os intervalos das expedições, incluindo histórias ilustradas e materiais de bordo. Um painel no terminal ajudará a acompanhar essa coleção sem depender de conexão com a central.

Comece após as missões essenciais 13–15, na semana 3 estimada do Marco A, ampliando o tempo quando necessário. A POC integra o portão essencial; a avaliação final e as missões de reforço pertencem à conclusão integral posterior. O nome temático não altera o caminho existente `organizador-leituras/`.

## Comportamento — necessidades da tripulação

Uma pessoa quer manter informações sobre leituras, distinguir as concluídas das que ainda pretende fazer, consultar uma parte da coleção e visualizar um resumo numérico.

O programa deve permitir demonstrar:

- Inclusão de uma leitura na coleção.
- Apresentação das leituras registradas.
- Mudança da situação de uma leitura.
- Consulta segundo um critério explicado por você.
- Resumo numérico coerente com os dados usados.

Você define quais informações representar, quais situações existem, como identificar uma leitura e qual resumo será útil. Documente suas decisões antes de apresentar o resultado.

## Escopo e restrições

Use JavaScript executado pelo Node.js, sem dependências externas. Os dados são fictícios e podem estar definidos no código; a demonstração pode ocorrer por chamadas escritas por você, sem menu interativo ou entrada pelo teclado.

Não é necessário salvar dados entre execuções, acessar rede, criar servidor, banco de dados ou interface web. O comportamento para entradas fora do que você decidiu aceitar deve ser documentado por você; não é necessário construir um sistema completo de validação nesta etapa.

Pratique funções, condicionais, coleções, objetos e uso de módulos onde fizer sentido. Você escolhe arquivos, responsabilidades e interfaces. Não há arquitetura, modelo de domínio, pseudocódigo ou testes fornecidos. Callback é praticado na missão 15, não exigência artificial da POC.

## Entrega

Escreva sua implementação em [organizador-leituras/](./organizador-leituras/) e crie ali um README com:

- Problema atendido e decisões que tomou.
- Comando exato para executar, indicando de qual diretório partir.
- Explicação dos dados fictícios e das regras.
- Limites da versão.
- Referências às evidências reais das verificações que você escolheu.

Registre execuções em [evidencias/execucoes.md](../evidencias/execucoes.md). Um programa sem erro de execução não comprova sozinho que atende ao enunciado.

**Explique:** descreva o caminho dos dados, as decisões de representação e o papel dos trechos escritos por você, relacionando-os ao que observou.

**Variação posterior:** escolha uma pequena mudança no comportamento da sua POC, implemente por conta própria e registre como verificou seu efeito. Para usá-la no portão do Marco A, cumpra a regra dessa etapa: sem IA, com documentação permitida e escolha autoral de mudança e verificações.

## Critérios da POC

- [ ] Demonstrei as cinco necessidades descritas.
- [ ] Expliquei a representação dos dados e as regras.
- [ ] Expliquei os trechos do programa e suas relações.
- [ ] Documentei a execução e os limites.
- [ ] Registrei evidências e uma mudança independente.

Concluir a POC não conclui sozinho o Marco A nem o módulo. Consulte o [portão essencial](../README.md#portão-do-marco-a--antes-de-http) para reunir também as evidências das missões e da investigação.

## Uso de IA e aplicação profissional

A IA pode ajudar com setup, consulta pontual de sintaxe e uma pista após tentativa na prática assistida. Não pode implementar a POC, escolher modelagem, funções ou verificações. Etapas sem IA não recebem pistas ou correções durante a execução.

A prática de representar informações, consultar uma coleção e explicar mudanças prepara competências usadas em sistemas internos. Esta POC é de aprendizagem, não o projeto de portfólio; a temática não determina a arquitetura da futura API.
