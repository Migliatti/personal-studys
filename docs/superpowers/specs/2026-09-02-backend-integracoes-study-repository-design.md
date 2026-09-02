# Backend e Integrações — Design do Repositório de Estudo

## Contexto

Este repositório apoia a transição de Analista de Help Desk e Implantação para Backend Júnior ou Analista de Sistemas/Integrações em 12–18 meses, com dedicação máxima de 8 horas semanais.

## Decisões

- O repositório guarda anotações, exercícios e provas de conceito.
- Projetos concluídos de portfólio são promovidos para repositórios próprios.
- A trilha possui 16 módulos estritamente sequenciais (00–15) e soma 69 semanas, aproximadamente 552 horas.
- O módulo 00 oferece seis semanas de revisão de lógica e fundamentos de JavaScript para quem está retomando programas pequenos e ainda não escreve nas linguagens da trilha. Ele antecede a construção de APIs do módulo 01.
- Cada módulo contém objetivo, checklist, notas, exercícios, POC, evidências e retrospectiva.
- TypeScript/Node é a stack principal; PostgreSQL, Docker, Redis/BullMQ, GitHub Actions e n8n entram apenas após seus pré-requisitos.
- Serviços externos não podem exigir curso pago, infraestrutura paga ou cartão de crédito.
- IA é permitida para setup, sintaxe, boilerplate e formatação; arquitetura e debugging permanecem autorais.
- Um módulo só termina quando o estudante consegue explicar, modificar e depurar sozinho.

## Saídas de portfólio

1. Após o módulo 07: API de operações e SLA.
2. Após o módulo 10: Relay confiável de webhooks.
3. Após o módulo 14: Pipeline de conciliação de implantações.

## Estrutura padrão de módulo

- `README.md`: objetivo, pré-requisito, conteúdo, entregável, verificação e recursos.
- `notas.md`: síntese autoral do conteúdo praticado.
- `exercicios/`: exercícios executáveis.
- `poc/`: prova de conceito integradora.
- `evidencias/`: comandos, saídas e demonstrações do critério de verificação.
- `retrospectiva.md`: entendimento, erros, debugging e próximos passos.

## Restrições de escopo

Kubernetes, Terraform, cloud ampla, certificações, microsserviços, Kafka, GraphQL, NestJS como segundo framework, frontend completo e DDD avançado ficam fora desta primeira trilha.
