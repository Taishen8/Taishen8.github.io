# Quick Start Guide - Minimal Mistakes Theme

Welcome! This guide will help you get your personal site up and running quickly.

## 🚀 First Steps

### 1. Install Dependencies

Run this command to install all required gems:

```bash
bundle install
```

### 2. Customize Your Site

Edit `_config.yml` and update:
- `title` - Your site title
- `email` - Your email
- `description` - Site description
- `url` - Your site URL (e.g., `https://yourusername.github.io`)
- `author` section - Your name, bio, social links

### 3. Start the Server

```bash
bundle exec jekyll serve
```

Visit `http://localhost:4000` to see your site!

---

## 📄 Understanding Layouts

### Single Layout (Most Common)
**Use for:** Blog posts, individual pages

```yaml
---
layout: single
title: "My Page"
---
```

### Archive Layout
**Use for:** Listing posts, portfolios

```yaml
---
layout: archive
title: "My Posts"
permalink: /posts/
---
```

### Splash Layout
**Use for:** Landing pages, hero sections

```yaml
---
layout: splash
title: "Welcome"
header:
  overlay_image: /assets/images/hero.jpg
---
```

### Home Layout
**Use for:** Main homepage (`index.markdown`)

```yaml
---
layout: home
---
```

---

## 📝 Creating Content

### Blog Posts

Create files in `_posts/` folder with format: `YYYY-MM-DD-title.md`

```yaml
---
layout: single
title: "My First Post"
date: 2026-01-20
categories: [blog]
tags: [jekyll, tutorial]
---
```

### Pages

Create `.markdown` files in the root directory:

```yaml
---
layout: single
title: "About"
permalink: /about/
---
```

---

## 🎨 Customization

### Navigation Menu

Edit `_data/navigation.yml` to customize your menu:

```yaml
main:
  - title: "Home"
    url: /
  - title: "About"
    url: /about/
```

### Author Profile

Edit the `author` section in `_config.yml`:

```yaml
author:
  name: "Your Name"
  bio: "Your bio"
  avatar: "/assets/images/bio-photo.jpg"
  links:
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/yourusername"
```

### Theme Skin

Change the color scheme in `_config.yml`:

```yaml
minimal_mistakes_skin: "default"  # Options: air, aqua, contrast, dark, dirt, neon, plum, sunrise
```

---

## 📚 Learn More

- **Full Layouts Guide:** See `LAYOUTS-GUIDE.md` for detailed layout examples
- **Example Pages:** Check `/examples/` folder for working examples
- **Official Docs:** https://mmistakes.github.io/minimal-mistakes/

---

## 📁 File Structure

```
your-site/
├── _config.yml           # Site configuration
├── _data/
│   └── navigation.yml    # Menu navigation
├── _posts/               # Blog posts go here
│   └── YYYY-MM-DD-title.md
├── index.markdown        # Homepage
├── about.markdown        # About page
├── portfolio.markdown    # Portfolio page
├── contact.markdown      # Contact page
└── assets/
    └── images/           # Your images
```

---

## ✅ Checklist

- [ ] Updated `_config.yml` with your info
- [ ] Customized `_data/navigation.yml`
- [ ] Added your bio photo to `/assets/images/`
- [ ] Created your first blog post
- [ ] Updated the About page
- [ ] Tested the site locally

---

## 🆘 Common Issues

### "Unknown tag 'include_cached'" Error
**Solution:** Make sure `jekyll-include-cache` is in your `Gemfile` and `_config.yml` plugins list.

### Images Not Showing
**Solution:** Use full paths starting with `/assets/images/` (not relative paths).

### Layout Not Working
**Solution:** 
- Use `layout: single` for posts (not `layout: post`)
- Restart Jekyll server after changing `_config.yml`

### Navigation Not Showing
**Solution:** Check that `_data/navigation.yml` exists and has correct format.

---

## 🎯 Next Steps

1. **Personalize:** Update all the placeholder content with your own
2. **Add Images:** Add your photos to `/assets/images/`
3. **Write Posts:** Create your first real blog post
4. **Customize:** Experiment with different layouts and skins
5. **Deploy:** Push to GitHub Pages when ready!

---

Happy building! 🎉

