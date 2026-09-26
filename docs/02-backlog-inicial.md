# Backlog inicial — Squad 3

Backlog provisório derivado do documento-base. P0 = necessário para demonstrar o MVP; P1 = necessário antes de piloto real; P2 = evolução. Estimativas ficam com a squad após quebrar as histórias.

| ID | Prioridade | História | Critério de aceite resumido | Dependência |
|---|---|---|---|---|
| S3-01 | P0 | Como equipe, quero iniciar frontend, API Java, PostgreSQL e Compose para desenvolver de forma reproduzível. | Um comando sobe os serviços; health checks passam; banco vazio recebe Flyway; CI executa build e testes. | Java alvo, versões e repo definidos. |
| S3-02 | P0 | Como usuário autorizado, quero entrar e receber somente as permissões do meu papel. | Login válido; inválido recusado; rota admin negada a solicitante; ninguém se cadastra como admin sem autorização. | Provedor/modelo de identidade e papel aprovados. |
| S3-03 | P0 | Como solicitante, quero filtrar salas por campus, capacidade e recursos. | Filtros combináveis; sala inativa não aparece; tela distingue vazio, erro e carregamento. | Fonte e responsável pelo catálogo. |
| S3-04 | P0 | Como solicitante, quero consultar disponibilidade por data e intervalo. | Exibe intervalo ocupado e sala; intervalos adjacentes são permitidos; timezone documentado. | Regra temporal e bloqueios definidos. |
| S3-05 | P0 | Como solicitante, quero pedir uma sala para uma finalidade e horário. | Valida campos e período; cria estado inicial; devolve identificador; pedido fica na lista do autor. | Estados e campos obrigatórios aprovados. |
| S3-06 | P0 | Como sistema, quero recusar sobreposição mesmo em requisições simultâneas. | Teste concorrente comprova que no máximo uma transação ativa ocupa sala/intervalo; API retorna conflito explicável. | Estratégia de constraint/transação aprovada. |
| S3-07 | P0 | Como solicitante, quero acompanhar meus pedidos e seu histórico. | Lista paginada; mostra estado atual, sala e período; histórico registra mudanças sem expor pedidos de terceiros. | Modelo de histórico e políticas de acesso. |
| S3-08 | P0 | Como solicitante, quero cancelar um pedido dentro da política permitida. | Cancelamento autorizado para próprio pedido; estados não canceláveis retornam erro claro; histórico atualizado. | Prazo/estados canceláveis aprovados. |
| S3-09 | P0 | Como coordenação/admin, quero revisar a fila e decidir um pedido. | Filtros por estado/período; aprovar/rejeitar conforme papel; cada ação grava ator, instante e nota. | Quantidade e ordem de aprovações. |
| S3-10 | P1 | Como sistema, quero notificar pessoas sobre decisões. | E-mail de teste enviado; falha não perde atualização; retentativa/erro é observável sem segredo no log. | Provedor, remetente e templates definidos. |
| S3-11 | P1 | Como administrador, quero manter salas, recursos e bloqueios. | CRUD protegido; bloqueio aparece na busca; alterações relevantes são auditadas. | Responsável e regra do catálogo. |
| S3-12 | P1 | Como coordenação, quero consultar horários acadêmicos como bloqueios de salas. | Grade importada/consultada por contrato versionado; sala/curso/tempo mapeados sem inferência textual; indisponibilidade fica clara. | Fonte oficial, crosswalk de códigos e contrato de integração. |
| S3-13 | P1 | Como equipe, quero importar dados legados com rastreabilidade. | Dry run; mapping table; contagem origem/destino; relatório de inválidos; repetição idempotente; rollback ensaiado. | Decisão formal de migração e acesso aos dados. |
| S3-14 | P1 | Como equipe, quero observar e restaurar a aplicação. | Logs com request ID; métricas/health; backup restore demonstrado; secrets documentados. | Hospedagem e responsáveis operacionais. |
| S3-15 | P2 | Como administrador, quero exportar agenda e relatórios. | Exportação respeita filtro e permissões; CSV/PDF aceito pela Coordenação. | Formato e necessidade confirmados. |

## Primeiro vertical slice

Priorizar nesta ordem: S3-01 → S3-02 → S3-03 → S3-04 → S3-05 → S3-06 → S3-09. O slice deve terminar com uma reserva auditada e conflito recusado no PostgreSQL. Isso prova a stack e a regra mais importante sem tentar portar os sistemas inteiros.

## Evidências para cada história

Anexar ao cartão: decisão/requisito relacionado, teste automatizado (incluindo o caso que falhava antes quando for correção), resultado de CI, captura da tela relevante e nota de mudança de deploy quando houver schema/configuração.
