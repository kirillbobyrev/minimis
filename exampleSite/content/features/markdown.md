+++
title = 'Markdown rendering'
date = 2023-05-07
tags = ['markdown', 'features']
math = true
+++

This is a demo of the basic Markdown rendering.

## Headings

## H2

### H3

#### H4

##### H5

## Text styling

**Bold** and *italic*.

## Lists

### Unordered

- Dogs
- Cats
  - Abyssinian
  - Siamese
- Cows

### Ordered

1. Build a blog.
    1. Find good static site generator.
    2. Select a theme.
        - Shouldn't be too complicated.
        - Shouldn't take too long to setup.
2. Congrats!

## Footnote

Here is a simple footnote[^1]. With some additional text after it.

## Table

| Column 1 | Column 2 |
| --- | --- |
| Value 1 | Value 2 |

## Code

The code can be either inline `import discord.py` or multiline with the fences:

```c++
class Foo {
public:
  Foo(int x);
};

int main() {
  std::vector vec = {1, 2, 3};
  vec[42] = x;
  std::string s = "Hello, world!";
  return 0;
}
```

Check out [extensions]({{< ref "/features/extensions.md#code-highlighting" >}})
for more code highlighting examples.

## Quotes

> This is a single quote.

Some text in-between.

> This is a
> multi line
> quote

[^1]: My footnote reference.
