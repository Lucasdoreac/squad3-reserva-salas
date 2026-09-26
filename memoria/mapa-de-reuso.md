# Mapa de reuso — preservar valor, manter o novo produto independente

## Reaproveitar diretamente como conhecimento

| Trabalho anterior | Valor que fica | Ação na stack nova |
|---|---|---|
| Fluxo de pedido, Coordenação e Reitoria | Vocabulário de estados, pontos de decisão e evidências de ponta a ponta. | Confirmar número de aprovações e traduzir para histórias/estados de domínio. |
| Correção de datas e horários passados | Caso real que revela limites da agenda. | Portar como regra com timezone e `Clock` injetável; manter teste de regressão. |
| Bloqueio por aula/oferta | Necessidade de combinar reserva de evento e ocupação recorrente. | Representar ambas como ocupações; usar fonte oficial/versionada se integrada. |
| Protótipo de grade da Alocação | Padrão de grade e experiência de Coordenação. | Tratar como referência UX e contrato candidato, não como calendário real. |
| Testes existentes e cenário E2E | Casos para teste de aceitação e demo. | Reescrever com fixtures limpas para Spring/React/PostgreSQL. |
| Padrões de apresentação e mockup | Hierarquia visual, navegação e componentes de fluxo. | Reusar tokens/ideias de UX; validar acessibilidade e responsividade na nova interface. |

## Reimplementar

- API REST e validação no Spring Boot.
- Autorização com Spring Security; papéis decididos pela squad e verificados no backend.
- Persistência em PostgreSQL com JPA/Flyway e transações.
- Restrição de conflito de intervalos e histórico/auditoria.
- Envio de notificações e configurações seguras.
- Frontend adaptado ao contrato OpenAPI novo.

## Não copiar como está

- Código Flask/Python, MongoEngine ou acesso a bancos de sistemas antigos.
- IDs de curso/disciplina/sala sem crosswalk acordado.
- Seeds e horários sintéticos tratados como calendário oficial.
- Regras implementadas só em JavaScript.
- Estados/status legados sem aprovação do Product Owner.

## Princípio de integração

O PostgreSQL do novo sistema é a única fonte de verdade para reservas durante o MVP. Qualquer fonte acadêmica futura integra via API autenticada e versionada, com chave estável, idempotência, observabilidade e política de indisponibilidade. Não compartilhar conexão ou escrever direto no banco de outro produto.
