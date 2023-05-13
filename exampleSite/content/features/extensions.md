+++
title = 'Extensions'
date = 2023-05-08
tags = ['hugo', 'features']
math = true
+++

Use `{{</* toc */>}}` [Hugo
shortcode](https://gohugo.io/content-management/shortcodes/) to generate table
of contents:

{{< toc >}}

## Checklist

- [ ] TODO
- [x] Completed

## Code highlighting

Use highlight
[shortcode](https://gohugo.io/content-management/syntax-highlighting/#example-highlight-shortcode)
or Markdown-style code fences with attributes to highlight regions, set line
numbers etc.

````markdown
go {linenos=inline,hl_lines=[8,"15-17"],linenostart=199}
````

```go {linenos=inline,hl_lines=[8,"15-17"],linenostart=199}
// GetTitleFunc returns a func that can be used to transform a string to
// title case.
//
// The supported styles are
//
// - "Go" (strings.Title)
// - "AP" (see https://www.apstylebook.com/)
// - "Chicago" (see https://www.chicagomanualofstyle.org/home.html)
//
// If an unknown or empty style is provided, AP style is what you get.
func GetTitleFunc(style string) func(s string) string {
  switch strings.ToLower(style) {
  case "go":
    return strings.Title
  case "chicago":
    return transform.NewTitleConverter(transform.ChicagoStyle)
  default:
    return transform.NewTitleConverter(transform.APStyle)
  }
}
```

### Mermaid diagrams

You can use [Mermaid](https://mermaid-js.github.io/mermaid/#/) diagrams in your
posts. Just write the diagram definition in a fenced code block with `mermaid`
language identifier:

```mermaid
graph LR;
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
```

### Unsafe

Sometimes you might want to render plain HTML code:

>```html
>Please press <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>R</kbd>
>```

Use `{{</* unsafe */>}} YOUR TEXT {{</* /unsafe */>}}` shortcode for that:

>{{< unsafe >}}
Please press <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>R</kbd>
{{< /unsafe >}}

## Math

If you want to use KaTeX-based math rendering in your posts, set `math = true`
in the post front matter or in the site config. Then you can use LaTeX syntax to
write math equations (`$$` for display mode, `$` for inline mode):

$$
i \hbar \frac{\partial}{\partial t}\Psi(\mathbf{r},t) = \hat H \Psi(\mathbf{r},t)
$$

## Default Hugo shortcodes

You can use all the [built-in Hugo
shortcodes](https://gohugo.io/content-management/shortcodes/#use-hugos-built-in-shortcodes)
in your posts. Here are some examples:

### Gist

{{< gist kirillbobyrev 3acb1f32d9333d91c12046df7672bf4b >}}

### YouTube

{{< youtube VhxrFor3VyQ >}}

### Twitter

{{< tweet user="kirillbobyrev" id="1465758062967463940" >}}
