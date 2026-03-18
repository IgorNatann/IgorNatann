# Backlog V1 - Perfil GitHub (Engenharia de Dados)

## Objetivo da V1
Reposicionar o perfil para Engenharia de Dados, destacando projetos reais do repositorio, com narrativa tecnica clara e visual mais limpo.

## Diretriz obrigatoria
Manter a animacao `snake` no README.

## Fluxo por etapa (auditoria + commit)
1. Executar apenas os itens da etapa.
2. Validar criterios de aceite da etapa.
3. Revisar o diff da etapa.
4. Fazer 1 commit de conclusao da etapa.
5. Marcar a etapa como concluida neste backlog.

## Quadro de status
- Etapa atual: `V1 concluida`
- Regra: nao iniciar a proxima etapa sem fechar a anterior.
- Evidencia minima por etapa: diff revisado + checklist de auditoria validado.

## Etapas

- [x] Etapa 0 - Baseline e Planejamento
Entregaveis:
- Criar backlog versionado no repositorio.
- Definir lista de projetos que suportam o posicionamento em Engenharia de Dados.

Criterios de aceite:
- Backlog presente e legivel.
- Lista inicial de projetos definida: `project_e_commerce_dw`, `projeto_etl_consolidacao_vendas`, `project_dw_ataca_dez`, `projeto_dados_dbt`, `airflow_orchestration` ou `project_analytics_warehouse_platform`.

Commit sugerido:
`chore(profile): criar backlog de redesign e baseline da V1`

- [x] Etapa 1 - Hero e Posicionamento
Entregaveis:
- Reescrever topo do README com headline de Engenharia de Dados.
- Ajustar resumo profissional para foco em ETL, DW, orquestracao e qualidade.

Criterios de aceite:
- Primeiras secoes comunicam posicionamento em ate 10 segundos de leitura.
- Texto das secoes iniciais sem erros de encoding.

Commit sugerido:
`feat(profile): atualizar hero e posicionamento para engenharia de dados`

- [x] Etapa 2 - Projetos em Destaque (Data Engineering)
Entregaveis:
- Substituir bloco de projetos atuais por projetos de dados.
- Para cada projeto, incluir: problema, stack principal e link.

Criterios de aceite:
- Minimo de 4 projetos de dados destacados.
- Cada projeto com contexto tecnico curto e objetivo.
- Links clicaveis e corretos.

Commit sugerido:
`feat(profile): destacar projetos de engenharia de dados com contexto tecnico`

- [x] Etapa 3 - Stack e Trilhas de Estudo
Entregaveis:
- Reorganizar skills em blocos coerentes (Linguagens, Dados, Orquestracao, Cloud/DevOps).
- Revisar secao de estudos atuais para ficar aderente ao posicionamento.

Criterios de aceite:
- Menos ruido visual (sem badges redundantes).
- Stack principal e stack em estudo claramente separadas.

Commit sugerido:
`refactor(profile): reorganizar stack principal e trilha de estudos`

- [x] Etapa 4 - Visual e Qualidade de Conteudo
Entregaveis:
- Simplificar layout geral do README.
- Corrigir erros textuais e padronizar linguagem.

Criterios de aceite:
- Sem caracteres quebrados (ex.: sequencias de mojibake no texto).
- Sem erros de escrita evidentes.
- Leitura fluida no desktop e mobile do GitHub.

Commit sugerido:
`fix(profile): padronizar texto, encoding e legibilidade do README`

- [x] Etapa 5 - Workflow (Snake + Modernizacao)
Entregaveis:
- Manter geracao da `snake`.
- Atualizar actions para versoes mais atuais/estaveis.
- Preservar geracao de cards do summary.

Criterios de aceite:
- Workflow executa manualmente sem falhas.
- Branch `output` segue recebendo o SVG da snake.

Commit sugerido:
`chore(ci): modernizar workflow mantendo snake e summary cards`

- [x] Etapa 6 - Auditoria Final V1
Entregaveis:
- Revisao final de links, secoes e consistencia do posicionamento.
- Checklist final de pronto para merge/publicacao.

Criterios de aceite:
- Posicionamento em Engenharia de Dados evidente em todo o README.
- Projetos destacados refletem o conteudo real do GitHub.
- Sem regressao na `snake`.

Commit sugerido:
`docs(profile): fechar auditoria da v1 e validar pronto para publicacao`

## Checklist rapido de auditoria por etapa
- [x] Sem caracteres quebrados em `README.md`.
- [x] Links dos projetos abrindo corretamente.
- [x] Texto alinhado ao posicionamento de Engenharia de Dados.
- [x] Mudancas da etapa isoladas no commit.

## Comandos uteis para auditoria
- `git diff -- README.md .github/workflows/cobrinha.yml BACKLOG_REDESIGN_PERFIL.md`
- `rg -n "Ã.|â.|ð.|�" README.md`
- `rg -n "http|https" README.md`
- `git status --short`
