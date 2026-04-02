---
title: "Markdown Syntax"
draft: false
---

Below are some examples of how the theme renders the main markdown components.
To learn how to use them, you can see this file at
`themes/unstyled/content/markdown-syntax.md` or you can visit the website
[https://www.markdownguide.org/](https://www.markdownguide.org/)

## Headings

# Heading level 1

## Heading level 2

### Heading level 3

#### Heading level 4

##### Heading level 5

###### Heading level 6

## Emphasis

### Bold

Here is some **bold text**

### Italic

Here is some _italic text_

### Bold and Italic

Here is some **_bold and italic text_**

### Strikethrough

~~The world is flat.~~ We now know that the world is round.

## Blockquotes

> Dorothy followed her through many of the beautiful rooms in her castle.

### Blockquotes with Multiple Paragraphs

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### Nested Blockquotes

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### Blockquotes with Other Elements

> #### The quarterly results look great
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>   _Everything_ is going according to **plan**.

## Lists

### Ordered Lists

1. First item
2. Second item
3. Third item
   1. Indented item
   2. Indented item
4. Fourth item

### Unordered Lists

- First item
- Second item
- Third item
  - Indented item
  - Indented item
- Fourth item

## Code

### Inline code

At the command prompt, type `nvim`.

### Escaping Backticks

``Use `code` in your Markdown file.``

### Code Blocks

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello, world!")
}
```

## Horizontal Rules

---

---
{data-content = " with text "}

## Links

My favorite Hugo them is [unstyled](https://codeberg.org/d33trik/unstyled)

## Images

![Hugo logo](https://gohugo.io/images/hugo-logo-wide.svg)

## Tables

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

## Footnotes

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.

## Task Lists

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
