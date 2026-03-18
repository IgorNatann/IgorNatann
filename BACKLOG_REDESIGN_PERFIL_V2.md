# Backlog V2 - Perfil GitHub (Engenharia de Dados)

## Objetivo da V2
Refinar o perfil para aumentar clareza, autoridade tecnica e legibilidade, mantendo o posicionamento em Engenharia de Dados validado na V1.

## Diretrizes obrigatorias
- Manter a animacao `snake` no README.
- Nao inventar metricas, resultados ou experiencias que nao estejam sustentadas pelos repositorios.
- Seguir fluxo por etapa com auditoria e 1 commit por conclusao de etapa.

## Fluxo por etapa (auditoria + commit)
1. Executar apenas os itens da etapa.
2. Validar criterios de aceite da etapa.
3. Revisar o diff da etapa.
4. Fazer 1 commit de conclusao da etapa.
5. Marcar a etapa como concluida neste backlog.

## Quadro de status
- Etapa atual: `Etapa 0 - Planejamento V2`
- Regra: nao iniciar a proxima etapa sem fechar a anterior.
- Evidencia minima por etapa: diff revisado + checklist de auditoria validado.

## Etapas

- [ ] Etapa 0 - Planejamento V2
Entregaveis:
- Criar backlog V2 versionado.
- Definir foco da V2: autoridade tecnica + narrativa de impacto + legibilidade.

Criterios de aceite:
- Escopo da V2 claro e sem sobreposicao com V1.
- Backlog com etapas, criterios de aceite e commits sugeridos.

Commit sugerido:
`chore(profile): criar backlog da v2 com plano de refinamento`

- [ ] Etapa 1 - Reforco de narrativa tecnica
Entregaveis:
- Ajustar headline e resumo para comunicar valor tecnico e tipo de problema resolvido.
- Incluir um bloco curto "Como gero valor com dados".

Criterios de aceite:
- Leitura inicial comunica posicionamento e proposta de valor em menos de 10 segundos.
- Texto objetivo, sem termos genericos excessivos.

Commit sugerido:
`feat(profile): reforcar narrativa tecnica e proposta de valor`

- [ ] Etapa 2 - Projetos com prova de escopo
Entregaveis:
- Evoluir secao de projetos para formato mais auditavel (contexto do problema + stack + evidencia de escopo).
- Padronizar estrutura de cada item.

Criterios de aceite:
- Minimo de 4 projetos mantidos.
- Todos os itens com formato consistente.
- Nenhum projeto com descricao vaga.

Commit sugerido:
`feat(profile): padronizar projetos com evidencia tecnica de escopo`

- [ ] Etapa 3 - Hierarquia visual e escaneabilidade
Entregaveis:
- Melhorar hierarquia entre secoes (titulos, espacamento, ordem de leitura).
- Reduzir blocos longos e priorizar listas objetivas.

Criterios de aceite:
- Leitura escaneavel em desktop e mobile.
- Secoes principais claramente separadas.

Commit sugerido:
`refactor(profile): melhorar hierarquia visual e escaneabilidade`

- [ ] Etapa 4 - Credibilidade e atualizacao
Entregaveis:
- Adicionar bloco "Foco atual" ou "Roadmap tecnico" com trilhas reais de estudo.
- Revisar stack principal vs em evolucao para evitar redundancia.

Criterios de aceite:
- Conteudo mostra direcao tecnica de curto prazo.
- Sem contradicao entre stack principal e estudo.

Commit sugerido:
`feat(profile): adicionar foco tecnico atual e alinhar trilhas`

- [ ] Etapa 5 - Automacao e consistencia do README
Entregaveis:
- Revisar workflow e referencias dinamicas para garantir consistencia da V2.
- Confirmar manutencao da `snake` e dos cards de stats.

Criterios de aceite:
- Workflow permanece funcional.
- README sem links quebrados e sem regressao visual.

Commit sugerido:
`chore(ci): validar automacao e consistencia da v2`

- [ ] Etapa 6 - Auditoria final V2
Entregaveis:
- Revisao final de texto, links, consistencia de narrativa e qualidade visual.
- Checklist final de pronto para publicacao.

Criterios de aceite:
- Posicionamento em Engenharia de Dados forte e coerente.
- Projetos com evidencias tecnicas claras.
- `snake` preservada.

Commit sugerido:
`docs(profile): fechar auditoria da v2 e validar publicacao`

## Checklist rapido de auditoria por etapa
- [ ] Sem sinais de mojibake em `README.md`.
- [ ] Links de projetos e contato abrindo corretamente.
- [ ] Narrativa alinhada a Engenharia de Dados.
- [ ] Mudancas da etapa isoladas no commit.

## Comandos uteis para auditoria
- `git diff -- README.md .github/workflows/cobrinha.yml BACKLOG_REDESIGN_PERFIL_V2.md`
- `rg -n "[^\\x00-\\x7F]" README.md`
- `rg -n "http|https" README.md`
- `git status --short`
