---
layout: post
title: "Creating a post"
author:
    name: "sunriax"
    github: true
categories: [General]
introduction: "This post provides a brief introduction to the Jekyll template and describes the basic functionality of variables in the header and their application on the page."
---

A simple introduction what is possible in blog post.

### Title

The title of the post can be defined with the variable `title` in the header of the post markdown. If the title is not set, it will be derived from the filename.

```
---
layout: post
title: "Title of the Post"
...
---
```

### Dates in the post

Also the publishing date can either be derived from the filename or set with a variable called `date`. If the post is later modified an optional modifiaction date can be set with `modified_date`. The format of the date is set to `%b %-d, %Y` but can be modified in `_config.yml`

```
---
layout: post
date: 2025-08-08 14:00:00 +0200
modified_date: 2025-08-09 13:37:37 +0200
...
---
```

Further information can be found in the next posts...