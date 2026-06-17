# Setup Guide — Get Your Site Live

This walks you through publishing your site for the first time. Total time: about 15–20 minutes. You only do this once.

## Step 1 — Create the repository on GitHub

1. Log into GitHub.
2. Click the **+** in the top right → **New repository**.
3. Name it **exactly**: `yourusername.github.io` (replace `yourusername` with your actual GitHub username). This exact naming is what makes GitHub give you a free website automatically.
   - Example: if your username is `nsnandvanshi`, the repo must be named `nsnandvanshi.github.io`.
4. Set it to **Public**.
5. Do **not** check "Add a README" — leave it empty.
6. Click **Create repository**.

## Step 2 — Upload these files

The easiest way the first time, with no command line at all:

1. On your new (empty) repository page, click **uploading an existing file**.
2. Drag in **every file and folder** from this project, keeping the folder structure intact (the `_layouts`, `_includes`, `_books`, `_posts`, `assets`, `books`, and `blog` folders, plus `index.html` and `_config.yml`).
3. Scroll down, write a commit message like "Initial site", and click **Commit changes**.

GitHub's drag-and-drop uploader preserves folder structure as long as you drag whole folders in, not just files. If it doesn't accept folders directly in your browser, the alternative is using GitHub Desktop (free) or the `git` command line — see Step 5 below for those commands, since you said you're open to learning them.

## Step 3 — Set the homepage URL in `_config.yml`

Open `_config.yml` in your repo (click it, then the pencil/edit icon).

If your repo is named `yourusername.github.io`, leave `baseurl` as an empty `""`. If you named it anything else, set `baseurl: "/your-repo-name"`.

## Step 4 — Turn on GitHub Pages

1. In your repository, go to **Settings** → **Pages** (left sidebar).
2. Under "Build and deployment," set **Source** to **Deploy from a branch**.
3. Set branch to **main** and folder to **/ (root)**.
4. Click **Save**.

Your site will be live in 1–2 minutes at `https://yourusername.github.io`.

## Step 5 — Set up the email signup (Formspree, free)

1. Go to formspree.io and sign up free (no credit card).
2. Create a new form. Formspree gives you a **Form ID** (a string of letters/numbers in your form's endpoint URL).
3. Open `_config.yml` in your repo and replace `YOUR_FORM_ID_HERE` with that ID.
4. Commit the change. Test the signup form on your live site — Formspree will send the first submission to your email for confirmation; click confirm.

The free Formspree plan allows 50 submissions per month, which resets every month — plenty for getting started. If you outgrow it, Mailchimp's free tier (up to 500 contacts) is a common next step, but isn't needed yet.

## Step 6 (optional) — Working from your computer instead of the browser

If you want to write posts in a text editor on your computer and publish from there instead of GitHub's website, install **Git** (free) and **GitHub Desktop** (free, has a visual interface — easier than typing commands) or use the command line:

```
git clone https://github.com/yourusername/yourusername.github.io.git
cd yourusername.github.io
# make your edits in a text editor (e.g. VS Code, also free)
git add .
git commit -m "Add new blog post"
git push
```

Every time you `git push`, GitHub rebuilds your live site automatically within about a minute. No separate "publish" button needed.

## Updating your bio, logo, or links later

- **Bio text**: edit `index.html`, the paragraphs inside `<div class="about-body">`.
- **Logo**: replace `/assets/images/logo.jpg` with a new file of the same name, or update the filename references in `_layouts/default.html` and `_layouts/book.html`.
- **Instagram / Medium links**: edit the `social:` section at the top of `_config.yml`.
