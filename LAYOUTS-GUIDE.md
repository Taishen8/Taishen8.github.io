# Minimal Mistakes Layouts Guide

A simple guide to using different layouts in the Minimal Mistakes Jekyll theme.

## Quick Reference

| Layout | Best For | Sidebar | Full Width |
|--------|----------|---------|------------|
| `single` | Blog posts, individual pages | Optional | No |
| `archive` | Listing posts, portfolios | Optional | No |
| `splash` | Landing pages, home pages | No | Yes |
| `home` | Main homepage with posts | Optional | No |
| `categories` | Category listing | Optional | No |
| `tags` | Tag listing | Optional | No |

---

## 1. Single Layout

**Use for:** Blog posts, individual pages, articles

### Basic Example

```yaml
---
layout: single
title: "My Blog Post"
date: 2026-01-19
categories: [blog]
tags: [jekyll, tutorial]
---
```

### With Header Image

```yaml
---
layout: single
title: "My Post with Image"
header:
  image: /assets/images/header.jpg
  overlay_image: /assets/images/overlay.png
  overlay_filter: 0.5
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---
```

### With Author Profile

```yaml
---
layout: single
title: "My Post"
author_profile: true  # Shows your bio in sidebar
---
```

**Key Options:**
- `author_profile: true` - Shows author sidebar
- `header.image` - Header background image
- `header.overlay_filter` - Darken overlay (0.0 to 1.0)
- `header.actions` - Call-to-action buttons

---

## 2. Archive Layout

**Use for:** Listing blog posts, portfolio pages, project collections

### Basic Example

```yaml
---
layout: archive
title: "My Blog Posts"
permalink: /posts/
author_profile: true
---
```

The archive layout automatically displays:
- All posts from `_posts/` folder
- Posts matching specific categories/tags
- Paginated results

**Key Options:**
- `author_profile: true` - Shows author sidebar
- Automatically paginates if configured in `_config.yml`

---

## 3. Splash Layout

**Use for:** Landing pages, hero sections, marketing pages

### Basic Example

```yaml
---
layout: splash
title: "Welcome"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/hero.jpg
  actions:
    - label: "Get Started"
      url: "/about/"
    - label: "Learn More"
      url: "/portfolio/"
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
excerpt: "A compelling tagline or description"
---
```

**Key Options:**
- `header.overlay_color` - Hex color for overlay
- `header.overlay_filter` - Darken overlay (0.0 to 1.0)
- `header.actions` - Array of buttons
- `excerpt` - Short description below header

**Tips:**
- Use high-quality images (1920x1080+)
- Keep excerpt short and punchy
- Limit to 2-3 action buttons

---

## 4. Home Layout

**Use for:** Main homepage (typically `index.markdown`)

### Basic Example

```yaml
---
layout: home
author_profile: true
---
```

**Features:**
- Shows recent posts automatically
- Supports pagination
- Clean blog-style homepage

**Pagination Setup** (in `_config.yml`):
```yaml
paginate: 5  # Posts per page
paginate_path: "/page:num/"
```

---

## 5. Categories Layout

**Use for:** Category listing pages

### Basic Example

```yaml
---
layout: categories
title: "Categories"
permalink: /categories/
---
```

### Individual Category Page

```yaml
---
layout: category
title: "Web Development"
permalink: /category/web-development/
taxonomy: web-development
---
```

**In Posts:**
```yaml
---
layout: single
title: "My Post"
categories: [web-development, tutorial]
---
```

---

## 6. Tags Layout

**Use for:** Tag listing pages

### Basic Example

```yaml
---
layout: tags
title: "Tags"
permalink: /tags/
---
```

### Individual Tag Page

```yaml
---
layout: tag
title: "JavaScript"
permalink: /tag/javascript/
taxonomy: javascript
---
```

**In Posts:**
```yaml
---
layout: single
title: "My Post"
tags: [javascript, react, tutorial]
---
```

---

## Common Front Matter Options

### All Layouts

```yaml
---
layout: single  # or archive, splash, etc.
title: "Page Title"
permalink: /your-url/  # Custom URL
author_profile: true  # Show author sidebar
---
```

### For Posts

```yaml
---
layout: single
title: "Post Title"
date: 2026-01-19 12:00:00 +0800
categories: [category1, category2]
tags: [tag1, tag2, tag3]
---
```

### With Images

```yaml
---
layout: single
title: "Post with Image"
header:
  image: /assets/images/image.jpg
  overlay_image: /assets/images/overlay.png
  overlay_filter: 0.5
  caption: "Image caption"
---
```

---

## File Structure Tips

```
your-site/
├── index.markdown          # Home page (layout: home)
├── about.markdown          # About page (layout: single)
├── portfolio.markdown      # Portfolio (layout: archive)
├── contact.markdown        # Contact (layout: single)
├── _posts/                 # Blog posts (layout: single)
│   └── 2026-01-19-post.md
├── _data/
│   └── navigation.yml      # Menu navigation
└── assets/
    └── images/             # Your images
```

---

## Quick Tips

1. **Always use `layout: single` for posts** (not `layout: post`)
2. **Set `author_profile: true`** to show your bio in sidebar
3. **Use full paths for images**: `/assets/images/image.jpg`
4. **Categories are broad**, **tags are specific**
5. **Restart Jekyll server** after changing `_config.yml`

---

## Need Help?

- Check example files in `/examples/` folder
- Minimal Mistakes docs: https://mmistakes.github.io/minimal-mistakes/
- Jekyll docs: https://jekyllrb.com/docs/

---

## Example Pages Created

I've created example pages for you to reference:

- `/examples/single-layout/` - Single layout example
- `/examples/archive-layout/` - Archive layout example
- `/examples/splash-layout/` - Splash layout example
- `/examples/home-layout/` - Home layout example
- `/examples/categories/` - Categories example
- `/examples/tags/` - Tags example

Visit these pages to see each layout in action!

