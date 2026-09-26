# Memória de projeto (inicializada limpa)

Esta pasta mantém o contexto pequeno, verificável e próprio da Squad 3. Ela não é um dump do histórico de conversas nem uma cópia de memórias de outros produtos.

## Ordem de confiança

1. Decisão aprovada pela Squad/Coordenação e registrada em ADR.
2. Requisito e regra atual em `docs/01-documento-base.md`.
3. Contexto verificado nesta pasta.
4. Proposta ainda pendente, sempre rotulada como proposta.
5. Código legado: referência histórica, nunca fonte automática de verdade.

## Arquivos

- [`estado-inicial.md`](estado-inicial.md): escopo, stack, fatos e limites conhecidos na criação do repo.
- [`mapa-de-reuso.md`](mapa-de-reuso.md): o que aproveitar do trabalho anterior e como fazê-lo sem acoplamento.
- [`decisoes-abertas.md`](decisoes-abertas.md): perguntas que a Squad precisa fechar.
- [`decisoes/`](decisoes/): ADRs curtos e datados; não reescrever uma decisão aprovada sem registrar novo ADR.

## Como atualizar

- Anote data, fonte e status (`confirmado`, `proposto`, `pendente`) para cada fato relevante.
- Não registre credenciais, tokens, cookies, e-mails pessoais não necessários ou dados reais de usuários.
- Não promova amostras locais a dados oficiais.
- Apague uma hipótese da memória quando ela for refutada; preserve no ADR se tiver impacto em decisão já tomada.
