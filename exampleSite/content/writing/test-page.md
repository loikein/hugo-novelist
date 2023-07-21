---
author: Hugo Authors
title: Test
date: '2023-07-16'
# description: >-
#   Sample article showcasing basic Markdown syntax and formatting for HTML
#   elements.
fandoms:
  - "Greatest TV Show"
characters:
  - "A (Greatest TV Show)"
tags:
  - Testing
ratings:
  rating: "general-audience"
  warning: "no"
  category: "no"
  complete: "yes"
---

## Normal tests

Begin test file…

### Formatting

**Bold**, __bold__, **加粗**

*Italic*, _italic_, *斜体*

<u>Underline</u>, <underline>underline</underline>

<del>Strike</del>, <s>strike</s>, ~~strike~~, ~strike~, --strike--

<mark>Highlight</mark>, =highlight=, ==highlight==

<!-- Comments-->

Footnote[^1], footnote[^2]

[^1]: The linked footnote appears at the end of the document.

[^2]: New lines

---


### Lists

- `ul`
- Unordered list

1. `ol`
1. Ordered list

`dl`
:   `dt`
:   Description list

- [x] Task list
- [ ] Task list

### Code

Inline `code`, `` `escape` ``, and <kbd>keystroke</kbd>

Inline `code`, `` `escape` ``, and <kbd>keystroke</kbd>

This theme does not support code blocks yet.

```go {hl_lines=["2-5"],linenostart=199}
package main

import "log"

func add(x int, y int) int {
  log.Println("We are going to take the sum of two numbers, and leave a very very very long comment.")
  return x + y
}

func main() {
  y := add(1, 2)
  log.Println(y)
}
```

Here's an example with line numbers. The CSS is buggy.

```go {linenos=table,hl_lines=["2-5"],linenostart=199}
package main

import "log"

func add(x int, y int) int {
  log.Println("We are going to take the sum of two numbers, and leave a long comment.")
  return x + y
}

func main() {
  y := add(1, 2)
  log.Println(y)
}
```

### Font

> 我能体に傷つけないで吞下 259 ml glass。

> Four score and seven years ago our fathers brought forth upon this continent, a new nation, conceived in Liberty, and dedicated to the proposition that all men are created equal.

0 Oo Ii Ll 1 | 2 Z 5 s 8 Bb 6 # * ^ ~ \(\) {} \[\] . , : ; “ ‘ ’ \`

```
0 Oo Ii Ll 1 | 2 Z 5 s 8 Bb 6 # * ^ ~ () {} [] . , : ; “ ‘ ’ `
```

### LaTeX & Table

This theme does not support LaTeX yet.

`$\LaTeX{}$`

`$$R_1 \begin{cases} >\mu_{2} \\ \leq \mu_{2} \end{cases}$$`

| Message to agent 1 | `$M_1$`          |
| ------------------ | -------------- |
| Agent 1's action   | `$a_1$`          |
| New finding        | `$R_1 \begin{cases} >\mu_{2} \\ \leq \mu_{2} \end{cases}$` |
