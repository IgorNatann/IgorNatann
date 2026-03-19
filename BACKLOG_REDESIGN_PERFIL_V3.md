# Backlog V3 - Perfil GitHub (Consolidacao de Posicionamento)

## Objetivo da V3
Consolidar o perfil como vitrine tecnica para tech recruiters e profissionais de engenharia de dados, mantendo descoberta organica e networking tecnico, sem sinalizacao explicita de busca de vaga.

## Diretrizes obrigatorias
- Manter a animacao `snake` no README.
- Nao inserir "open to work", "buscando vagas" ou equivalente.
- Nao inventar metricas, resultados ou experiencia nao sustentados por repositorios.
- Executar uma etapa por vez, com auditoria e commit de conclusao.

## Fluxo por etapa (auditoria + commit)
1. Executar apenas os itens da etapa.
2. Validar criterios de aceite da etapa.
3. Revisar o diff da etapa.
4. Fazer 1 commit de conclusao da etapa.
5. Marcar a etapa como concluida neste backlog.

## Quadro de status
- Etapa atual: `Etapa 1 - Narrativa de alto impacto (sem sinalizacao de vaga)`
- Regra: nao iniciar a proxima etapa sem fechar a anterior.
- Evidencia minima por etapa: diff revisado + checklist de auditoria validado.

## Etapas

- [x] Etapa 0 - Planejamento V3
Entregaveis:
- Criar backlog V3 versionado.
- Definir criterio de sucesso para recruiters + techs + organico.

Criterios de aceite:
- Escopo da V3 claro e sem conflito com V1/V2.
- Etapas com criterios de aceite e commit sugerido.

Commit sugerido:
`chore(profile): criar backlog da v3 para consolidacao de posicionamento`

- [ ] Etapa 1 - Narrativa de alto impacto (sem sinalizacao de vaga)
Entregaveis:
- Ajustar narrativa inicial para reforcar proposta de valor tecnico e contexto de negocio.
- Manter tom de autoridade tecnica e networking.

Criterios de aceite:
- Leitura inicial comunica valor em menos de 10 segundos.
- Sem frases de busca explicita por oportunidade.

Commit sugerido:
`feat(profile): refinar narrativa de alto impacto para vitrine tecnica`

- [ ] Etapa 2 - Curadoria de projetos flagship
Entregaveis:
- Destacar 3 projetos flagship no topo da secao de projetos.
- Manter padrao de prova: contexto, stack, evidencias.

Criterios de aceite:
- Projetos mais relevantes ficam visiveis primeiro.
- Estrutura consistente e escaneavel.

Commit sugerido:
`feat(profile): curar projetos flagship com foco em impacto tecnico`

- [ ] Etapa 3 - Evidencias tecnicas de maturidade
Entregaveis:
- Adicionar sinais de maturidade tecnica no README (qualidade, confiabilidade, operacao, arquitetura).
- Reforcar linguagem de ownership tecnico.

Criterios de aceite:
- Perfil demonstra profundidade tecnica alem de stack.
- Texto evita generalidades.

Commit sugerido:
`feat(profile): explicitar evidencias de maturidade tecnica`

- [ ] Etapa 4 - Consistencia com repositorios-chave
Entregaveis:
- Ajustar links/descricoes para alinhar README principal com repositorios de destaque.
- Adicionar referencia curta para repositorios-chave (se necessario).

Criterios de aceite:
- Narrativa do perfil bate com conteudo tecnico dos repositorios.
- Sem links quebrados.

Commit sugerido:
`refactor(profile): alinhar vitrine principal com repositorios chave`

- [ ] Etapa 5 - CTA de networking tecnico
Entregaveis:
- Refinar bloco de contato para networking tecnico (troca tecnica, colaboracao, comunidade).
- Manter linguagem profissional e discreta.

Criterios de aceite:
- CTA incentiva conexao tecnica sem parecer busca ativa de vaga.
- Contatos continuam diretos e funcionais.

Commit sugerido:
`feat(profile): otimizar call to action para networking tecnico`

- [ ] Etapa 6 - Auditoria final V3
Entregaveis:
- Revisao final de narrativa, links, consistencia tecnica e legibilidade.
- Fechar checklist e marcar V3 concluida.

Criterios de aceite:
- Posicionamento forte para recruiter e tech community.
- Sem contradicao com diretriz de perfil organico.
- `snake` preservada.

Commit sugerido:
`docs(profile): fechar auditoria da v3 e validar prontidao`

## Checklist rapido de auditoria por etapa
- [ ] Sem sinais de mojibake em `README.md`.
- [ ] Links principais abrindo corretamente.
- [ ] Narrativa alinhada a Engenharia de Dados e networking tecnico.
- [ ] Mudancas da etapa isoladas no commit.

## Comandos uteis para auditoria
- `git diff -- README.md BACKLOG_REDESIGN_PERFIL_V3.md .github/workflows/cobrinha.yml`
- `rg -n "[^\\x00-\\x7F]" README.md`
- `rg -n "http|https" README.md`
- `git status --short`
