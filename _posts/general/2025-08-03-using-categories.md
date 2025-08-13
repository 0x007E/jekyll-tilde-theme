---
layout: post
categories: [General]
introduction: "Description of how to use categories within a post and why this maybe makes sense."
---

If you post how to make some cookies and nothing else you won't need any category (simply do not add a `categories` variable to the header of the markdown file). But if you start to post different things (e.g. Mikrocontroller and Hardware Design) it totally makes sense that you start with categories.

### Setup categories

It is not necessary to create folders for a set of categories. A category itself can simple be defined with a variable in the header of the markdown and then automatically is listed in the main `/` page under the varialbe text.

```
---
layout: post
categories: [Hardware]
...
---
```

But to keep things tidy it makes totally sense if the different posts are in subdirectories. So that they can easily be found.

```
Folder structure:
+ /
  /posts +
         /hardware +
                   - 2025-08-01-how-to-use-a-microcontroller.md
                   - 2025-08-02-......md
         /software
                   - 2025-08-01-read-uncle-bobs-clean-code.md
                   - 2025-08-02-......md
         /garden
                   - 2025-08-01-what-are-you-doing-with-chillis-in-your-garden.md
                   - 2025-08-02-......md
```


A post itself can also be renderd in software and hardware. If the post should appear in hardware and software the `categories` variable has to be extenden:

```
Folder structure for multi-category-posts:
+ /
  /posts +
         - 2025-08-01-multi-post.md
```

```
---
layout: post
categories: [Hardware, Software]
...
---
```

