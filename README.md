[![Version: 1.0 Release](https://img.shields.io/badge/Version-1.0%20Release-green.svg)](https://github.com/0x007e/jekyll-tilde-theme) [![License MIT](https://img.shields.io/badge/License-MIT-lightgrey)](./LICENSE.md) [![Jekyll](https://img.shields.io/badge/Powered%20by-Jekyll-red.svg)](https://jekyllrb.com/) ![Build](https://github.com/0x007e/jekyll-tilde-theme/actions/workflows/pages/pages-build-deployment/badge.svg)

# Jekyll Tilde Template

This theme is designed to be used as a (multi-category) blog that gets automatically built with github-pages.

> An introduction of the functionallity, how to use this theme and a preview of it´s looking can be found [here](https://0x007e.github.io/jekyll-tilde-theme).

## Usings within this Template

The template is designed using `bootstrap` and `tabler` icons.

| Framework        | Version  |
|:-----------------|:--------:|
| **Bootstrap**    | `5.3.7`  |
| **Tabler Icons** | `latest` |

# Quickstart guide

To use this theme within your own repository on `github` simply create a repository from this template (details can be found [here](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)) or clone it locally.

```bash
git clone https://github.com/0x007E/jekyll-tilde-theme.git
```

Then change the `_config.yml` according to your requirements and if necessary set the correct `url` and `baseurl`.

```yaml
url: "https://0x007e.github.io"
baseurl: "/jekyll-tilde-theme"
```

> If the template is used as your main page (e.g. `username.github.io`) leave the baseurl empty!

## Necessary Github settings

To enable `github-pages` within your repository it is necessary to activate them in the repository settings:

![Enable GH-Pages](./assets/images/enable-gh-pages.png)

> If the theme should appear within a code repository just create a new branch (e.g. called github-pages) and put the files in there. It is necessary to choose the right `branch` in the `settings`.

---

R. GAECHTER