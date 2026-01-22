---
layout: archive
title: "Archive Layout Example"
permalink: /examples/archive-layout/
author_profile: true
---

This is an example of the **archive** layout. It's perfect for:

- Listing blog posts
- Portfolio pages
- Project collections
- Category pages

## Features

- Automatically lists posts/pages
- Grid or list view of items
- Pagination support
- Filtering by category or tag

## How It Works

The archive layout automatically displays:
- All posts in `_posts/` folder
- Pages with specific categories
- Items matching certain tags

## Front Matter Options

```yaml
layout: archive
title: "Archive Page Title"
permalink: /archive-url/
author_profile: true  # Shows author sidebar
```

## Filtering Posts

You can filter what appears on archive pages by adding to `_config.yml`:

```yaml
archive:
  type: grid  # or "list"
  entries_layout: grid  # or "list"
```

Or filter by category/tag in the page front matter.

