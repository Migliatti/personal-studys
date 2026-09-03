# Missões — Lógica e JavaScript na Frota Aurora

Leia o [README do módulo](../README.md) e o conceito relevante no [guia](../guia-de-estudo.md). Faça uma missão por vez, seguindo a ordem do seu percurso.

O **núcleo essencial do Marco A** contém **1, 3, 4, 6, 7, 12, 13, 14 e 15**. As missões **2, 5, 8–11 e 16–18** são **reforço recomendado**, também necessário para a conclusão integral posterior. O portão essencial não é contagem de exercícios: exige as evidências do README.

Crie seus arquivos `.mjs` em [pratica/](./pratica/), sem substituir tentativas existentes. Escolha os nomes dos arquivos. Documentação e pistas após tentativa são permitidas na prática assistida, exceto nas restrições indicadas. Não copie implementações prontas.

Use dados fictícios definidos nos arquivos. Você escolhe valores, representação, regras quando solicitadas, verificações e previsões antes de executar. Registre tentativas, comandos e observações reais nas [evidências](../evidencias/README.md). As variações são posteriores à primeira tentativa; nenhuma explicação ou reflexão vem preenchida.

## Valores e operações

### Missão 1 — Apresentação na ponte de comando

**Percurso:** núcleo essencial. **Conceito técnico:** valores, variáveis e saída no terminal.

**Lore:** a Frota Aurora recebe uma pessoa em treinamento na ponte de comando. O terminal deve apresentar quem chegou e qual aprendizado essa pessoa procura.

**Comportamento e restrições:** mostre um apelido fictício e algo que esse personagem quer aprender, usando variáveis para os dados. Você escolhe o texto e sua apresentação.

**Entrega:** arquivo autoral e registro real da execução. **Explique:** identifique os valores usados e a relação entre o arquivo e a mensagem exibida.

**Variação posterior:** altere um dado escolhido por você, execute e explique o que mudou.

### Missão 2 — Tempo de manutenção do mecha

**Percurso:** reforço. **Conceito técnico:** operações aritméticas e transformação de unidades.

**Lore:** a oficina da Frota Aurora planeja uma manutenção de mecha. A duração foi informada em horas, mas o painel do turno precisa apresentá-la em minutos.

**Comportamento e restrições:** escreva um programa que transforme a duração para um valor escolhido por você. Defina seus próprios dados e verificações, sem entrada obrigatória pelo teclado.

**Entrega:** arquivo e registro da execução. **Explique:** relacione entrada, operação, unidade e saída.

**Variação posterior:** escolha outra duração, registre sua previsão e compare com a execução.

### Missão 3 — Telemetria recebida como texto

**Percurso:** núcleo essencial. **Conceito técnico:** tipos, operações e conversão explícita para número.

**Lore:** um arquivo de telemetria da Frota Aurora traz uma quantidade numérica como texto. A equipe quer compreender o que acontece quando essa leitura entra em uma operação.

**Comportamento e restrições:** compare usar o texto em uma operação e usar sua conversão explícita para número. Escolha a operação e os dados; investigue também uma conversão que não produza número válido.

**Entrega:** experiência autoral, previsão anterior e saída real. **Explique:** compare os tipos e a diferença observada, se houver, sem esconder resultados inesperados.

**Variação posterior:** escolha outra entrada textual e justifique o que espera observar antes de executar.

## Condições e repetições

### Missão 4 — Limite de energia do mecha

**Percurso:** núcleo essencial. **Conceito técnico:** comparação, booleano e decisão condicional.

**Lore:** um mecha da Frota Aurora precisa comunicar sua situação de energia no painel. A equipe de treinamento trabalhará com um limite definido para essa missão.

**Comportamento e restrições:** escolha e documente um limite de energia e informe a situação de uma leitura segundo essa regra. Você decide a regra, as mensagens e como verificar que o programa a representa.

