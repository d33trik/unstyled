---
title: Code Syntax Highlighting
draft: false
---

This document showcases how this theme display the various options available for
code syntax highlighting in Hugo.

To learn how to use them, you can see this file at
`themes/unstyled/content/code-syntax-highlighting.md`. For more options,
see the [Hugo documentation](https://gohugo.io/content-management/syntax-highlighting/#options-1).

## codeFences

This option, enabled by default, determines whether to highlight code within
fenced code blocks (```).

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}
```

## guessSyntax

If no language is specified, `guessSyntax` will attempt to determine the
language automatically. If it cannot, it will default to plain text.

```
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}
```

## tabWidth

`tabWidth` controls the number of spaces that a tab character will be rendered with.

```go {tabWidth=8}
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}
```

## lineNos

`lineNos` enables or disables line numbers.

```go {linenos=true}
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}
```

## hl_Lines

This option allows you to highlight specific lines within a code block. You can
specify a single line, a range of lines, or a combination of both.

```go {linenos=true, hl_lines="3 6"}
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}
```

## lineNoStart

`lineNoStart` sets the starting number for the line count.

```go {linenos=true,linenoStart=10}
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}
```

