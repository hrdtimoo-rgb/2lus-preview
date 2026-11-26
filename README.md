# 2lus Preview

**Public design-preview artifacts only.** The actual 2lus source code remains in a separate **private** GitHub repository.

This repository stores generated static HTML/CSS for an article-layout preview. It does not include backend source, frontend source, database contents, credentials, user uploads, or unpublished JSON drafts.

The preview is a design mock, not a fully functional React/Spring Boot site. It intentionally does not provide login, short links, file uploads or live API functions. Official SEO and the live application remain at https://2lus.cc/.

## Publish this site

GitHub → this repository → **Settings → Pages** → **Build and deployment → Source: GitHub Actions**. Then inspect the **Deploy 2lus preview (public artifacts only)** workflow in Actions. If your GitHub Pages setup uses **Deploy from a branch**, use **main / (root)** instead.

Expected URL after successful Pages deployment: https://hrdtimoo-rgb.github.io/2lus-preview/ . This URL is NOT active merely because repository files exist.

All preview content here is public and should be treated as such, even though search engines are asked not to index it.

## Source-of-truth

Private source repository: `hrdtimoo-rgb/2lus`; only explicitly reviewed static preview artifacts should be copied from it. To enable automatic updating across repositories, configure an owner-scoped publishing token in the private repository; never place that credential here.
