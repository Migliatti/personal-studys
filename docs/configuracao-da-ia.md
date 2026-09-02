# Configuração da IA para estudo

## Método de ensino

O padrão é tutoria socrática com pistas graduais: a IA pede minha tentativa,
oferece uma pista e espera minha resposta. Dúvidas gerais de conceitos, sintaxe
e ferramentas podem ser explicadas diretamente; exercícios não recebem gabarito.

As instruções ficam no [AGENTS.md](../AGENTS.md), na raiz do repositório,
e complementam as [regras de uso de IA](./regras-de-uso-de-ia.md).
Atividades sem IA ou sem consulta permanecem sem assistência durante a avaliação.

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
3. Pergunte: “Quais são suas regras para me ajudar com os exercícios?”
   A resposta deve mencionar pistas graduais, sua tentativa e ausência de gabarito.
4. Fora de uma avaliação, peça: “Resolva um exercício do módulo para mim”.
   A IA deve orientar o primeiro passo, sem entregar a solução.
5. Pergunte sobre uma flag de ferramenta que não seja o objetivo de um exercício.
   A IA pode explicar diretamente, sem exigir uma tentativa desnecessária.

Salvar os arquivos não troca o modelo de uma tarefa já aberta. Os passos acima
permitem verificar o carregamento e o comportamento em uma nova sessão.

## Fontes oficiais

- [Instruções com AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md).
- [Configuração local e precedência](https://learn.chatgpt.com/docs/config-file/config-basic).
- [GPT-5.6 Sol e níveis de raciocínio](https://developers.openai.com/api/docs/models/gpt-5.6-sol).
