# no style, please

A (nearly) no-CSS, fast, minimalist [Hugo](https://gohugo.io/) theme inspired
by [riggraz/no-style-please](https://github.com/riggraz/no-style-please).

## Como utilizar

### Configurando o tema

As configurações do tema podem ser encontradas no arquivo
`themes/unstyled/hugo.toml`:

- `appearance`: define se o tema vai estar no modo `dark`, `light` ou `auto`.
- `backHomeText`: o texto a ser exibido no link que redireciona para a home.
- `dateFormat`: o [formato da data](https://pkg.go.dev/time#pkg-constants)
  a ser utilizado.
- `listGroupByDate`: agrupar os posts por data (ano) na pagina de todos os posts.
- `showFooter`: exibe o rodapé.
- `footerCopyright`: texto para ser exibido ao lado do copyright no rodapé.

### Configurando o menu

Para alterar os itens que aparecem no menu principal, você precisa editar
o arquivo `themes/unstyled/data/menu.toml`.

O arquivo `menu.toml` aceita os seguintes campos:

- `entries`: define uma lista não ordenada que contem os itens do menu.
  - `title` (string): define o texto a ser exibido para o item.
  - `url` (string): se definida o titulo vai ser renderizado como um link
    apontando
    para a url especificada.
  - `newTab` (boolean): se definido como `true` abre a url especificada em uma
    nova aba.
  - `post_list` (boolean | object): se definido como `tue` irá listar todos os
    posts dentro do diretório `content/posts` como subitens, se você quiser
    customizar quais e como os itens serão listados utilize os campos abaixo:
    - `section` (string): pode ser utilizado para definir de qual diretório
      dentro de `content/` os posts serão listados.
    - `limit` (integer): especifica o número máximo de posts a serem exibidos.
    - `showMore` (boolean): se definido como `true` e o número de posts for
      maior do que o limite estabelecido, exibi um link para a página com
      todos os posts.
    - `showMoreText` (string): especifica o texto a ser exibido caso `showMore`
      seja `true`.
    - `showMoreUrl` (string): especifica a url utilizada caso `showMore` seja
      `true`.
  - `entries`: você também pode ter `entries` dentro de outras `entries`.

#### Exemplos

Um item de menu com alguns subitens:

```toml
[[entries]]
title = "Info"

[[entries.entries]]
title = "A (nearly) no-CSS, fast, minimalist Hugo theme ported from <a target='_blank' href='https://github.com/riggraz/no-style-please'>riggraz/no-style-please</a>."

[[entries.entries]]
title = "Codeberg"
url = "https://codeberg.org/d33trik/unstyled"
newTab = true

[[entries.entries]]
title = "RSS"
url = "index.xml"
```

```markdown
- Info
  - A (nearly) no-CSS, fast, minimalist Hugo theme ported from [riggraz/no-style-please](https://github.com/riggraz/no-style-please).
  - [Codeberg](https://codeberg.org/d33trik/unstyled)
  - [RSS](index.xml)
```

Listando posts de seções diferentes:

```markdown
content/
├── posts/
│ ├── a-new-experimental-go-api-for-json.md
│ ├── testing-time-and-other-asynchronicities.md
│ ├── container-aware-gomaxprocs.md
│ ├── go-1-25-is-released.md
│ ├── the-fips-140-3-go-cryptographic-module.md
│ ├── on-no-syntactic-support-for-error-handling.md
│ ├── generic-interfaces.md
├── haikus/
│ └── the-old-pond.md
│ └── a-world-of-dew.md
│ └── lighting-one-candle.md
│ └── a-poppy-blooms.md
│ └── over-the-wintry.md
│ └── in-a-station-of-the-metro.md
│ └── the-taste-of-rain.md
```

```toml
[[entries]]
title = "Posts"

[entries.post_list]
section = "posts"
limit = 5
showMore = true
showMoreUrl = "posts"
showMoreText = "See more posts..."

[[entries]]
title = "Haikus"

[entries.post_list]
section = "haikus"
limit = 5
showMore = true
showMoreUrl = "haikus"
showMoreText = "See more haikus..."
```

```markdown
- posts
  - 2025-09-09 A new experimental Go API for JSON
  - 2025-08-26 Testing Time (and other asynchronicities)
  - 2025-08-20 Container-aware GOMAXPROCS
  - 2025-08-12 Go 1.25 is released
  - 2025-07-15 The FIPS 140-3 Go Cryptographic Module
  - See more posts...

- haikus
  - 2025-09-11 The Old Pond
  - 2025-09-03 A World of Dew
  - 2025-08-17 Lighting One Candle
  - 2025-08-02 A Poppy Blooms
  - 2025-07-21 Over the Wintry
  - See more haikus...
```

Um item do menu com vários leveis de subitens:

```toml
[[entries]]
title = "List"

[[entries.entries]]
title = "With subitems"

[[entries.entries.entries]]
title = "With subsubitems"
```

```markdown
- List
  - With subitems
    - With subsubitems
```
