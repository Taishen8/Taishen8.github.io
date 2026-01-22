---
layout: tags
title: "Tags"
permalink: /tags/
---

This page shows all tags used in your posts.

## How Tags Work

Tags are similar to categories but more flexible. Add them to post front matter:

```yaml
---
layout: single
title: "My Post"
tags: [javascript, react, tutorial]
---
```

## Tag Pages

You can create individual tag pages by creating files like:

- `tag-javascript.markdown`
- `tag-react.markdown`

With front matter:

```yaml
---
layout: tag
title: "JavaScript"
permalink: /tag/javascript/
taxonomy: javascript
---
```

## Tags vs Categories

- **Categories:** Broad topics (e.g., "Web Development", "Design")
- **Tags:** Specific topics (e.g., "javascript", "react", "css")

Use categories for main sections, tags for specific topics.