**Entrega:** programa, regra autoral e evidências. **Explique:** relacione a decisão do programa ao critério registrado.

**Variação posterior:** altere o limite ou uma leitura por escolha própria e explique o efeito observado.

### Missão 5 — Sessão de anime da tripulação

**Percurso:** reforço. **Conceito técnico:** combinação de duas condições booleanas.

**Lore:** a tripulação da Frota Aurora organiza uma sessão com títulos de sua biblioteca de anime. A atividade no espaço de convivência depende da presença de um responsável e da disponibilidade da sala.

**Comportamento e restrições:** represente a decisão que considera essas duas exigências em conjunto. Escolha os dados e as verificações; não há expressão condicional fornecida.

**Entrega:** programa e evidências da decisão. **Explique:** justifique como relacionou as exigências.

**Variação posterior:** escolha uma mudança na situação, preveja seu efeito e explique a nova execução.

### Missão 6 — Sequência no painel de expedição

**Percurso:** núcleo essencial. **Conceito técnico:** repetição, estado e término.

**Lore:** o painel de uma expedição da Frota Aurora precisa apresentar uma sequência numérica. A equipe quer entender tanto sua extensão quanto o momento em que a exibição termina.

**Comportamento e restrições:** exiba números entre um início e um fim escolhidos por você. Defina se os extremos participam; escolha a repetição e como verificar seu comportamento, sem necessidade de arrays.

**Entrega:** programa, limites documentados e execução real. **Explique:** por que a repetição termina e como o estado muda.

**Variação posterior:** escolha novos limites e explique a diferença antes e depois de executar.

## Funções e escopo

### Missão 7 — Conversão reutilizável da oficina

**Percurso:** núcleo essencial. **Conceito técnico:** função, interface, parâmetros, chamada e retorno.

**Lore:** diferentes turnos da oficina da Frota Aurora precisam apresentar durações em minutos quando recebem horas. A transformação deve poder ser reutilizada sem depender de uma única exibição no terminal.

**Comportamento e restrições:** crie uma função para essa transformação, decidindo sua interface. A missão é autossuficiente; se fez a missão 2, pode retomar sua tentativa, mas ela não é pré-requisito.

**Entrega:** programa com uso autoral da função e registros reais. **Explique:** entrada, retorno e diferença entre devolver um resultado e exibir uma mensagem.

**Variação posterior:** escolha outra chamada ou uso do retorno, execute e explique o efeito sem mudar a finalidade da transformação.

### Missão 8 — Mensagens entre expedições

**Percurso:** reforço. **Conceito técnico:** parâmetros, argumentos e valores de cada chamada.

**Lore:** a central da Frota Aurora prepara mensagens para expedições distintas. Cada comunicação precisa refletir as informações recebidas naquela ocasião.

**Comportamento e restrições:** crie uma função que construa uma mensagem a partir de informações recebidas, em contexto diferente da apresentação da missão 1. Você escolhe quais informações entram e demonstra chamadas distintas.

**Entrega:** programa e execuções das chamadas escolhidas. **Explique:** quais valores pertencem a cada chamada e de onde vêm.

**Variação posterior:** escolha uma nova chamada e explique o que permanece e o que muda na mensagem.

### Missão 9 — Alcance das leituras de temperatura

**Percurso:** reforço. **Conceito técnico:** escopo de variáveis em funções e blocos.

**Lore:** a oficina da Frota Aurora acompanha leituras fictícias de temperatura durante uma simulação. A equipe quer investigar onde uma variável pode ser acessada no programa que você escrever.

**Comportamento e restrições:** crie uma experiência autoral de acesso a variáveis dentro e fora de funções ou blocos. Preveja antes de executar; falhas são material de investigação, não respostas a esconder.

**Entrega:** experiência, previsão e observação reais. **Explique:** relacione os acessos observados ao escopo.

**Variação posterior:** escolha uma alteração de localização de um acesso ou declaração e investigue seu efeito.

