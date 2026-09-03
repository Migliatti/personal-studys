# Trajetória essencial de Backend até janeiro de 2027 — Design

## Contexto confirmado

Em 3 de setembro de 2026, o repositório possui 16 módulos sequenciais, 69 semanas estimadas e 552 horas a oito horas por semana. O primeiro projeto de portfólio é promovido somente após o módulo 07, por volta da semana 36. A página inicial aponta para o módulo 00, mas não resume em um único lugar a sessão atual, a próxima entrega e as evidências necessárias para avançar.

O estudante está retomando fundamentos, pretende começar Ciência da Computação em janeiro de 2027 e busca sua primeira oportunidade de backend por estágio ou vaga júnior. O planejamento usa oito horas semanais como base e até sete horas adicionais apenas como margem opcional. Conhecer termos ou utilizar IA não comprova domínio; tentativas, explicações, modificações e investigação independente continuam sendo as evidências de aprendizagem.

## Decisão de organização

A estrutura numerada `00`–`15` e seus caminhos serão preservados. O repositório passará a apresentar dois horizontes:

1. **Trajetória essencial até janeiro de 2027:** fundamentos e uma API pequena, completa e demonstrável.
2. **Continuação de longo prazo:** aprofundamentos de backend e integrações que não cabem com segurança no primeiro horizonte.

Os módulos deixam de ser interpretados como uma única fila obrigatória de 69 semanas. Documentos centrais indicarão quais recortes de módulos pertencem à trajetória essencial e quais módulos completos ficam para depois. Datas serão referências de planejamento; avanço continuará condicionado a evidências.

Essa abordagem foi escolhida porque preserva histórico, links, tentativas e materiais existentes. Renumerar todos os módulos causaria ruptura desnecessária. Manter apenas um atalho informal não resolveria a falta de um caminho executável até janeiro.

## Trajetória essencial

A trajetória essencial terá 16 semanas estimadas, com uma semana de margem antes de janeiro de 2027. Se uma evidência não for atingida, o prazo se desloca e a entrega é reduzida; o conteúdo não é comprimido e não há promessa de empregabilidade.

| Fase | Semanas estimadas | Carga-base | Resultado observável |
|---|---:|---:|---|
| 1. Retomada de JavaScript e Git | 1–3 | 24 h | Programas pequenos explicados, modificados e versionados em commits coerentes |
| 2. HTTP aplicado | 4–5 | 16 h | Requisições analisadas e servidor HTTP pequeno explicado pelo estudante |
| 3. Node.js e TypeScript | 6–8 | 24 h | API em memória com TypeScript estrito, execução reproduzível e comportamento assíncrono compreendido |
| 4. SQL e PostgreSQL essencial | 9–11 | 24 h | Esquema autoral pequeno, migrations simples e consultas com filtros, agregação e `JOIN` |
| 5. Projeto integrado, testes e documentação | 12–15 | 32 h | API persistida com testes essenciais, README técnico e demonstração reproduzível |
| 6. Publicação e apresentação | 16 | 8 h | API publicada quando houver opção gratuita adequada, ou demonstração local reproduzível se a publicação bloquear |
| Margem de calendário | 17 | até 8 h base | Retomar lacunas ou reduzir o escopo final sem fingir conclusão |

As horas adicionais, até o limite total de 15 horas semanais, não recebem conteúdo obrigatório novo. Elas servem para repetição, recuperação de uma semana, leitura complementar, correção autoral e prática opcional.

### Marcos de domínio

- **Marco A — fundamentos:** executar, explicar e modificar JavaScript com valores, decisões, repetições, funções, arrays, objetos, módulos e JSON; usar Git para registrar sessões coerentes.
- **Marco B — protocolo:** explicar request e response, método, URL, cabeçalhos, corpo e status; observar e modificar um servidor HTTP pequeno.
- **Marco C — API tipada:** executar uma API TypeScript, explicar tipos relevantes e o fluxo assíncrono, e modificar um comportamento sem copiar solução.
- **Marco D — persistência:** propor e justificar um modelo pequeno, recriar o banco e escrever consultas fundamentais sem depender de ORM.
- **Marco E — projeto demonstrável:** executar testes escolhidos pelo estudante, reconstruir o ambiente, explicar decisões e apresentar a API em cinco minutos.

Se o Marco A exigir mais de três semanas, os marcos seguintes serão deslocados. Para ainda produzir uma entrega até janeiro, o projeto pode perder funcionalidades e manter somente um recurso principal com persistência, testes e documentação. Evidências não serão eliminadas para satisfazer o calendário.

## Projeto essencial de portfólio

