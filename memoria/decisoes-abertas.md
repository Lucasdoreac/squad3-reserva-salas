# Decisões abertas

Fechar no alinhamento de produto/arquitetura antes de implementar histórias que dependam delas.

| ID | Pergunta | Sugestão inicial | Quem confirma |
|---|---|---|---|
| D-01 | Aprovação é única ou passa por Coordenação e Reitoria? | Começar com um papel administrativo configurável; não fixar fluxo até ouvir a Coordenação. | Product Owner/Coordenação |
| D-02 | Como os usuários entram e quem cria/desativa contas? | Usar provedor institucional se houver; sem auto cadastro privilegiado. | Coordenação/TI |
| D-03 | Qual Java LTS e versões exatas da stack? | Escolher uma combinação ainda suportada e fixar em CI/Docker. | Tech lead |
| D-04 | Quem fornece salas, campus, capacidade e recursos? | Uma fonte identificada com responsável de atualização. | Coordenação/infra |
| D-05 | Quais estados bloqueiam sala e quando cancelar é permitido? | Definir tabela de transição e exemplos antes de criar a constraint. | Product Owner/Coordenação |
| D-06 | Qual fuso, antecedência e duração máxima? | `America/Sao_Paulo` como hipótese a confirmar; política numérica pendente. | Coordenação |
| D-07 | Calendário acadêmico entra no MVP? | Não, até haver fonte oficial e crosswalk de IDs. | Product Owner/Coordenação |
| D-08 | Onde hospedar e quem mantém CI, secrets, backup e deploy? | Ambientes dev/test/prod separados; nunca credencial no Git. | Dono da organização/infra |
| D-09 | Quais evidências a avaliação da Squad exige? | Testes, screenshots datados, README e demonstração com seed sintética. | Docente/Product Owner |
| D-10 | O protótipo visual representa direção aprovada? | Validar com uma pessoa solicitante e uma da Coordenação. | Product Owner/UX |
