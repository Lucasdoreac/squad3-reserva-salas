# Checklist de início — Squad 3

## Produto e negócio

- [ ] Aprovar problema, público e escopo do MVP.
- [ ] Decidir se a reserva exige uma ou duas aprovações.
- [ ] Definir estados da solicitação e quais ocupam a sala.
- [ ] Definir período mínimo/máximo, antecedência, duração e cancelamento.
- [ ] Confirmar timezone, fins de semana, feriados e grade de períodos.
- [ ] Definir quem é solicitante, coordenação, administrador e auditor.
- [ ] Nomear responsável pelo catálogo de salas e calendário acadêmico.

## Reuso e migração

- [ ] Tratar o mockup Reservas + Alocação como referência, não como tela aprovada.
- [ ] Revisar cenários do fluxo local pedido → Coordenação → Reitoria.
- [ ] Copiar para a nova suíte os casos de datas passadas, conflito, autorização, cancelamento e histórico.
- [ ] Identificar fontes de dados e donos de cada fonte.
- [ ] Mapear `COD_DISC` e `Disciplina.id`; nunca juntar só por nome.
- [ ] Separar dados sintéticos dos dados oficiais.
- [ ] Escrever plano de migração, reconciliação, backup e rollback antes de importar dados reais.
- [ ] Definir se grade acadêmica entra no MVP e por qual API autenticada.

## Engenharia

- [ ] Confirmar versão Java LTS e versões suportadas de Node/PostgreSQL.
- [ ] Criar repositório e proteger `main` com review e CI.
- [ ] Configurar React, Spring Boot, Spring Security, PostgreSQL, Flyway e Docker Compose.
- [ ] Definir padrão de DTOs, erros, paginação, timezone e OpenAPI.
- [ ] Implementar constraint/transação que evita dupla reserva concorrente.
- [ ] Configurar testes unitários e de integração contra PostgreSQL.
- [ ] Configurar lint, build de produção, análise de dependências e política de secrets.
- [ ] Definir logs com request ID sem credenciais/dados sensíveis.

## UX e validação

- [ ] Revisar o mockup integrado com uma pessoa solicitante e uma pessoa da Coordenação.
- [ ] Testar o fluxo em tela pequena e com navegação por teclado.
- [ ] Definir rótulos, mensagens de conflito, vazio, carregamento e erro.
- [ ] Validar se os horários em grade devem ser editados por curso/turma ou por sala.
- [ ] Capturar telas finais somente depois de validar fluxos e dados representativos.

## Operação e entrega

- [ ] Definir ambientes local, teste e produção, responsáveis e URL.
- [ ] Definir provedor de identidade e política para criar/desativar usuários.
- [ ] Definir serviço de e-mail e templates de notificação.
- [ ] Documentar variáveis de ambiente sem valores secretos.
- [ ] Definir backup, retenção, restauração e monitoramento.
- [ ] Fazer demonstração do primeiro vertical slice e obter aceite da Coordenação.

## Pronto para iniciar desenvolvimento quando

- [ ] Stack, repo e owner de deploy estão confirmados.
- [ ] As regras de conflito e o primeiro ciclo de estados foram aprovados.
- [ ] Existe catálogo seed sintético com salas identificadas como exemplo.
- [ ] O contrato de `availability` está revisado antes de construir telas dependentes.
- [ ] Histórias S3-01 a S3-06 têm critérios de aceite e dependências visíveis.
