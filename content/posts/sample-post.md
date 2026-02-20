---
title: "Your First Post Title Here"
subtitle: "An optional subtitle that appears below the title"
date: 2026-02-20
tags: ["essay"]
draft: true
summary: "This is a sample post to show you how the formatting works. Delete this file and replace it with your own writing."
---

This is a sample post to show you how the site renders your Markdown. Everything below is just a demo of the formatting options available to you.

## How to Write a New Post

Create a new `.md` file in the `content/posts/` folder. Each post starts with front matter — the metadata between the `---` lines at the top:

```yaml
---
title: "Your Title"
subtitle: "Optional subtitle"
date: 2026-02-20
tags: ["essay", "philosophy"]
summary: "A brief description for the homepage."
---
```

Then write your essay in plain Markdown below.

## Formatting You Can Use

Regular paragraphs are just text separated by blank lines. You can use **bold**, *italic*, and [links](https://example.com) as you'd expect.

> Blockquotes look like this. They're useful for pulling out a key idea or quoting someone else.

You can also use lists if you need them, horizontal rules to break up sections, and images with the standard Markdown syntax.

---

When you're ready to publish, remove `draft: true` from the front matter (or just omit it), push to GitHub, and the site will update automatically.
