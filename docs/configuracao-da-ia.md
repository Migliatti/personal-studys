# Configuração da IA para estudo

## Método de ensino

O padrão é tutoria socrática com pistas graduais. Antes de orientar uma
atividade, a IA lê a atividade atual, as evidências existentes e o ponto de
retomada. Ela define um objetivo pequeno e trabalha em uma atividade por vez.

Conceitos novos, sintaxe e ferramentas podem ser explicados diretamente; para
conceitos novos, a explicação usa um exemplo curto de outro contexto. Ajuda
específica sobre a atividade só vem depois da minha tentativa. A IA oferece uma
pista por interação e espera minha resposta antes de ampliar a ajuda. Ao revisar,
separa acertos verificáveis das lacunas, pede uma explicação e uma pequena
alteração autoral. Ela encerra com um próximo passo concreto e orientação para
registrar apenas fatos do progresso.

Dificuldade, demora ou desânimo não são interpretados como traços psicológicos:
a IA investiga compreensão, tamanho da tarefa e condições de execução. Exercícios
não recebem gabarito. Atividades sem IA ou sem consulta não recebem pistas nem
correções durante a avaliação.

As instruções ficam no [AGENTS.md](../AGENTS.md), na raiz do repositório,
e complementam as [regras de uso de IA](./regras-de-uso-de-ia.md).


## Modelo escolhido

- Modelo: **GPT-5.6 Sol** (`gpt-5.6-sol`).
- Esforço de raciocínio: **médio** (`medium`).
- Configuração local: [`.codex/config.toml`](../.codex/config.toml).

A escolha prioriza qualidade de raciocínio e revisão técnica. O nível médio é
um ponto de partida para interações curtas de estudo. É uma recomendação para
este projeto, não uma comparação experimental entre tutores. O catálogo local
do Codex consultado em 02/09/2026 oferece esse modelo e esse nível de raciocínio.

O comportamento de tutoria depende das instruções, não apenas do modelo.
Essas instruções orientam o Codex; não são um bloqueio técnico infalível e não
configuram automaticamente outras ferramentas de IA.

## Como ativar e conferir

1. Abra uma nova tarefa do Codex neste projeto para carregar as instruções.
2. A configuração local depende de o projeto estar marcado como confiável no
   Codex. Confira se o seletor da tarefa mostra GPT-5.6 Sol e raciocínio médio;
   uma seleção explícita na sessão pode prevalecer sobre o padrão do arquivo.
3. Pergunte: “Quais são suas regras para me ajudar com os exercícios?” A resposta
   deve mencionar objetivo pequeno, uma atividade por vez, tentativa, uma pista,
   acertos verificáveis, pequena alteração e ausência de gabarito.
4. Fora de uma avaliação, apresente uma atividade, seu entendimento e uma
   tentativa mínima. A IA deve manter um objetivo pequeno e oferecer apenas uma
   pista, sem entregar a solução.
5. Peça uma revisão dessa tentativa. A IA deve distinguir acertos verificáveis de
   lacunas e pedir uma explicação e uma pequena alteração autoral.
6. Pergunte qual é o próximo passo e o que registrar. A IA deve indicar uma ação
   concreta e orientar um registro factual, sem marcar a atividade como concluída.
7. Em uma atividade marcada como sem IA ou sem consulta, a IA deve aguardar o
   encerramento da avaliação antes de oferecer pistas ou correções.
8. Pergunte sobre uma flag de ferramenta que não seja o objetivo de um exercício.
   A IA pode explicar diretamente, sem exigir uma tentativa desnecessária.

Salvar os arquivos não troca o modelo de uma tarefa já aberta. Os passos acima
permitem verificar o carregamento e o comportamento em uma nova sessão.

## Fontes oficiais

- [Instruções com AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md).
- [Configuração local e precedência](https://learn.chatgpt.com/docs/config-file/config-basic).
- [GPT-5.6 Sol e níveis de raciocínio](https://developers.openai.com/api/docs/models/gpt-5.6-sol).
