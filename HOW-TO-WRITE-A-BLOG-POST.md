# How to Write a Blog Post

Every post is one text file in the `_posts` folder, written in plain text with light formatting (called Markdown). No code involved.

## Step 1 — Name the file correctly

The filename must start with the date, then a short title, like this:

```
YYYY-MM-DD-a-short-title.md
```

Example: writing a post called "On Writing Heartbreak" on June 20, 2026:
```
2026-06-20-on-writing-heartbreak.md
```

This date is what controls the order posts appear in — newest first.

## Step 2 — Fill in this template

```
---
title: "Your Post Title Here"
date: 2026-06-20
---

Write your post here in plain text.

Leave a blank line between paragraphs — that's all you need to do to start a new paragraph.
```

## Step 3 — Basic formatting (all optional)

While writing the body of the post, you can use:

- `*italic text*` → *italic text*
- `**bold text**` → **bold text**
- `## A Heading` → makes a section heading inside the post
- `> A quote` → indents and styles it as a quote
- To add an image: `![description](/assets/images/blog/your-image.jpg)` — upload the image to `assets/images/blog/` first (create that folder if it doesn't exist yet)

You don't need to use any of these — plain paragraphs work fine on their own.

## Step 4 — Save and publish

If editing directly on GitHub's website: create the file inside `_posts`, paste in your filled-out template, scroll down, write a commit message like "Add new post," click **Commit changes**. Live within about a minute.

If working from your computer:
```
git add .
git commit -m "Add new post"
git push
```

Your post will automatically appear at the top of the Blog page and in the homepage preview — no other file needs to change.