## Arrays e objetos

### Missão 10 — Palavras do inventário de bordo

**Percurso:** reforço. **Conceito técnico:** arrays e percurso de uma coleção.

**Lore:** a Frota Aurora está preparando uma relação de palavras para um inventário fictício da nave. A equipe precisa visualizar todos os itens no terminal.

**Comportamento e restrições:** represente uma coleção de palavras escolhidas por você e apresente todos os itens. Você decide os dados e como verificar o percurso.

**Entrega:** programa e registro real da apresentação. **Explique:** como a coleção é percorrida e como os itens são acessados.

**Variação posterior:** altere a coleção por escolha própria e explique o efeito observado.

### Missão 11 — Equipamento da nave

**Percurso:** reforço. **Conceito técnico:** objeto, propriedades, leitura e alteração.

**Lore:** um equipamento cotidiano fictício acompanha a tripulação da Frota Aurora. Suas informações relacionadas precisam ser representadas no pequeno programa de treinamento.

**Comportamento e restrições:** represente o equipamento em um objeto, escolhendo quais propriedades fazem sentido. Leia e altere uma propriedade; nenhum modelo de domínio é fornecido.

**Entrega:** programa e evidências do acesso e da alteração. **Explique:** diferencie propriedade, nome da propriedade e valor.

**Variação posterior:** escolha outra informação para alterar e explique a nova observação.

### Missão 12 — Consulta aos registros de expedição

**Percurso:** núcleo essencial. **Conceito técnico:** coleção de objetos, percurso, acesso a propriedades e seleção condicional.

**Lore:** a central da Frota Aurora reúne registros fictícios de expedições. Para uma reunião de bordo, será necessário apresentar apenas os registros que atendem a um critério.

**Comportamento e restrições:** represente informações de vários registros em uma coleção de objetos e apresente os que atendem ao critério definido por você. Dados, propriedades, regra e verificações são seus; não há modelo de domínio nem algoritmo fornecido.

**Entrega:** programa, critério documentado e execução real. **Explique:** sua representação, o percurso e a regra aplicada.

**Variação posterior:** escolha uma mudança nos registros ou no critério e explique o efeito da nova execução.

## JSON, módulos e callbacks

### Missão 13 — Registro de bordo em texto

**Percurso:** núcleo essencial. **Conceito técnico:** JSON, serialização, leitura e tipos.

**Lore:** um registro da Frota Aurora precisa ganhar uma representação textual para uma simulação. Depois, a equipe quer voltar a acessar suas informações no programa.

**Comportamento e restrições:** escolha dados simples representáveis em JSON e experimente converter para texto e ler esse texto. Compare tipos e acesso antes e depois; não precisa gravar arquivos ou acessar rede.

**Entrega:** experiência autoral e registros reais das observações. **Explique:** por que o texto não é o próprio objeto em memória.

**Variação posterior:** escolha uma alteração nos seus dados e explique o efeito ao repetir a experiência.

### Missão 14 — Reutilização entre arquivos de bordo

**Percurso:** núcleo essencial. **Conceito técnico:** módulos, exportação, importação e execução.

**Lore:** a equipe da Frota Aurora quer utilizar em outro arquivo um comportamento que você já escreveu. A organização dessa pequena transferência fica sob sua responsabilidade.

**Comportamento e restrições:** exporte e importe um comportamento autoral para utilizá-lo a partir de outro arquivo. Decida a divisão e use `.mjs` com caminhos locais e extensão explícita; não há nomes de funções ou fronteiras de arquivos sugeridos.

**Entrega:** arquivos autorais e comando exato de execução com diretório. **Explique:** a relação entre exportação, importação e uso do comportamento.

**Variação posterior:** escolha uma pequena mudança no uso do comportamento importado e explique o que observou.

### Missão 15 — Avisos agendados na ponte

**Percurso:** núcleo essencial. **Conceito técnico:** função como valor, chamada imediata, callback e agendamento.

