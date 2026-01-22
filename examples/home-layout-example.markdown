---
layout: home
author_profile: true
---

This is an example of the **home** layout. It's typically used for your main `index.markdown` file.

## Features

- Displays recent posts
- Pagination support
- Author profile sidebar (optional)
- Clean, blog-style homepage

## Front Matter Options

```yaml
layout: home
author_profile: true  # Shows author sidebar
```

## Pagination

To enable pagination, add to `_config.yml`:

```yaml
paginate: 5  # Posts per page
paginate_path: "/page:num/"
```

Then add pagination to your home layout:

```html
{% if paginator.total_pages > 1 %}
  <!-- Pagination links -->
{% endif %}
```

## Customization

The home layout automatically shows:
- Recent posts from `_posts/` folder
- Post excerpts
- Post metadata (date, categories, tags)
- Featured images (if set in post front matter)

