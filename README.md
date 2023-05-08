# minimis

[![Build and deploy](https://github.com/kirillbobyrev/kirillbobyrev.com/actions/workflows/build-and-deploy.yml/badge.svg)](https://github.com/kirillbobyrev/kirillbobyrev.com/actions/workflows/build-and-deploy.yml)

Minimalistic theme for personal websites built with [Hugo](https://gohugo.io).
The goal of minimis is to be:

- Small, so that the codebase is very easy to understand and easily
  understandable
- Focused to avoid feature bloat. The goal is to build a theme for a personal
  page and software engineering blog.
- Simple: no complicated and large CSS frameworks, JavaScript libraries and
  heavy dependencies.

This theme is heavily inspired by [bearblog](https://bearblog.dev/) and
[hugo-bearblog](https://github.com/janraasch/hugo-bearblog), but is focused on
features that I was missing and wanted to change/adjust to my liking. bearblog
is a prime example of something that looks very good with minimal CSS
configuration, so realized I don't need a complicated CSS framework to make a
good looking website.

I am not a professional web developer, so I am sure there are many things that
could be improved. If you have any suggestions, please open an issue or a pull
request: I am happy to accept contributions.

## Features

The theme is still in development, but the following features are already
implemented:

- Tags and filtering
- Custom links in the main menu
- Google Analytics, Twitter cards support
- RSS support
- Favicons
- Math rendering with KaTeX
- Diagram rendering with Mermaid.js
- Mastodon verification

If you want to use this theme and are missing something, feel free to create a
GitHub Issue.

## Live demo

### exampleSite

The example site is a good place to start. It showcases the features of the
theme and is a good starting point for your own website. The source code for the
example site is available under [exampleSite](./exampleSite/) and it is uploaded
to <https://kirillbobyrev.github.io/minimis> on every commit to `main` branch
through GitHub Actions workflow:
[build-and-deploy.yml](./.github/workflows/build-and-deploy.yml).

Whenever you make a change to the theme, you can test it by running

```shell
hugo server --source exampleSite --watch
```

if you are in the root directory of the repository or just

```shell
hugo server --watch
```

If you are in the `exampleSite` directory.

### My personal website

Minimis powers my personal website and blog at <https://kirillbobyrev.com>. I
use it to write about software and hobbies. The source code for the website is
available at
[github.com/kirillbobyrev/kirillbobyrev.com](https://github.com/kirillbobyrev/kirillbobyrev.com).
It doesn't differ much from the example site, but it has some customizations
such as resume page, favicons and custom domain usage. It is a good example of a
real-world usage of minimis.
