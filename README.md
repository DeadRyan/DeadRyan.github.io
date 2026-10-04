# KROTAL Community

Static community/forum-style GitHub Pages site for the **KROTAL** project.

## What this is

A free, no-backend "forum" front page:

- **Home / announcements** → `index.html`
- **Discussion threads** → GitHub Discussions (the actual forum)
- **Docs / about** → linked pages

Since GitHub Pages is static-only, the *threads, posts, and replies* live in
**GitHub Discussions**, and this site acts as the styled front door + landing
page that links into them.

## Structure

```
deadryan.github.io/
├── index.html          # home + announcements + links into Discussions
├── about.html          # what KROTAL is
├── docs.html           # documentation index
├── assets/
│   └── style.css       # shared styling
```

## How to deploy

1. Create a repo named exactly `DeadRyan.github.io` (public) on GitHub.
2. Push this folder to it.
3. Enable **Discussions** in the repo settings (Settings → Features → Discussions).
4. Your site goes live at `https://deadryan.github.io`.

## Where the actual forum lives

Replace the placeholder discussion URLs in `index.html` with the real
Discussion category links from your repo. The out-of-the-box categories are:

- 💬 General
- 🙏 Q&A
- 🚀 Announcements
- 💡 Ideas

## Customizing

- Edit `assets/style.css` for colors/branding.
- Edit the `DISCUSS_URL` placeholder links (search for `https://github.com/DeadRyan/KROTAL/discussions`).
- Add your KROTAL logo to `assets/` and reference it in the `<header>`.
