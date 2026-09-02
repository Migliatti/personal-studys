# Guia de estudo — HTTP e REST

Seu objetivo é olhar uma requisição e explicar o que foi pedido, para quem, com quais dados e qual resposta chegou. Ao final, você vai construir e diagnosticar um servidor pequeno.

Antes de iniciar este módulo, conclua o [módulo 00 — Lógica e JavaScript](../00-logica-javascript/README.md). Este guia parte da prática de programas pequenos; o servidor HTTP será uma aplicação dessa base.

## Como estudar

Leia um trecho, execute uma atividade e registre o que observou em [notas.md](./notas.md). Antes de rodar um comando, escreva sua previsão. Depois, compare o resultado. As respostas e decisões dos exercícios devem ser suas. Use o [modo de tutoria do projeto](../AGENTS.md): durante a prática assistida, a IA pode orientar uma tentativa sua com uma pista por vez, esperando sua resposta antes de avançar. A [configuração da IA](../docs/configuracao-da-ia.md) registra o modelo escolhido; os limites de ajuda valem independentemente do modelo.

Reserve três semanas de até oito horas, totalizando 24 horas. Se uma atividade demorar mais, desloque as próximas. A prova de 40 minutos é para o encerramento, depois da prática.

## Sessão 1 — comece aqui (duas horas)

### 1. Preparar o ambiente — 10 minutos

Abra o PowerShell:

```powershell
Set-Location -LiteralPath 'C:\Users\Gabriel Speedpro\Music\projetos\personal-studys\01-http-rest'
node --version
curl.exe --version
```

Na preparação deste guia, em 02/09/2026, foram encontrados Node.js `v24.20.0` e curl `8.21.0`. Não é necessário instalar pacotes para esta sessão. Use `curl.exe` no Windows para chamar diretamente o programa.

### 2. Entender a conversa — 20 minutos

O **cliente** inicia uma requisição: pode ser seu navegador, curl ou outro programa. O **servidor** recebe essa mensagem e produz uma resposta. **HTTP** define como essa comunicação funciona. Uma **API** oferece uma interface para programas interagirem; neste módulo, essa interface usa HTTP.

```text
Cliente                       Servidor
   | ---- requisição HTTP ----> |
   | <---- resposta HTTP ------ |
```

Uma página pode exigir várias requisições, por exemplo para HTML, imagens e dados. HTTP é um protocolo sem estado: a aplicação precisa transportar o contexto necessário, por exemplo com cookies, quando oferece uma sessão. Isso não impede o servidor de armazenar dados. Leia a [visão geral da MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Overview).

### 3. Observar três requisições — 45 minutos

