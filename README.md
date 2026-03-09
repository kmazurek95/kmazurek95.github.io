# kmazurek95.github.io

Personal research website built with [Hugo](https://gohugo.io/) and deployed on GitHub Pages.

## Quick Start

### Prerequisites
- [Hugo Extended](https://gohugo.io/installation/) v0.139.0+

### Local Development
```bash
# Clone the repo
git clone https://github.com/kmazurek95/kmazurek95.github.io.git
cd kmazurek95.github.io

# Start local server with live reload
hugo server -D
```
Site will be at `http://localhost:1313/`

### Create New Content
```bash
# New blog post
hugo new posts/my-new-post.md

# New project page
hugo new projects/my-project.md
```

### Deploy
Push to `main` branch. GitHub Actions handles the build and deployment automatically.

## Structure

```
.
├── content/
│   ├── posts/          # Blog posts, commentary, research notes
│   ├── projects/       # Research project pages
│   ├── experience/     # Work experience timeline
│   └── cv/             # CV page
├── layouts/            # Custom Hugo templates
├── assets/css/         # Stylesheet
├── static/             # Images, PDFs, other static files
└── hugo.toml           # Site configuration
```

## Writing a New Post

Front matter template:
```yaml
---
title: "Your Title"
date: 2026-03-09
summary: "One-line description for listings"
tags: ["tag1", "tag2"]
type: "Commentary"   # or "Research Note", "Essay", "Analysis"
---
```

### Shortcodes

**Key finding callout:**
```
{{</* finding label="Key Finding" */>}}
Your finding text here.
{{</* /finding */>}}
```

## Adding a Project

Create `content/projects/your-project.md`:
```yaml
---
title: "Project Title"
type: "Method Category"
summary: "Description for cards"
date: 2026-01-01
weight: 1          # Lower = appears first
featured: true     # Show on homepage
repo: "https://github.com/..."
dashboard: "https://..."
stats:
  - "Stat 1"
  - "Stat 2"
tags: ["tag1"]
---
```

## Configuration

Edit `hugo.toml` to update:
- `baseURL` — your GitHub Pages URL
- `[params]` — description, social links
- `[menu]` — navigation items
