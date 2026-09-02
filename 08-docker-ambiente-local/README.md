# 08-docker-ambiente-local

**Alvo:** Ambos
**Pré-requisito:** `07-testes-automatizados`
**Tempo estimado:** 3 semanas a 8h/semana

## Objetivo

Executar API, PostgreSQL, Redis e n8n localmente em ambientes reproduzíveis.

## Conteúdo

- Imagem, container, volume, rede e registry.
- Dockerfile multi-stage e Docker Compose.
- Health checks e ordem de inicialização.
- Bind mounts versus volumes.
- Usuário não-root, recursos, logs e persistência.

## Entregável no repo

- POC com API, Postgres e Redis.
- Dockerfile multi-stage e `compose.yml`.
- Scripts documentados para subir, derrubar e recriar.
- Comparação de tamanho de duas imagens.
- IA aceitável: sintaxe YAML e boilerplate inicial.
- IA proibida: topologia, persistência ou debugging de rede.

## Projeto-portfólio

Aplicar Docker ao Projeto 1 no repo próprio.

## Critério de verificação binário

Subir tudo com um comando em ambiente limpo, recriar containers sem perder dados e diagnosticar um serviço deliberadamente sem rede.

## Checklist

- [ ] Build reproduzível.
- [ ] Dados sobrevivem à recriação correta.
- [ ] Falha de rede diagnosticada sem IA.
- [ ] Prova binária e retrospectiva concluídas.

## Recursos gratuitos

- [Docker — Get Started](https://docs.docker.com/get-started/)
- [Docker Compose](https://docs.docker.com/compose/)
- [Dockerfile best practices](https://docs.docker.com/build/building/best-practices/)
