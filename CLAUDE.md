# CLAUDE.md

Orientações para o Claude Code (e agentes) ao trabalhar neste repositório.

## Descrição do projeto

**studylog** (repositório remoto: `lista-de-estudos`) é o repositório pessoal de
**logs de estudo de programação** do Gabriel Bursi. Não é um projeto de software com
código executável — é uma base de conhecimento em Markdown que organiza, documenta e
rastreia o progresso do aprendizado em desenvolvimento: cursos, livros, artigos,
roadmaps, playlists do YouTube e projetos pessoais.

O conteúdo é todo em **português (pt-BR)**. O objetivo de cada arquivo é registrar o
que está sendo estudado, com links para o material original e indicadores visuais de
progresso.

## Estrutura

Cada pasta agrupa um tipo de material de estudo; cada arquivo `.md` é um log
independente de um curso, trilha ou tema.

```
.
├── README.md              # Índice geral com links para todos os logs
├── artigos/               # Anotações de artigos técnicos (DDD, design de banco, padrões…)
├── cursos-pagos/          # Logs de cursos pagos (JStack, branas.io, Coffstack/PRN, Udemy)
├── projetos-pessoais/     # Specs/logs de projetos próprios (UI Kit, Connect Flow, Jiraya…)
├── roadmaps/              # Trilhas de carreira (Frontend, Backend, Mobile, Fullstack, Fundamentos)
└── youtube-playlists/     # Coleções de playlists por tema (React, AWS, Kafka, Docker…)
```

> A pasta `/livros` aparece como seção no `README.md`, mas é apenas uma lista de
> referências (sem pasta no disco).

## Convenções

Ao criar ou editar logs, siga os padrões já existentes no repositório:

- **Idioma:** sempre português (pt-BR).
- **Badges de progresso:** use `geps.dev` para barras de porcentagem —
  `![](https://geps.dev/progress/NN)` onde `NN` vai de 0 a 100.
- **Status por emoji:** o significado é definido no topo da seção do `README.md`.
  - Livros: ✅ Finalizado · 📖 Estou lendo · 📚 Ainda não iniciado
  - Projetos: ✅ Concluído · 👷 Trabalho em progresso · 🚫 Ainda não iniciado
- **Links internos âncora:** os logs maiores (ex.: `JSTACK.md`) usam um *Sumário* com
  links absolutos para âncoras no GitHub
  (`https://github.com/GabrielBursi/studylog/blob/main/<caminho>#<ancora>`). Mantenha
  esse padrão ao adicionar seções.
- **Nomes de arquivo:** `MAIUSCULAS-COM-HIFEN.md`.
- **Títulos:** o primeiro heading costuma ser um link para o material original
  (curso, playlist, artigo).

## Instruções para o Claude

- **Edite o conteúdo, não invente progresso.** Só atualize badges/emojis de status
  quando o Gabriel indicar o avanço. Não estime porcentagens por conta própria.
- **Preserve os links.** Ao reorganizar um arquivo, mantenha as URLs e âncoras
  funcionando; atualize o *Sumário* correspondente.
- **Mantenha o `README.md` sincronizado.** Ao adicionar um novo log, inclua o link na
  seção apropriada do `README.md`.
- **Respeite o estilo conciso e em pt-BR** já presente nos arquivos.
- **Sem build/teste.** Não há toolchain, dependências, lint ou CI — não tente rodar
  `npm`, `make`, etc. O "produto" é a documentação.

## Git

- Branch principal: `main`. Remoto: `origin`
  (`https://github.com/GabrielBursi/lista-de-estudos.git`).
- Mensagens de commit seguem o padrão simples do histórico:
  `Update <ARQUIVO>.md` para edições, ou uma frase curta descrevendo a mudança.
- Commits podem ser feitos diretamente na `main`.

## Skills disponíveis

Este projeto contém uma skill de projeto para auxiliar na organização dos arquivos:

- **`.claude/skills/studylog-organizer/`** — Guia de formatação e organização dos arquivos MD.
  Use antes de adicionar ou reformatar qualquer conteúdo no repositório. Cobre as regras
  de separação de links/itens para cada tipo de pasta (`cursos-pagos/`, `youtube-playlists/`,
  `roadmaps/`, `artigos/`, `projetos-pessoais/`).