Para cada comando abaixo, leia a pergunta “Antes” e registre sua previsão antes de executar. Depois, faça sua própria leitura da saída e responda à pergunta “Depois”. Os comandos são material de observação guiada; não são respostas preenchidas nem definem o contrato da sua POC. O [httpbin](https://httpbin.org/) é um serviço de demonstração para inspecionar requisições. Use apenas dados fictícios. Se estiver indisponível, registre o bloqueio e tente em outra sessão; uma falha de conexão não é a resposta HTTP esperada do exercício.

**A — Parâmetros na URL**

```powershell
curl.exe --http1.1 --connect-timeout 10 --max-time 30 -v 'https://httpbin.org/get?curso=http&semana=1'
```

Antes: onde você acha que os valores `http` e `1` aparecerão? Depois: encontre método, caminho, status e os parâmetros devolvidos no corpo.

**B — Cabeçalho próprio**

```powershell
curl.exe --http1.1 --connect-timeout 10 --max-time 30 -v -H 'X-Estudo: modulo-01' 'https://httpbin.org/headers'
```

Antes: o cabeçalho mudará a URL? Depois: encontre o valor enviado na requisição e no JSON devolvido. Diferencie um cabeçalho real da resposta de um campo JSON que descreve sua requisição.

**C — Resposta de erro**

```powershell
curl.exe --http1.1 --connect-timeout 10 --max-time 30 -v 'https://httpbin.org/status/404'
```

Antes: você espera um corpo? Depois: registre status e presença ou ausência de corpo. Aqui, o código foi solicitado a um simulador; você ainda não diagnosticou a causa de um erro numa API real.

Na saída, `>` indica cabeçalhos enviados, `<` indica recebidos e `*` traz informações de conexão. O corpo aparece separadamente. `-v` mostra detalhes; `-H` adiciona um cabeçalho; `--http1.1` facilita a leitura usando essa versão; os limites evitam espera indefinida. O curl pode terminar com código de saída zero mesmo recebendo HTTP 404: sucesso de transferência difere de sucesso HTTP. Referência: [manual do curl](https://curl.se/docs/manpage.html).

### 4. Registrar e explicar — 30 minutos

Preencha as três fichas em [notas.md](./notas.md). Cole apenas os trechos necessários para sustentar suas observações. Não registre tokens, cookies de sessão ou dados pessoais.

Feche o guia e a ajuda de IA por cinco minutos e explique em voz alta quem era o cliente, quem era o servidor, o que enviou e o que recebeu. Durante essa recuperação de memória, não peça pistas. Encerre a tentativa e só então reabra o material para revisar o que faltou.

### 5. Encerrar — 15 minutos

- [ ] Executei três requisições ou registrei um bloqueio concreto.
- [ ] Diferenciei cabeçalhos enviados, recebidos e corpo.
- [ ] Registrei uma previsão que confirmei ou corrigi.
- [ ] Anotei uma dúvida para a próxima sessão.

Registre o tempo real. No fim da semana, atualize o [diário](../docs/diario-de-estudo.md). Ler este material não equivale a executar as atividades.

## Conceitos para as próximas sessões

### URL

No exemplo fictício `https://api.exemplo.test:443/chamados/42?idioma=pt#detalhes`, `https` é o esquema, `api.exemplo.test` é o host, `443` é a porta explícita, `/chamados/42` é o caminho e `idioma=pt` é a query. O fragmento `#detalhes` é tratado pelo cliente e não é enviado como parte do alvo da requisição HTTP. Não execute esse endereço fictício. Consulte [o que é uma URL](https://developer.mozilla.org/en-US/docs/Learn_web_development/Howto/Web_mechanics/What_is_a_URL).

### Mensagens e JSON

Uma requisição HTTP/1.1 tem linha inicial com método, alvo e versão, seguida de cabeçalhos e, quando presente, corpo. A resposta contém versão, status, cabeçalhos e, quando aplicável, corpo. JSON é um formato de dados que pode aparecer nesse corpo. HTTP/2 e HTTP/3 mudam a representação das mensagens no transporte; este exemplo textual é didático para HTTP/1.1:

```http
GET /catalogo?pagina=2 HTTP/1.1
Host: loja.exemplo.test
Accept: application/json
```

Explique cada linha sem copiar o guia. Referência: [mensagens HTTP — MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Messages).

### Métodos e repetição

| Método | Semântica geral |
|---|---|
| GET | Solicitar uma representação |
| HEAD | Solicitar os cabeçalhos correspondentes a GET, sem o corpo da resposta |
| POST | Pedir que o recurso processe o conteúdo enviado |
| PUT | Criar ou substituir o estado do recurso alvo pela representação enviada |
| PATCH | Aplicar modificações parciais |
| DELETE | Solicitar a remoção da associação do recurso alvo |

**Seguro** significa que a semântica é essencialmente de leitura; não significa ausência de logs ou criptografia. **Idempotente** significa que repetir pedidos idênticos tem o mesmo efeito pretendido que fazê-lo uma vez; as respostas podem variar. GET, HEAD, PUT e DELETE têm semântica idempotente; POST e PATCH não oferecem essa garantia geral. Você justificará o comportamento da sua POC. Consulte [métodos HTTP — MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods).

### Status e cabeçalhos

| Família | Significado geral |
|---|---|
| 1xx | Informação provisória |
| 2xx | Sucesso |
| 3xx | Redirecionamento ou outras condições dessa classe, como 304 |
| 4xx | Erro associado à requisição do cliente |
| 5xx | Falha do servidor ao atender uma requisição |

O significado específico depende do código. `Content-Type` descreve o formato do conteúdo enviado naquela mensagem. `Accept` expressa preferências do cliente para a representação recebida. Declarar JSON não transforma texto inválido em JSON. A negociação depende do suporte do servidor. Para escolher os códigos do exercício, consulte a [RFC 9110, seções 8.3, 12 e 15](https://www.rfc-editor.org/rfc/rfc9110.html).

### Antes da resposta

No cenário HTTPS com HTTP/1.1 usado aqui, pense na sequência simplificada: resolver o host via DNS, estabelecer TCP, negociar TLS e trocar mensagens HTTP. DNS ajuda a localizar o servidor; TCP transporta os dados; TLS protege a comunicação. Cache, proxies e conexões reaproveitadas podem mudar o que aparece na saída. Não generalize TCP para toda versão de HTTP. Revise a [visão geral de HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Overview) junto com a saída do curl.

### REST e organização de uma API

REST é um estilo arquitetural com restrições como interface uniforme, comunicação sem estado, cache e camadas. Usar JSON e verbos HTTP, isoladamente, não comprova que uma API segue REST. RPC organiza a interação em chamadas de operações. Estude a diferença e explique como reconheceria cada abordagem. Não precisa implementar todas as restrições REST nesta POC. Referência: [REST — MDN](https://developer.mozilla.org/en-US/docs/Glossary/REST).

Filtros, paginação e versionamento também entram nos exercícios. Você investigará como um contrato comunica esses comportamentos. Basta documentar propostas no papel; implementá-los não é exigência adicional da prova final.

## Roteiro das três semanas

Cada sessão dura duas horas. Nas sessões 4, 8 e 12, use uma hora para POC e uma para revisão, diagnóstico e registros. Cada semana reserva duas horas de teoria aplicada, duas de exercícios, três de POC e uma de revisão.

| Semana | Sessão | Foco | Entrega |
|---|---:|---|---|
| 1 | 1 | Teoria aplicada e três observações guiadas | Anatomia das requisições nas notas |
| 1 | 2 | Exercícios 1 e 2: URL e DevTools | Comparações registradas |
| 1 | 3 | POC: enunciado e início das duas rotas GET | Código autoral |
| 1 | 4 | Continuar POC; introduzir e investigar erro de status sem IA | Diagnóstico próprio e diário |
| 2 | 5 | Teoria: métodos, idempotência, JSON e status | Explicações próprias |
| 2 | 6 | Exercícios 3 e 4: semântica e contrato | Decisões justificadas por você |
| 2 | 7 | POC: receber corpo e trabalhar na rota POST | Implementação autoral |
| 2 | 8 | Continuar POC e revisar contrato contra execução | Evidências reais e diário |
| 3 | 9 | Teoria: conexão, REST/RPC, filtros, paginação e versões | Comparação escrita |
| 3 | 10 | Exercícios 5 e 6: contrato; explicação sem consulta e diagnóstico sem IA | Propostas e explicação próprias |
| 3 | 11 | POC: revisar e praticar reconstrução | Execução reproduzível |
| 3 | 12 | POC: prova de 40 min sem consulta nem IA; 20 min para evidências; 1h de revisão | Resultado, retrospectiva e diário |

Se funções, condicionais, objetos ou callbacks ainda bloquearem a sessão 3, retome a prática correspondente do [guia do módulo 00](../00-logica-javascript/guia-de-estudo.md). Desloque o roteiro se necessário.

## Ajuda durante o módulo

### Durante a prática assistida

Apresente o enunciado, sua tentativa e a dúvida específica. Se houver comandos, inclua sua previsão e o trecho real da saída. A IA deve identificar o que você já entendeu, oferecer no máximo uma pista e esperar sua próxima tentativa. Ela não deve preencher notas, montar sua tabela de respostas ou editar a solução do exercício.

Você pode pedir:

> Estou na atividade [número]. Minha tentativa foi [...], observei [...] e minha dúvida é [...]. Faça uma pergunta que me ajude a avançar, sem resolver a questão.

> Revise minha justificativa abaixo. Indique uma lacuna conceitual por vez, sem escrever a resposta corrigida.

Se não souber começar, diga o que entendeu do enunciado. A IA pode retomar um conceito ou apresentar um exemplo menor de outro contexto; não deve entregar a mesma solução com nomes trocados. Se pedir “resolva para mim”, a orientação continua por pistas.

### Explicações diretas permitidas

Peça explicações gerais de conceitos, sintaxe ou ferramentas, como “o que significa esta flag?” ou “qual é a assinatura desta função?”. Uma explicação pode ser direta quando não responde ao objetivo avaliado. A IA pode ajudar com preparação do ambiente e sintaxe mínima; não deve montar as rotas ou o tratamento de erros da POC.

Você decide contrato, status e comportamento de repetição, além da estratégia de verificação. As tabelas conceituais deste guia são material de estudo: seus exemplos, escolhas e justificativas continuam sendo autorais.

### Durante atividades sem IA ou sem consulta

- Na investigação do defeito de status, trabalhe sem IA, incluindo a escolha do defeito, as hipóteses, a identificação da causa e a correção.
- Na explicação sem consulta do exercício 6 e nos momentos de recuperação de memória com o guia fechado, não use pistas nem correções da IA.
- Na prova de 40 minutos, feche este guia, notas, documentação, código anterior e ajuda de IA. Não peça validação parcial durante a tentativa.

Encerre e registre a tentativa antes de solicitar revisão. Depois, a IA pode ajudar a reconhecer lacunas no seu relato e orientar a próxima prática, sem inventar evidências nem marcar o módulo como concluído.

Consulte as [regras de uso de IA](../docs/regras-de-uso-de-ia.md) e registre usos relevantes na [retrospectiva](./retrospectiva.md), com suas próprias palavras.
