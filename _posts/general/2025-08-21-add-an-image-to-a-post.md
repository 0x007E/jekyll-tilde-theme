---
layout: post
title: "Add an image to a post"
categories: [General]
introduction: "Description how to add an image to a post with relative and absolute path."
---

A simple introduction how to add an image to a blog post

### Relative Path

If the image is hosted on github it should be copied into the assets folder `/assets/images/...'. After that the image can easyly be included.

```
{% raw %}
![Image Desciption]({{ '/assets/images/picture.png' | relative_url }})
{% endraw %}
```

> it is necessary to convert the path to the relative_url of the page (`{{ '' | relative_url }}`) or the image is not getting displayed correctly wenn the site is hosted in a subfolder!

### Absolute Path

An absolute path can be used normaly as in any other markdown page on github oder any other platform.

```
![Image Desciption](https://path.to/image.png)
```