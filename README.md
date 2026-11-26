# 2lus Preview — public static artifacts only

This repository contains **only the compiled, public HTML/CSS article-design preview**. The full 2lus Java / React / SQL / Docker source remains in the separate **private** `hrdtimoo-rgb/2lus` repository.

Public pages currently included:
- `/index.html` — preview home
- `/articles/iceland-complete-guide/` — approved Iceland article layout
- `/articles/busan-3-day-first-timer/` — approved Busan article layout

The pages are static design demonstrations, **not** the functional 2lus frontend. They cannot provide login, short links, uploads, Admin functions, API access or real DB data. They contain `noindex,nofollow,noarchive` because the official SEO site is https://2lus.cc/. The preview content is **publicly readable** even when the private source repository is not.

## Enable the free GitHub Pages website (owner setting)

Open **Settings → Pages** in this repository:

1. Under **Build and deployment**, set **Source = Deploy from a branch**.
2. Set **Branch = main**, **Folder = / (root)**.
3. Click **Save**.
4. Verify Pages completed successfully; then open https://hrdtimoo-rgb.github.io/2lus-preview/.

Pages is not enabled merely by committing HTML. A 404 before this setting succeeds is expected.

## Future synchronization

The private source repository contains `scripts/build-pages-preview.py`, which exports **only** exact allowlisted, previously approved travel article blobs. After an owner configures its Actions secret `PREVIEW_REPO_TOKEN` (a fine-grained PAT with **Contents: Read and write** on **only** `2lus-preview`), the private GitHub Actions workflow can push the generated HTML/CSS to this public repository.

**Never** copy the entire private repository or its source archives to `2lus-preview`, and never commit a token. Changes to draft JSON require independent approval before they may appear in this public site.
