# minimis

[![Build and deploy](https://github.com/kirillbobyrev/kirillbobyrev.com/actions/workflows/build-and-deploy.yml/badge.svg)](https://github.com/kirillbobyrev/kirillbobyrev.com/actions/workflows/build-and-deploy.yml)

Minimalistic theme for personal sites built with [Hugo](https://gohugo.io).
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
good looking site.

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
- Math rendering with [KaTeX](https://katex.org/)
- Diagram rendering with [Mermaid.js](https://mermaid.js.org/)
- Mastodon [verification](https://joinmastodon.org/verification)
- Adding HTML to Markdown pages

If you want to use this theme and are missing something, feel free to create a
GitHub Issue.

## Live demo

### exampleSite

The example site is a good place to start. It showcases the features of the
theme and is a good starting point for your own site. The source code for the
example site is available under [exampleSite](/exampleSite/) and it is uploaded
to [kirillbobyrev.github.io/minimis](https://kirillbobyrev.github.io/minimis) on
every commit to `main` branch through GitHub Actions workflow:
[build-and-deploy.yml](/.github/workflows/build-and-deploy.yml).

Whenever you make a change to the theme, you can test it by running

```shell
hugo server --source exampleSite --watch
```

if you are in the root directory of the repository or just

```shell
hugo server --watch
```

If you are in the `exampleSite` directory.

### My personal site

Minimis powers my personal site and blog at
[kirillbobyrev.com](https://kirillbobyrev.com). I use it to write about software
and hobbies. The source code for the site is available at
[github.com/kirillbobyrev/kirillbobyrev.com](https://github.com/kirillbobyrev/kirillbobyrev.com).
It doesn't differ much from the example site, but it has some customizations
such as resume page, favicons and custom domain usage. It is a good example of a
real-world usage of minimis.

## Using the theme

[Hugo documentation](https://gohugo.io/documentation/) is very extensive and I
can't recommend it enough to understand the whole system and how to use external
themes.

Here is a quick start guide if you are already familiar with Hugo and want to
start using minimis:

### Create a new site

```shell
hugo new site $YOUR_SITE_NAME
```

### Add the theme

The easiest way to use the theme is through [Hugo
modules](https://gohugo.io/hugo-modules/use-modules/):

Add the following to your `hugo.toml`/`config.toml`:

```toml
theme = 'github.com/kirillbobyrev/minimis'
```

And then run

```shell
# Initialize hugo module for your site.
hugo mod init github.com/$YOUR_GITHUB_ACCOUNT/$REPO
# Fetch the theme.
hugo mod get -u
```

Alternatively, you can use the theme as a git submodule and put it under
`themes/minimis`. Check out [Hugo
docs](https://gohugo.io/getting-started/quick-start/) for more information.

### Configure the theme and your website

The theme is configured through `params` in `hugo.toml`/`config.toml`. Check out
[exampleSite/hugo.toml](/exampleSite/hugo.toml) for an example configuration of
the demo site. For a full list of available options, check out `params` in
[hugo.toml](/hugo.toml).

### Deployment

For deployment, I recommend using GitHub Pages. You can check out [Hugo
docs](https://gohugo.io/hosting-and-deployment/hosting-on-github/) on how to set
it up, but I think the provided GitHub Actions workflow is unnecessarily
complicated. Here is the workflow that powers deployment of minimis demo:
[build-and-deploy.yml](/.github/workflows/build-and-deploy.yml)
