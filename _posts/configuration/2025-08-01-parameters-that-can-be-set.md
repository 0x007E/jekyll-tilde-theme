---
layout: post
title: "Parameters that can be set in _config.yml"
categories: [Configuration]
introduction: "Howto setup the _config.yml for your preferred needings"
tags: [parameters, config, yaml]
---

In the following post you will be familiarized with the configuration of the `_config.yml`.

## General

In the begining of the `_config.yml` you find the standard page settings such as the `title`, `subtitle` and many more. These settings can be adjusted as desired for your personal blog page.

```yaml
title: "My Jekyll Blog Page"
subtitle: "Blog Entries"

description: >
  Write an awesome description for your new site here. You can edit this line
  in _config.yml. It will appear in your document head meta (for Google search
  results) and in your feed.xml site description.
```

This theme implemented to be used with github pages so a github account who manages the blogs should be defined in the config section of the `_config.yml`.

> The mail-address can be deleted from the mail adress if it is not used.

```yaml
github:
  user: "0x007e"
  email: "person@mail.address"
```

A copyright text can also be set. The text gets displayed at the end of each page. If a link to a license is defined it also lights up at the end of each page.

```yaml
copyright: "Powerd by 0x007E"
license: "https://github.com/0x007e/tilde/LICENSE.md"
```

Over the `url` parameter it is possible to define the hostname and the protocol for the site. The `baseurl` defines whether the blog is in a subdirectory.

```yaml
url: "https://0x007e.github.io" # the base hostname & protocol for your site, e.g. http://example.com
baseurl: "" # the subpath of your site, e.g. /blog
```

Social badges can be added to the bottom of the page. Therefore it is necessary to define a Title and give the badge an icon that is available on [https://tabler.io/icons ](https://tabler.io/icons) under the `brand-` category. With the `color` property it is possible to set a different color for the bade. Following colors are possible:

- primary
- secondary
- success
- danger
- warning
- info
- light
- dark
- body-emphasis

```yaml
social:
  - title: Tilde Theme repository at GitHub
    icon: github
    link: "https://github.com/?"
    # values: primary, secondary, success, danger, warning, info, light, dark, body-emphasis
    color: "danger"
  - title: Tilde Theme repository at GitLab
    icon: gitlab
    link: "https://gitlab.com/?"
```

The page settings itself are containing differnt properties to define the layout/design and what is displayed on the site. The `nav_pages` property  sets the links in thee navbar that shold be displayed. All other links to file are removed from the navbar. In this example only the `about`-site would be linked in the navbar. The `date_format`sets the format of the date in the Bloglist and the blogs itself. The standardformat is `%b %-d, %Y` but can be adapted to every desired format.

```yaml
tilde:
  # Restict links in navbar to listed pages
  nav_pages:
    - about.md
  date_format: "%b %-d, %Y"
  show_introduction: true
  visible_posts: 2
  category_show_goto: true
```

```yaml
# footer:
# Column allocation in the footer. A total of 10 is always required.
#   github_column: 4
#   description_column: 6


feed:
  hide: false
  color: "success"

#google_analytics: "UA-XXXXXXXXX-X" # Google Analytics tracking ID

plugins:
  - jekyll-feed
  - jekyll-seo-tag
  - jekyll-sitemap
  - jemoji
  - jekyll-avatar

markdown: kramdown
kramdown:
  input: GFM
  syntax_highlighter: rouge
  highlighter: rouge
  syntax_highlighter_opts:
    line_numbers: false 

sass:
  style: compressed

defaults:
  -
    scope:
      path:            "assets/*"
    values:
      sitemap:         false
```