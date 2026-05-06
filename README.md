# perseverance.ai Portfolio

A minimal, clean, and elegant portfolio website built with Jekyll and hosted on GitHub Pages.

## Features

- **About Me**: Professional background and expertise
- **Projects**: Showcase of AI/LLM projects
- **Skills**: Technologies and tools
- **Experience**: Professional timeline
- **Blog**: Articles organized by date with tag filtering
- **Contact**: Social media and email links

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

Visit `http://localhost:4000` to see your site.

## Adding Blog Posts

Create a new file in `_posts/` with the format: `YYYY-MM-DD-title.md`

```yaml
---
date: 2026-05-06
title: "Your Post Title"
tags: [AI, LLM, System Design]
excerpt: "Short description here"
reading_time: 5
---

Your content here...
```

## Customization

- Edit `_config.yml` to update site information and social links
- Modify `assets/css/style.css` to change colors and styling
- Update `_includes/` files for layout changes
