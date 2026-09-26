# Instruções do repositório — Squad 3

- Escreva documentação e mensagens em português claro; preserve nomes técnicos em inglês quando forem parte da stack.
- Este é um projeto greenfield em React, Java/Spring Boot, PostgreSQL, Spring Security e Docker.
- Trabalhe uma história por vez. Antes de corrigir uma regra, crie um teste que falha sem a correção e confirme a falha; depois implemente e rode a suíte relevante.
- Não exponha senhas, tokens, API keys ou dados pessoais em código, logs, commits, imagens ou exemplos. Use `.env.example` com valores fictícios.
- Nunca deixe autorização apenas no frontend. Teste acesso permitido e negado no backend.
- Disponibilidade visual é informativa; a API e o PostgreSQL devem arbitrar conflitos simultâneos.
- Use migrations versionadas. Não altere esquema manualmente em ambientes compartilhados.
- Código legado de Reservas/Alocação é fonte de requisitos e casos de teste, não dependência do runtime desta aplicação.
- Não migre/importa dados reais sem mapeamento aprovado, cópia de segurança, ensaio de reconciliação e rollback.
- Documente decisões em `memoria/decisoes/` como ADR curto. Separe decisões confirmadas de propostas e pendências.
- Não faça merge, deploy ou publicação externa sem solicitação explícita. A criação inicial deste repositório foi solicitada pelo dono.
