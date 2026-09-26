# Sistema de Reserva de Salas — Squad 3

Repositório greenfield da Squad 3. O produto deve permitir consultar disponibilidade, solicitar/cancelar salas e acompanhar decisões administrativas. A squad migrou para **React + Java/Spring Boot + PostgreSQL + Spring Security + Docker**.

## Comece pela documentação

1. [`docs/01-documento-base.md`](docs/01-documento-base.md) — visão, MVP, requisitos, regras, arquitetura, plano e reuso.
2. [`docs/02-backlog-inicial.md`](docs/02-backlog-inicial.md) — primeiras histórias e critérios de aceite.
3. [`docs/03-checklist-de-inicio.md`](docs/03-checklist-de-inicio.md) — prontidão para começar.
4. [`memoria/README.md`](memoria/README.md) — como manter o contexto deste projeto limpo.
5. [`docs/design/experiencia-integrada.png`](docs/design/experiencia-integrada.png) — proposta visual; dados e sincronização são ilustrativos.

## Estrutura

```text
docs/       decisões de produto, requisitos, arquitetura e design
memoria/    contexto curto, mapa de reuso e decisões da squad
frontend/   futura aplicação React
backend/    futura API Java/Spring Boot
infra/      futuro Docker Compose, CI e operação
```

O repositório começa intencionalmente sem implementação. Primeiro valide as regras e o contrato; depois construa um fluxo vertical pequeno com dados sintéticos.

## Regras para contribuição

- A stack alvo está registrada em `memoria/decisoes/ADR-0001-greenfield-e-stack.md`.
- Use referências dos sistemas legados para descobrir comportamento; não copie seus bancos, credenciais, dados ou código sem decisão explícita da squad.
- A disponibilidade precisa ser protegida pela API e pelo PostgreSQL contra requisições concorrentes.
- Atualize requisitos, backlog, memória e evidências junto com cada decisão que altere comportamento.
- Leia [`AGENTS.md`](AGENTS.md) antes de iniciar trabalho assistido por agente.
