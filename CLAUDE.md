# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Jialin Li's personal academic website (https://melancholy123.github.io), adapted from Jon Barron's template (https://jonbarron.info/). It is a static site deployed by GitHub Pages directly from the `master` branch. There is no build system, package manager, linter, or test suite.

## Development

- Preview the main page by opening `index.html` in a browser, or serve locally with `python3 -m http.server`.
- The blog is the exception: `blog.html` and `_posts/*.md` use Jekyll front matter and Liquid tags (`site.posts` loop), which only render through GitHub Pages' Jekyll build. To preview the blog locally you would need `jekyll serve`; plain file serving will not render it. Note there is no `_config.yml` or `_layouts/` in the repo (a minimal config was intentionally removed in commit 371ad40), so the blog relies entirely on GitHub Pages' default Jekyll processing.
- Deployment is just `git push` to `master`; GitHub Pages publishes automatically.

## Structure and conventions

- `index.html` is the entire homepage: bio, publications, academic service, and teaching are hand-edited HTML tables (Jon Barron template style). Content updates (new papers, teaching entries, etc.) mean editing these tables directly, following the existing row markup. Publication images go in `images/`, the CV lives at `data/JialinLi_CV.pdf`.
- `stylesheet.css` is the only stylesheet for the homepage.
- `mipnerf/`, `mipnerf360/`, `zipnerf/` are self-contained project-page templates carried over from the Barron template (each with its own `css/`, `js/`, `img/`). They still reference jonbarron.info assets and are kept as templates for future project pages; they are not part of Jialin's own content.
- `CNAME` controls the custom domain for GitHub Pages.