O primeiro projeto será uma **API de registros de expedições**, em um universo original de exploração espacial. O tema não determina arquitetura nem modelo de dados.

O produto deve permitir uma apresentação profissional: problema atendido, contrato HTTP, decisões de modelagem, persistência, tratamento básico de erros, testes selecionados pelo estudante, instruções de execução e limites conhecidos. Sua aplicação profissional é demonstrar fundamentos comuns a APIs internas e sistemas operacionais: receber dados, validar um contrato, persistir registros, consultar informações e comunicar o comportamento técnico.

### Escopo máximo da primeira versão

- Uma API HTTP em Node.js e TypeScript.
- Um recurso de domínio principal relacionado a registros de expedição.
- PostgreSQL com esquema e migrations reproduzíveis.
- Operações suficientes para demonstrar criação e consulta, definidas pelo estudante durante o projeto.
- Tratamento básico de entradas inválidas e falhas esperadas, decidido e justificado pelo estudante.
- Testes essenciais orientados pelos riscos identificados pelo estudante.
- README técnico, exemplos de uso fictícios e roteiro de demonstração.
- Publicação gratuita sem cartão quando houver opção vigente; caso contrário, demonstração local reproduzível documentada.

Não são requisitos da primeira versão: autenticação, autorização, ORM, Docker, Redis, filas, webhooks, CI/CD avançado, observabilidade completa, frontend ou múltiplos serviços. Um segundo projeto permanece opcional e só começa depois que o primeiro estiver demonstrável.

## Continuação de longo prazo

O horizonte posterior preservará os módulos atuais como aprofundamentos, reorganizados por dependência:

1. Arquitetura em camadas, validação e tratamento de erros.
2. Autenticação, autorização e segurança.
3. ORM, transações e desempenho de persistência.
4. Testes adicionais e integração contínua.
5. Docker e ambiente local reproduzível.
6. APIs de terceiros e webhooks.
7. Filas, eventos, retry, idempotência e recuperação.
8. Logs, monitoramento, deploy e operação aprofundados.
9. n8n, automação, ETL e documentação de integrações.
10. Empregabilidade contínua apoiada em evidências reais.

Os conteúdos não serão apagados. Cada README indicará seu horizonte e, quando necessário, o recorte essencial utilizado antes do estudo completo do módulo.

## Organização da página inicial

O `README.md` raiz será transformado em um painel de retomada com cinco respostas visíveis no início:

- **Onde estou:** módulo 00, semana 1, sessão 1, sem afirmar que a atividade já foi realizada.
- **Abra agora:** link exato para a primeira sessão do guia do módulo 00.
- **Próxima entrega:** tentativa autoral do primeiro exercício e registro factual da execução.
- **Como pedir ajuda:** formato curto com atividade, entendimento, tentativa, evidência e dúvida.
- **Como avançar:** explicação, modificação, investigação e registros exigidos pelo marco atual.

O cronograma de 69 semanas será substituído na apresentação principal pelos dois horizontes. A estimativa histórica poderá ser mencionada na especificação, mas não continuará como caminho padrão.

## Primeira semana completamente detalhada

A primeira semana continuará dentro do módulo 00 e terá quatro sessões de até duas horas:

1. **Sessão 1 — ambiente e primeiro ciclo:** conferir Node e Git, executar o arquivo de preparação já existente, estudar valores e variáveis, iniciar a missão 1 e registrar onde parou.
2. **Sessão 2 — operações e conversões:** concluir ou revisar a missão 1, realizar as missões 2 e 3 conforme o ritmo e registrar previsões e saídas reais.
3. **Sessão 3 — variação e explicação:** alterar dados ou uma regra pequena nas próprias tentativas, executar novamente e explicar tipos, entrada, processamento e saída.
4. **Sessão 4 — consolidação e Git:** revisar lacunas, organizar evidências, produzir um commit coerente e registrar a semana no diário.

Cada sessão exibirá objetivo, preparação, conceito técnico, missão, entrega, evidência de compreensão e próximo passo. O material não presumirá que os três exercícios foram concluídos no mesmo ritmo.

## Universo temático

Será usado um universo original e leve de exploração espacial chamado **Frota Aurora**. Todo exercício existente ou criado no futuro terá uma pequena situação narrativa ligada a ficção científica, mechas, anime, exploração espacial ou tecnologia futurista. Somente passos puramente mecânicos de setup podem ficar sem lore. A narrativa terá no máximo algumas frases por atividade e nunca exigirá conhecimento de franquias.

As atividades existentes receberão ambientações como energia e temperatura de mechas, inventário de nave, expedições, telemetria, registros de missão e biblioteca de animações. Em cada atividade ficarão explícitos:

