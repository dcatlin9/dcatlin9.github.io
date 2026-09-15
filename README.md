# dcatlin9.github.io — setup

This folder is a minimal, ready-to-publish Jekyll blog: `_config.yml`, an `index.md` that lists posts (via the built-in `minima` theme, which GitHub Pages supports natively — no Gemfile or local Ruby install needed), and your first post in `_posts/`.

## 1. Create the repo on GitHub

Go to github.com/new and create a new **public** repository named exactly:

```
dcatlin9.github.io
```

That exact name (your username + `.github.io`) is what makes GitHub treat it as your personal site rather than a project page. Leave it empty — don't initialize with a README, license, or .gitignore; you already have this folder's contents.

## 2. Push this folder

From inside this folder on your machine:

```
git init
git add .
git commit -m "Initial blog: one year into the EMBA"
git branch -M main
git remote add origin https://github.com/dcatlin9/dcatlin9.github.io.git
git push -u origin main
```

## 3. Confirm it's live

GitHub Pages builds automatically after the push — usually live within a minute or two at:

```
https://dcatlin9.github.io
```

Your first post will be at:

```
https://dcatlin9.github.io/2026/09/15/one-year-into-the-emba/
```

If nothing's live after a few minutes, check **Settings → Pages** on the repo — it should show "Your site is live at…"; if it says Pages isn't enabled, set the source to the `main` branch, root folder, and save.

## Publishing post 2 (and beyond)

Drop a new file in `_posts/` named `YYYY-MM-DD-your-slug.md` with the same front matter block (`layout: post`, `title`, `date`, `categories`), commit, and push — no other setup required. The filename's date and slug become the post's URL, matching the `permalink` pattern already set in `_config.yml`.

## If you actually publish on a different date than 2026-09-15

Jekyll uses the date in two places — the filename prefix and the `date:` line in the post's front matter — and they need to match each other. If you push later than today, rename the file and update the front matter date to match, or the post may not appear where you expect.
