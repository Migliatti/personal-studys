# 05-autenticacao-seguranca

**Alvo:** Ambos
**Pré-requisito:** `04-camadas-validacao-erros`
**Tempo estimado:** 4 semanas a 8h/semana

## Objetivo

Autenticar usuários, autorizar ações e proteger segredos sem inventar criptografia.

## Conteúdo

- Autenticação versus autorização.
- Hash de senha, sessões e tokens.
- JWT: claims, expiração, assinatura e limitações.
- RBAC simples: operador e administrador.
- Rate limiting, brute force, CORS, TLS e headers.
- Segredos em variáveis de ambiente.
- OWASP Top 10 aplicado à API.

## Entregável no repo

- Login, hash de senha e autorização por papel.
- Tabela de ameaças e controles.
- Exercícios de token expirado, assinatura inválida e acesso proibido.
- `.env.example` sem valores reais.
- IA aceitável: assinatura de biblioteca e dados fictícios.
- IA proibida: escolher fluxo de autenticação ou diagnosticar falha de segurança.

## Projeto-portfólio

Continuação do Projeto 1.

## Critério de verificação binário

Implementar login e duas permissões sem consulta, demonstrando tentativas inválidas com `401` e `403` corretos.

## Checklist

- [ ] Nenhum segredo versionado.
- [ ] Ameaças e controles documentados.
- [ ] Cenários `401` e `403` demonstrados.
- [ ] Prova binária e retrospectiva concluídas.

## Recursos gratuitos

- [OWASP Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
- [OWASP REST Security Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/REST_Security_Cheat_Sheet.html)
- [RFC 7519 — JWT](https://www.rfc-editor.org/rfc/rfc7519)
