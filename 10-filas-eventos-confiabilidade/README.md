# 10-filas-eventos-confiabilidade

**Alvo:** Ambos
**Pré-requisito:** `09-apis-terceiros-webhooks`
**Tempo estimado:** 5 semanas a 8h/semana

## Objetivo

Processar integrações assíncronas com retry limitado, backoff, idempotência e recuperação manual.

## Conteúdo

- Produtor, consumidor, mensagem e acknowledgment.
- Entrega at least once.
- Retry com backoff e jitter.
- Erros transitórios e permanentes.
- Dead-letter queue, inbox/outbox e replay.
- Idempotência, ordenação e concorrência.
- BullMQ e Redis como implementação didática.

## Entregável no repo

- POC com API produtora, worker e Redis.
- Retry exponencial limitado, fila de falhas e replay.
- Métricas de processados, reprocessados e falhos.
- Experimento derrubando o worker no meio da execução.
- IA aceitável: configuração inicial do BullMQ.
- IA proibida: classificar erros, definir retry, idempotência ou causa-raiz.

## Projeto-portfólio — saída 2

Promover o **Relay confiável de webhooks**: HMAC, inbox, fila, retry, dead-letter, idempotência, replay, OpenAPI e guia operacional.

## Critério de verificação binário

Interromper o worker entre efeito e acknowledgment, reiniciar e demonstrar ausência de efeito duplicado e presença de auditoria.

## Checklist

- [ ] Retry possui limite e jitter.
- [ ] Falha permanente vai para dead-letter.
- [ ] Projeto 2 passou pelo portão de domínio.
- [ ] Repo próprio criado e linkado no README raiz.

## Recursos gratuitos

- [BullMQ Guide](https://docs.bullmq.io/)
- [RabbitMQ Tutorials](https://www.rabbitmq.com/tutorials)
- [AWS Builders’ Library — Retry and backoff](https://aws.amazon.com/builders-library/timeouts-retries-and-backoff-with-jitter/)
