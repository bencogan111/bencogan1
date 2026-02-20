# Ben Cogan — Personal Writing Site

A Hugo-powered personal site for essays and blog posts, deployed on GitHub Pages.

## Quick Start

### 1. Create a GitHub Repository

1. Go to [github.com/new](https://github.com/new) and create a new repository (e.g., `bencogan-site` or `bencogan.com`)
2. Make it **public** (required for free GitHub Pages)
3. Push this code to that repo:

```bash
cd bencogan-site
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin git@github.com:YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

### 2. Enable GitHub Pages

1. In your repo, go to **Settings → Pages**
2. Under "Source", select **GitHub Actions**
3. The site will deploy automatically on the next push

Your site will be live at `https://YOUR_USERNAME.github.io/YOUR_REPO/`

### 3. Buy and Connect a Custom Domain

**Recommended registrars** (best value, no upselling):
- [Cloudflare Registrar](https://www.cloudflare.com/products/registrar/) — at-cost pricing, great DNS
- [Namecheap](https://www.namecheap.com/) — good prices, easy interface

**To connect your domain:**

1. Buy the domain (e.g., `bencogan.com`)
2. At your registrar's DNS settings, add these records:

| Type  | Name | Value                        |
|-------|------|------------------------------|
| A     | @    | 185.199.108.153              |
| A     | @    | 185.199.109.153              |
| A     | @    | 185.199.110.153              |
| A     | @    | 185.199.111.153              |
| CNAME | www  | YOUR_USERNAME.github.io      |

3. In your GitHub repo: **Settings → Pages → Custom domain** — enter your domain
4. Check "Enforce HTTPS" once the DNS propagates (takes up to 24 hours)
5. Update `baseURL` in `hugo.toml` to your domain:

```toml
baseURL = "https://bencogan.com/"
```

## Writing New Posts

### Create a new post

Create a new Markdown file in `content/posts/`:

```bash
# Using Hugo CLI (if installed locally):
hugo new content posts/my-new-essay.md

# Or just create the file manually:
touch content/posts/my-new-essay.md
```

### Post format

Every post starts with front matter:

```markdown
---
title: "The Title of Your Essay"
subtitle: "An optional subtitle"
date: 2026-02-20
tags: ["philosophy", "startups"]
summary: "A one-line description that appears on the homepage."
---

Your essay content in Markdown goes here...
```

### Publish

1. Write your post as a `.md` file in `content/posts/`
2. Make sure `draft: true` is **removed** (or set to `false`)
3. Commit and push:

```bash
git add content/posts/my-new-essay.md
git commit -m "New post: My New Essay"
git push
```

The site will rebuild and deploy automatically in about 30 seconds.

## Local Development

To preview the site locally before publishing:

```bash
# Install Hugo: https://gohugo.io/installation/
hugo server --buildDrafts
```

Then open `http://localhost:1313` in your browser. Changes auto-reload.

## Structure

```
bencogan-site/
├── content/
│   ├── about/index.md      ← Your about page
│   └── posts/              ← Your essays go here
│       └── my-essay.md
├── themes/writer/          ← Custom theme
├── hugo.toml               ← Site configuration
└── .github/workflows/      ← Auto-deploy config
```

## Customization

- **Site title & description**: Edit `hugo.toml`
- **About page**: Edit `content/about/index.md`
- **Colors & fonts**: Edit `themes/writer/static/css/style.css` (look for `:root` variables)
- **Navigation links**: Edit the `[menu]` section in `hugo.toml`
