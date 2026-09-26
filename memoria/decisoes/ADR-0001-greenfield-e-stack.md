# ADR-0001 — Repositório greenfield e stack alvo

- **Estado:** aceito para inicialização
- **Data:** 2026-09-26
- **Decisores:** Squad 3 (stack relatada pelo documentador/dono do projeto)

## Contexto

A Squad 3 migrou para React, Java com API, PostgreSQL, Spring Security e Docker. Existe trabalho prévio em produtos relacionados, com stack e dados distintos.

## Decisão

Criar um repositório de produto separado, iniciar sem código legado e adotar a stack alvo informada pela Squad. O trabalho anterior entra como referência de comportamento, UX, regras e testes de aceitação. Código e dados legados só entram por migração/integracão explicitamente aprovada.

## Consequências

- A implementação da API, segurança e persistência começa limpa em Java/Spring/PostgreSQL.
- A especificação, o backlog e as evidências anteriores reduzem redescoberta e orientam testes de regressão.
- A interface React pode reutilizar conceitos/componentes após revisão de dependências e do contrato novo.
- Os códigos de entidades não serão tratados como intercambiáveis; integração de cursos exige crosswalk confirmado.
- Versão Java, identidade, fontes de dados e deploy continuam pendentes em `../decisoes-abertas.md`.