- conceito técnico praticado;
- ambientação curta;
- comportamento desejado e restrições;
- entrega e explicação esperadas;
- variação posterior de compreensão.

Os nomes temáticos não fornecerão modelo de dados, algoritmo, arquitetura, estratégia de testes ou resposta esperada. Projetos explicarão também a aplicação profissional das competências praticadas.

## Tutoria e autonomia

O `AGENTS.md`, `docs/regras-de-uso-de-ia.md` e `docs/configuracao-da-ia.md` serão alinhados ao seguinte fluxo:

1. Ler a atividade atual, as evidências existentes e o ponto de retomada.
2. Apresentar um objetivo pequeno e uma atividade por vez.
3. Ensinar conceitos novos diretamente, usando exemplos curtos de outro contexto.
4. Esperar uma tentativa antes de oferecer ajuda específica sobre a atividade.
5. Dar uma pista por interação quando houver bloqueio.
6. Separar acertos verificáveis de lacunas ao revisar uma tentativa.
7. Pedir uma explicação e uma pequena alteração autoral para verificar compreensão.
8. Encerrar com próximo passo concreto e orientar somente o registro factual do progresso.

Dificuldade, desânimo ou demora não serão interpretados como traços psicológicos. A tutoria investigará compreensão, tamanho da tarefa e condições de execução.

Durante atividades avaliadas, a IA não fornecerá implementação, gabarito, pseudocódigo resolutivo, arquitetura, modelagem, estratégia de testes ou causa-raiz. Atividades marcadas como sem IA continuarão sem pistas durante a execução. Funcionamento isolado não será aceito como domínio: o estudante deverá explicar, modificar e investigar.

## Arquivos previstos

### Documentos centrais

- Modificar `README.md` para o painel de retomada e os dois horizontes.
- Criar `docs/trajetoria-essencial.md` com fases, marcos, carga e regras de redução de escopo.
- Criar `docs/continuacao-longo-prazo.md` com os aprofundamentos e dependências.
- Modificar `docs/portfolio-map.md` para antecipar o projeto essencial e deixar projetos adicionais opcionais ou posteriores.
- Modificar `docs/diario-de-estudo.md` apenas no formato e no próximo passo já factual, sem inventar horas ou entregas.
- Modificar `AGENTS.md`, `docs/regras-de-uso-de-ia.md` e `docs/configuracao-da-ia.md` para unificar o protocolo de tutoria.

### Primeiro percurso e exercícios

- Modificar `00-logica-javascript/README.md`, `guia-de-estudo.md`, `exercicios/README.md`, `poc/README.md` e `verificacao-final.md` para o ritmo essencial e a temática.
- Modificar `01-http-rest/README.md`, `guia-de-estudo.md`, `exercicios/README.md` e `poc/README.md` para o novo horizonte e a temática.
- Atualizar os READMEs dos módulos `02`, `03`, `07` e `12` para identificar seus recortes essenciais.
- Atualizar os demais READMEs para identificá-los como continuação e corrigir pré-requisitos conceituais quando necessário.
- Modificar os templates pedagógicos para exigir conceito, ambientação, entrega, explicação, variação e evidência.

Arquivos de tentativa, código, notas preenchidas, evidências e retrospectivas não serão substituídos. O arquivo `00-logica-javascript/exercicios/pratica/primeiro-programa.mjs` será preservado byte a byte.

## Verificação da implementação

Antes da conclusão serão executadas as seguintes verificações:

- comparar a lista de arquivos de tentativa e evidência antes e depois;
- confirmar que o arquivo de prática existente não mudou;
- procurar links Markdown relativos e validar se seus destinos locais existem;
- conferir totais de semanas e horas da trajetória essencial;
- revisar a ordem de pré-requisitos entre JavaScript, HTTP, Node/TypeScript, SQL, testes, documentação e publicação;
- conferir que cada missão mantém seu conceito técnico original;
- procurar trechos que forneçam resultado esperado, algoritmo, pseudocódigo resolutivo, arquitetura ou estratégia de testes;
- confirmar que nenhum status de módulo, hora estudada ou critério foi marcado como concluído;
- revisar o diff final para detectar mudanças fora do escopo.

## Condições de conclusão

A manutenção estará concluída quando a página inicial oferecer um primeiro passo inequívoco, os dois horizontes estiverem coerentes, a primeira semana estiver integralmente detalhada, os exercícios existentes tiverem missões temáticas sem gabarito, a tutoria estiver consistente e as verificações acima passarem.

A manutenção não inicia nem resolve a primeira atividade do estudante, não cria o projeto de portfólio e não publica ou envia alterações para serviços externos.
