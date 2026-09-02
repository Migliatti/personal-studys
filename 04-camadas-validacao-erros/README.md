# 04-camadas-validacao-erros

**Alvo:** Ambos
**Pré-requisito:** `03-node-typescript-api`
**Tempo estimado:** 4 semanas a 8h/semana

## Objetivo

Separar transporte, regra de negócio e persistência, produzindo erros previsíveis e respostas seguras.

## Conteúdo

- Handler, serviço/use case e repositório.
- Injeção manual de dependência.
- DTO versus entidade de domínio.
- Validação com Zod ou JSON Schema.
- Erros de domínio, infraestrutura e programação.
- Error handler central e identificador de correlação.
- Proteção de stack trace e detalhe interno.

## Entregável no repo

- Refatoração da POC para camadas.
- Matriz `erro → status → resposta → log`.
- Script exercitando entradas inválidas.
- Bug de acoplamento documentado e corrigido.
- IA aceitável: consultar API da biblioteca de validação.
- IA proibida: escolher responsabilidades, exceções ou fronteiras.

## Projeto-portfólio

Continuação do Projeto 1; ainda não promover.

## Critério de verificação binário

Trocar o adaptador de persistência sem alterar o serviço e provar que cinco entradas inválidas não alcançam a regra de negócio.

## Checklist

- [ ] Camadas possuem dependências explícitas.
- [ ] Erros seguem contrato consistente.
- [ ] Cinco entradas inválidas demonstradas.
- [ ] Prova binária e retrospectiva concluídas.

## Recursos gratuitos

- [Fastify — Validation and Serialization](https://fastify.dev/docs/latest/Reference/Validation-and-Serialization/)
- [Zod](https://zod.dev/)
- [RFC 9457 — Problem Details](https://www.rfc-editor.org/rfc/rfc9457)
