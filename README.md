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

If you want to use this theme and are missing something, feel free to create a
GitHub Issue.

## Using the theme

### Adding to your site

The easiest way to use the theme is through [Hugo
modules](https://gohugo.io/hugo-modules/use-modules/):

Add the following to your `hugo.toml`/`config.toml`:

```toml
theme = 'github.com/kirillbobyrev/minimis'
```

And then run

```shell
hugo mod init github.com/$YOUR_GITHUB_ACCOUNT/$REPO
hugo mod get -u
```

That's it! You can now start editing content for your site. Check out an example
config at [exampleSite/config.toml](/exampleSite/config.toml).

Alternatively, you can use the theme as a git submodule and put it under
`themes/minimis`. Check out [Hugo
docs](https://gohugo.io/getting-started/quick-start/) for more information.

### Deployment

For deployment, I recommend using GitHub Pages. You can check out [Hugo
docs](https://gohugo.io/hosting-and-deployment/hosting-on-github/) on how to set
it up, but I think the provided GitHub Actions workflow is a bit too complicated
there. I use the following workflow for the demo:
[build-and-deploy.yml](/.github/workflows/build-and-deploy.yml) and almost the
same version for my own site:
[github.com/kirillbobyrev.com/build-and-deploy.yml](https://github.com/kirillbobyrev/kirillbobyrev.com/blob/main/.github/workflows/build-and-deploy.yml).

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
