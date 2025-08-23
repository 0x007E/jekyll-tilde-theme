---
layout: post
categories: [General]
introduction: "How is it possible to write a short introduction text under the link to the blog!"
---

If the `show_introduction` variable in `_config.yml` is set true, a short introduction is displayed under the blog title.

```yaml
# _config.yml
tiled:
  # ...
  show_introduction: true
  # ...
```

To display an introduction on the  `home`-site a `introduction` variable need to be set in the markdown file:

```
---
layout: post
introduction: "How is it possible to write a short introduction text under the link to the blog!"
...
---

Here comes to blog post...
```

### Result

The introduction text is now displayed on the `home`-site:

![Introduction Text](/assets/images/tilde-short-introduction-text.png)