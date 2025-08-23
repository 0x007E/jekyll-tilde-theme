---
layout: post
title: "Parameters that can be set in _config.yml"
categories: [Configuration]
introduction: "Howto setup the _config.yml for your preferred needings"
tags: [parameters, config, _config.yml, yml, yaml]
---

In the following post you will be familiarized with the configuration of the `_config.yml`.

## General

In the begining of the `_config.yml` you find the standard page settings such as the `title`, `subtitle` and many more. These settings can be adjusted as desired for your personal blog page.

```yaml
title: "My Jekyll Blog Page"

description: >
  Write an awesome description for your new site here. You can edit this line
  in _config.yml. It will appear in your document head meta (for Google search
  results) and in your feed.xml site description.
```

This theme is implemented to be used with github pages so a github account who manages the blogs should be defined in the config section of the `_config.yml`.

> The mail-address can be deleted from the mail adress if it is not used.

```yaml
github:
  user: "0x007e"
  email: "person@mail.address"
```

If the brand logo should be different (and not the github avatar) it can be defined within the `brand` section in `_config.yml`.

```yaml
brand:
  # Can also be an image in the asses folder: /assets/images/image.png
  image: "https://path.to/image.png"
  # For Gravatar it is necessary to encrypted your mail with SHA256 -> https://emn178.github.io/online-tools/sm3.html
  # gravatar: "f4ef9cbf3c2c5a2a1afa89a33134b335b5237132f06729990cacbfc5646b0b6a"
  # Sizing the image
  # width: 20
  # height: 20
```
> If nothing is defined in the `brand` section the github avatar will be used!

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
    # color: primary, secondary, success, danger, warning, info, light, dark, body-emphasis
    color: "danger"
  - title: Tilde Theme repository at GitLab
    icon: gitlab
    link: "https://gitlab.com/?"
```

The page settings itself are containing differnt properties to define the layout/design and what is displayed on the site. The `nav_pages` property  sets the links in the navbar that should be displayed. All other links to markdown files are removed from the navbar. In this example only the `about` and `impressum`-site gets linked in the navbar. The `date_format` sets the format of the date in the list of blogs and the blogs itself. The standardformat is `%b %-d, %Y` but can be adapted to every desired format. More information for formatting the date can be found [here](https://shopify.github.io/liquid/filters/date/).

```yaml
tilde:
  # Restict links in navbar to listed pages
  # -> e.g. if you have a README.md/LICENSE.md in your root folder and they should not be displayed.
  nav_pages:
    - about.md
    - impressum.md
  # Set in which formate dates are displayed
  date_format: "%b %-d, %Y"
  show_introduction: true
  visible_posts: 4
  category_show_goto: true
  truncate_next_blog_link: 35
```

If `show_introduction` is enabled an short introduction text is displayed in the list of blogs when the `introduction` variable is defined in the blog markdown.

![Introduction](/assets/images/tilde-short-introduction-text.png)

> Informations how to write an introduction can be found in the *Write a short introduction* post

With the Variable `visible_posts` it is possible to control how much content is displayed on the `home`-site. If there are more posts in a category they get hided.

![Hiding Posts](/assets/images/tilde-categories.png)

> With the button `Show more` the hided posts can be displayed.

The `category_show_goto` option enabled a menu in the top to navigate to the categories within a heading.

![Goto Categories](/assets/images/tilde-category-goto.png)

In the bottom of the site a link to the previous and to the next blog post is displayed. If the Text is to long the design crashes. The `truncate_next_blog_link` parameter sets the maximum length of the link text before it gets truncated.

Within the `footer`-section it is possible to set the division between the `github` and the `description`.

```yaml
footer:
# Column allocation in the footer. A total of 10 is always required.
   github_column: 4
   description_column: 6
```

> Sumarized it always has to be 10!

![Footer Division](/assets/images/tilde-footer-division.png)

A `feed` is automatically generated. To disable the feed link set `hide` to `true`. If the link gets displayed the color can be adjusted throug the `bootstrap` standard color palette (same color as in the `social` section).

```yaml
feed:
  hide: false
  color: "success"
```

When `google_analytics` should be loaded add your personal analytics tracking id.

```yaml
google_analytics: "UA-XXXXXXXXX-X" # Google Analytics tracking ID
```

The rest of the `_config.yml` section is usually not relevant for user configuration.

```yaml
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