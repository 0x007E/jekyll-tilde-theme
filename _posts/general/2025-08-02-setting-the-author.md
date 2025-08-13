---
layout: post
author:
    name: "g.raf"
    icon: "linkedin"
    link: "https://linkedin.com/in/...."
categories: [General]
introduction: "In this post the handling of an author is described and how variables can be set to modify the author"
---

If no author is set the github user within the `_config.yml` will be used as author.

### Setup another author

If the post is done by a different user there are two possibilitis

#### Optional github author

To setup an optional github author the head of the post can be defined with the github username of the optional author:

```
---
layout: post
...
author:
    name: "sunriax"
    github: true
...
---
```

#### External author

If a user without a github account posts an entry it is possible to use another plattform like e.g. LinkedIn (used within this post):

```
---
layout: post
...
author:
    name: "g.raf"
    icon: "linkedin"
    link: "https://linkedin.com/in/...."
...
---
```
