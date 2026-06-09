---
name: studylog-organizer
description: Organiza e formata o conteúdo de arquivos MD do studylog, separando links e itens de forma clara e legível. Use esta skill sempre que o usuário quiser: adicionar um novo curso, playlist, artigo, livro ou roadmap ao studylog; reformatar seções de um arquivo existente para melhorar a separação entre links e itens; expandir listas com múltiplos links inline em sub-itens separados; verificar se um arquivo segue as convenções do projeto; ou ao mencionar "studylog", "log de estudos", "adicionar curso", "atualizar progresso", "formatar arquivo", "separar links", "organizar itens", "deixar mais legível". Sempre use esta skill antes de editar qualquer arquivo do studylog.
---

# Studylog Organizer

Esta skill orienta como organizar e formatar arquivos MD do studylog de forma consistente, com cada link e item bem separado para facilitar leitura e manutenção.

## Problema a resolver

Arquivos do studylog acumulam listas com muitos links inline em uma mesma linha, tornando o conteúdo difícil de ler. O objetivo é manter cada item/link em sua própria linha, com hierarquia visual clara.

**Exemplo problemático** (tudo numa linha, difícil de ler):
```md
- [ ] [Refresh tokens e RBAC](https://github.com/...) ([#006](url "Autenticação JWT"), [#007](url "RBAC"), [#015](url "Refresh Tokens"))
```

**Exemplo organizado** (um link por linha, hierarquia clara):
```md
- [ ] [Refresh tokens e RBAC](https://github.com/...)
  - [#006 - Autenticação JWT em APIs Node.js](url)
  - [#007 - Autorização baseada em Cargos (RBAC)](url)
  - [#015 - Implementando Refresh Tokens em APIs Node.js](url)
```

## Regras de formatação por tipo de arquivo

### cursos-pagos/

Estrutura esperada de cada arquivo:

```md
# [Nome do Curso](url-do-curso)

Descrição breve do curso.

## Seção Principal

### Subseção (opcional)

* Item com badge ![](https://geps.dev/progress/NN)

## Praticar

- [ ] [Título do exercício](url-do-projeto)
  - [#NNN - Nome do módulo](url-do-modulo)
  - [#NNN - Nome do módulo](url-do-modulo)

## *Sumário*

- **[Categoria](âncora-github)**
    - [Subcategoria](âncora-github)

## Nome da Seção de Conteúdo

* ⭐ [#NNN - Título](url) ![](https://geps.dev/progress/NN)
* [#NNN - Título](url) ![](https://geps.dev/progress/NN)
```

**Regras específicas:**
- Cada módulo/aula: um item `*` por linha, badge no final da mesma linha
- Seção "Praticar": cada referência de curso vai em sub-item `-` indentado com 2 espaços
- Links âncora no Sumário: sempre absolutos (`https://github.com/GabrielBursi/studylog/blob/main/...#ancora`)

### youtube-playlists/

Estrutura esperada:

```md
## Tema

* [Nome da Playlist](url-youtube)
* [Nome da Playlist](url-youtube)
  * [Sub-playlist ou vídeo avulso](url-youtube)
```

**Regras específicas:**
- Uma playlist por linha
- Vídeos avulsos dentro de um tema: sub-item `*` com 2 espaços de indentação
- Seções separadas por linha em branco antes e depois do `##`

### roadmaps/

Estrutura esperada:

```md
# Título do Roadmap

* [Nome do Roadmap](url) ![](https://geps.dev/progress/NN)

---

## Categoria Adicional (se houver)

* [Item](url) ![](https://geps.dev/progress/NN)
```

**Regras específicas:**
- Badge de progresso sempre na mesma linha do link
- Um item por linha

### artigos/

Estrutura esperada:

```md
## Tema

* [Título do Artigo](url)
* [Título do Artigo](url)
```

**Regras específicas:**
- Um artigo por linha
- Seções agrupadas por tema com `##`

### projetos-pessoais/

Usa emoji de status:
- ✅ Concluído
- 👷 Trabalho em progresso
- 🚫 Ainda não iniciado

Formato:
```md
# [Nome do Projeto](url-do-repo)

Status: 👷

Descrição breve.

## Tecnologias

## Funcionalidades

- [ ] Feature 1
- [x] Feature 2
```

---

## Como adicionar novo conteúdo

### 1. Novo curso (cursos-pagos/)

Ao adicionar um curso novo:
1. Crie `cursos-pagos/NOME-DO-CURSO.md` com `progress/0` em todos os badges
2. Adicione link no `README.md` na seção `/cursos-pagos`
3. Use a estrutura de `cursos-pagos/` acima como base

### 2. Nova playlist (youtube-playlists/)

Ao adicionar playlists a um arquivo existente:
- Coloque na seção temática correta, uma por linha
- Se o tema não existe ainda, crie novo `## Tema` separado por linha em branco

### 3. Novo livro (README.md)

Na seção `/livros` do README, adicione com o emoji correto:
```md
* 📚 [Título do Livro](url-amazon)
```

### 4. Novo roadmap (roadmaps/)

Adicione uma linha com badge `progress/0`:
```md
* [Nome](url-roadmap) ![](https://geps.dev/progress/0)
```

---

## Separação visual obrigatória

Sempre aplique linha em branco:
- Entre seções `##`
- Entre grupos de itens com contextos diferentes dentro da mesma seção
- Entre o título do arquivo e a primeira seção

Não aplique linha em branco:
- Entre itens consecutivos de uma mesma lista (`*` ou `-`)
- Entre um título `###` e seus itens imediatos

---

## Reformatando conteúdo existente

Ao reformatar um arquivo:
1. Leia o arquivo completo primeiro
2. Identifique itens com múltiplos links inline (padrão `([#NNN](url), [#NNN](url), ...)`)
3. Expanda cada referência para seu próprio sub-item indentado com 2 espaços
4. Mantenha o título do item principal na linha do checkbox
5. Preserve todos os URLs exatamente como estão
6. Atualize o Sumário se seções foram renomeadas ou adicionadas
7. Mantenha badges e emojis de status inalterados — só o Gabriel decide sobre progresso
