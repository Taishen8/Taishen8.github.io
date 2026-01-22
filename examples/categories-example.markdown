---
layout: categories
title: "Categories"
permalink: /categories/
---

This page shows all categories used in your posts.

## How Categories Work

Categories help organize your content. Add them to post front matter:

```yaml
---
layout: single
title: "My Post"
categories: [web development, tutorial]
---
```

## Category Pages

You can create individual category pages by creating files like:

- `category-web-development.markdown`
- `category-tutorial.markdown`

With front matter:

```yaml
---
layout: category
title: "Web Development"
permalink: /category/web-development/
taxonomy: web-development
---
```

