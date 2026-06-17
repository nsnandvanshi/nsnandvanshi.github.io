# How to Add a Book

Every book is one file in the `_books` folder. To add a new one:

## Step 1 — Add the cover image (optional but recommended)

Upload your cover image into `assets/images/books/`. Name it something simple with no spaces, e.g. `half-light.jpg`.

If you don't have a cover image yet, skip this — the page will show the title in its place until you add one.

## Step 2 — Create the book file

In the `_books` folder, create a new file. Name it after the book, all lowercase, words separated by hyphens, ending in `.md`.

Example: for "Half Light," name the file `half-light.md`.

## Step 3 — Fill in this template exactly

Copy everything below into your new file and fill in the blanks. Keep the three dashes (`---`) exactly where they are — they separate the book's details from its description.

```
---
title: "BOOK TITLE HERE"
description: "One short sentence about the book — this shows on the book grid/cards."
cover: /assets/images/books/YOUR-COVER-FILENAME.jpg
order: 2
links:
  - store: Amazon
    url: "PASTE YOUR AMAZON LINK HERE"
  - store: Google Play Books
    url: "PASTE YOUR GOOGLE PLAY LINK HERE"
  - store: Apple Books
    url: "PASTE YOUR APPLE BOOKS LINK HERE"
  - store: Flipkart
    url: "PASTE YOUR FLIPKART LINK HERE"
---

Write the full description here — a paragraph or two for the book's own page. This can be longer and more detailed than the one-line description above.
```

### Notes on the template

- `order` controls what sequence books appear in (1 first, 2 second, and so on). Use any numbers you like, just keep them unique.
- If a book isn't on a particular store, delete that store's two lines entirely (the `- store:` line and the `url:` line below it) rather than leaving the link blank.
- To add more stores beyond the four listed, copy the pattern:
  ```
  - store: Store Name
    url: "link"
  ```
- Don't remove the cover line even if you have no image yet — instead just leave the whole `cover:` line out and the site will handle it gracefully.

## Step 4 — Save and publish

If editing directly on GitHub's website: scroll down, write a commit message like "Add Half Light," click **Commit changes**. Your site updates automatically within about a minute.

If working from your computer: save the file, then run:
```
git add .
git commit -m "Add Half Light"
git push
```
