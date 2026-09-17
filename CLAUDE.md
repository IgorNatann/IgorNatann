# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## O que e este repositorio

`IgorNatann/IgorNatann` e um repositorio de **perfil do GitHub**: o unico entregavel escrito a mao e o `README.md`, que o GitHub renderiza na pagina de perfil do usuario. Nao existe aplicacao, gerenciador de pacotes, build, suite de testes nem etapa de lint. "Publicar" significa commitar uma mudanca do README em `main`.

O conteudo e em portugues do Brasil e o posicionamento e Engenharia de Dados (ETL, Data Warehouse, modelagem dimensional, orquestracao).

## Arquitetura: tres partes moveis

1. **`README.md`** - editado a mao. Tudo que e visual vem de URL de imagem externa (badges do shields.io, banners do capsule-render, cards de stats e o SVG da snake). Nada e construido localmente, entao "pre-visualizar" significa ler o Markdown ou publicar e olhar no GitHub.

2. **`.github/workflows/cobrinha.yml`** - roda a cada 12h (`cron: "0 */12 * * *"`) e por `workflow_dispatch`. Faz duas coisas independentes:
   - `vn7n24fzkq/github-profile-summary-cards@release` regenera `profile-summary-card-output/` (65 pastas de tema com SVGs e um README por tema) e **commita de volta na branch em que rodou**, com a mensagem `Generate profile summary cards`.
   - `Platane/snk@v3` gera o SVG da snake de contribuicoes e `crazy-max/ghaction-github-pages@v5` publica na branch **`output`** (`dist/` para a raiz da branch). O README consome esse arquivo de `raw.githubusercontent.com/IgorNatann/IgorNatann/output/github-contribution-grid-snake.svg`.

3. **`profile-summary-card-output/`** - totalmente gerado. Nunca editar a mao; a proxima execucao do workflow sobrescreve tudo.

### Organizacao das branches

- `main` - o conteudo do perfil. Tambem e onde caem os commits de cards do bot.
- `output` - **somente artefato**, guarda o SVG gerado da snake. Nunca fazer merge dela em `main` nem edita-la diretamente.
- Branches de trabalho (`refactor/page`, `feat/atualizacoes_profile`) - alteracoes do README.

O historico e dominado pelos commits `Generate profile summary cards` do bot, entao sempre rode `git pull` antes de comecar e use `git log --pretty="%h %an %s" | rg -v "Generate profile summary cards"` para enxergar o historico realmente autoral.

## Restricoes obrigatorias

- **Manter a animacao snake.** Os dois backlogs listam isso como requisito inegociavel de todo redesign.
- **`README.md` deve permanecer em ASCII puro.** O texto em portugues e escrito sem acentos de proposito (`Sumario`, `analiticos`, `orquestracao`) porque versoes anteriores publicaram mojibake. Valide com `rg -n "[^\x00-\x7F]" README.md` - zero ocorrencias e a condicao de aprovacao. Nao "corrigir" a grafia adicionando acentos. A mesma convencao vale para os demais markdowns escritos a mao, incluindo este arquivo.
- **Nao inventar metricas, resultados ou experiencia.** Cada bullet de projeto precisa estar sustentado pelo que existe de fato no repositorio linkado. Isso esta explicito em `BACKLOG_REDESIGN_PERFIL_V2.md`.
- Os cards de stats apontam de proposito para o mirror `github-readme-stats-one-bice.vercel.app`, e nao para o upstream `github-readme-stats.vercel.app`, que estava aplicando rate limit no perfil. Mantenha o host do mirror ao mexer nessas tags `<img>`.

## Processo de trabalho

`BACKLOG_REDESIGN_PERFIL.md` (V1) e `BACKLOG_REDESIGN_PERFIL_V2.md` (V2) definem o fluxo usado pelo dono do repositorio, e ambos estao marcados como concluidos. Uma nova rodada de mudancas segue o mesmo formato:

1. Executar apenas os itens da etapa atual.
2. Validar os criterios de aceite daquela etapa.
3. Revisar o diff da etapa.
4. Um commit por etapa concluida.
5. Marcar a etapa como concluida no arquivo de backlog.

Nunca iniciar a proxima etapa antes de fechar a anterior. As mensagens de commit seguem Conventional Commits com escopo, em portugues - por exemplo `feat(profile): reforcar narrativa tecnica`, `chore(ci): modernizar workflow mantendo snake`, `docs(profile): fechar auditoria da v2`.

## Comandos de verificacao

Nao ha test runner; a verificacao e o checklist de auditoria dos backlogs:

```powershell
rg -n "[^\x00-\x7F]" README.md      # nao pode retornar nada (checagem de encoding)
rg -n "http|https" README.md        # revisar cada link/host de imagem externo
git diff -- README.md .github/workflows/cobrinha.yml
git status --short
```

Para exercitar o pipeline depois de alterar o workflow, dispare-o manualmente (`workflow_dispatch`) pela aba Actions ou com `gh workflow run cobrinha.yml`, e depois confirme que a branch `output` recebeu um SVG novo e que `profile-summary-card-output/` foi atualizado.
