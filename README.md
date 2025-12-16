# Frank Tao · Personal Site

This repository contains the source for [frank-tao.github.io](https://frank-tao.github.io), a lightweight personal site and blog powered by [Jekyll](https://jekyllrb.com/) with the [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) theme. The site hosts Toastmasters notes, engineering journals, and links to current projects.

## Highlights
- Clean GitHub Pages deployment via the `Build and Deploy` workflow in `.github/workflows/pages-deploy.yml`
- First-class Markdown authoring with syntax highlighting, SEO tags, and RSS feed support
- Pinned posts, featured images, and social cards for share-ready articles
- Progressive web app (PWA) shell so the site is installable and works offline

## Local Development
1. Install [Ruby](https://www.ruby-lang.org/en/downloads/) and [Bundler](https://bundler.io/).
2. Install dependencies:
   ```bash
   bundle install
   ```
3. Run the local server with live reload:
   ```bash
   bundle exec jekyll serve --livereload
   ```
4. Browse to `http://127.0.0.1:4000` to preview the site.

## Writing
- New posts live in `_posts/` and use the filename format `YYYY-MM-DD-title.md`.
- Drafts can stay under `_drafts/` until they are ready; start Jekyll with `bundle exec jekyll serve --drafts` to preview them.
- Long-form assets (images, diagrams) sit under `assets/<year><month><day>/` and are referenced via front-matter `image:` blocks.

## Deployment
Every push to `main` automatically runs tests, builds the static site, and publishes it to GitHub Pages. No manual steps are required.
