# Estado inicial — memória greenfield

**Inicializado:** 2026-09-26  
**Fonte:** pedido do documentador e contexto de início fornecido para a Squad 3.

## Confirmado

- Projeto: **Squad 3 — Sistema de reserva de salas**.
- Papel informado: Lucas Dórea (ludoc), documentador.
- Objetivo mínimo: autenticar, consultar disponibilidade, solicitar e cancelar reserva e acompanhar administrativamente.
- Stack alvo informada após migração da Squad: React, Java com API, PostgreSQL, Spring Security, Docker e GitHub.
- Este repositório nasce greenfield; o código existente de Reservas/Alocação não está sendo copiado para cá.

## Referências de conhecimento (não são dependências)

O LabTech já contém protótipos e implementações que podem orientar requisitos, UX e testes. A nova aplicação precisa recompilar essas decisões na stack alvo e confirmar cada comportamento com a Squad. Nenhum dado local representa automaticamente o ambiente oficial.

- Reservas: ciclo de pedido/aprovação, agenda, histórico, regra de data passada e prevenção de conflitos.
- Alocação: navegação de Coordenação e protótipo de grade semanal por curso/semestre.
- Mockup integrado: direção visual para uma experiência coesa, sujeito a validação de usuário.

## Limites deste estado

- Não há ainda decisão confirmada sobre provedor de identidade, papéis exatos, etapas de aprovação, catálogo oficial, calendário oficial, hospedagem ou Java LTS.
- `COD_DISC` (catálogo legado) e `Disciplina.id` (banco da Alocação) não são identificadores equivalentes confirmados.
- A grade experimental não é fonte oficial de horários.
- O pacote documental é uma proposta inicial; o Product Owner e a Coordenação ainda precisam aprovar regras e aceite.
- Não há dados reais, credenciais ou configuração de produção neste repositório.