**Lore:** a ponte da Frota Aurora experimenta avisos de treinamento. Alguns avisos permitirão observar a diferença entre chamar uma função agora e entregá-la para outra operação chamar.

**Comportamento e restrições:** crie uma pequena experiência para essa comparação; depois use agendamento com `setTimeout`. Registre a previsão da ordem das mensagens antes de executar; não é necessário criar API ou usar promises.

**Entrega:** experiência e registros da previsão e ordem real. **Explique:** função, chamada e callback a partir da observação, sem supor que todo callback seja assíncrono.

**Variação posterior:** escolha uma pequena mudança na experiência e compare sua nova previsão com a execução.

## Integração e reforço posterior

### Missão 16 — Passagem de turno do painel de leituras

**Percurso:** reforço. **Conceito técnico:** integração e explicação do fluxo de dados.

**Lore:** um novo turno da Frota Aurora assumirá o painel de leituras de bordo. A equipe precisa entender o programa que você construiu, não apenas assistir à execução.

**Comportamento e restrições:** com sua POC aberta, explique o caminho dos dados e o papel dos trechos. Registre imprecisões; a IA pode fazer uma pergunta por vez sobre a tentativa, sem escrever a explicação por você.

**Entrega:** explicação autoral e referências aos trechos e evidências. **Explique:** como suas partes se relacionam e onde ainda há dúvida.

**Variação posterior:** escolha outro percurso de uso da sua POC e explique o que muda no caminho dos dados.

### Missão 17 — Ocorrência de treinamento — sem IA

**Percurso:** reforço. **Conceito técnico:** diagnóstico por hipóteses e evidências.

**Lore:** a Frota Aurora realiza uma simulação de falha em um programa de bordo já verificado. O exercício será isolado para preservar a versão funcional.

**Comportamento e restrições:** em uma cópia de programa seu, introduza uma alteração pequena que cause comportamento incorreto. Anote-a separadamente e investigue sem reler essa anotação. Um defeito introduzido por você é prática limitada; não comprova diagnóstico de defeito desconhecido.

Sem IA durante toda a execução. Documentação da linguagem é permitida, soluções prontas não. Você escolhe como verificar a correção. Preserve o original funcional e não deixe versão defeituosa na `main`. A IA não escolhe defeito, causa, correção ou verificações. Declare a atividade encerrada antes de pedir revisão.

**Entrega:** registro próprio de sintoma, hipóteses, evidências, alteração e observação posterior em [diagnostico.md](../evidencias/diagnostico.md). **Explique:** a causa investigada, a relação com a correção e os limites dessa prática.

**Variação posterior:** após a correção, escolha uma pequena variação de uso para observar o comportamento novamente; mantenha a atividade sem IA até declarar seu encerramento.

### Missão 18 — Atualização autoral do painel

**Percurso:** reforço. **Conceito técnico:** modificação independente e verificação de comportamento.

**Lore:** a tripulação da Frota Aurora quer uma pequena atualização no painel de leituras de bordo. Você será responsável por propor a mudança e demonstrar seu efeito.

**Comportamento e restrições:** escolha, descreva e implemente por conta própria uma pequena mudança no comportamento da POC. Documentação é permitida; não peça que a IA determine a mudança ou suas verificações.

**Entrega:** objetivo, versão modificada e registro de como verificou o resultado. **Explique:** o efeito da alteração e o que a evidência sustenta.

**Variação posterior:** escolha outro uso da versão modificada e explique o que sua nova observação permite afirmar.

## Encerramento

As missões 16–18 não substituem a [verificação final](../verificacao-final.md) da conclusão integral. Para o recorte essencial, use o portão próprio do [Marco A](../README.md#portão-do-marco-a--antes-de-http), com explicação, modificação e investigação nas tentativas essenciais e na POC. Registre apenas o que fez e retome conceitos que ainda não consegue explicar.
