# Repository Guidelines

## Project Structure & Module Organization
This repository contains the Orbit résumé theme built with Jekyll. Site-wide settings live in `_config.yml`, while personal content is centralized in `_data/data.yml`. Layout shells sit in `_layouts/`, reusable fragments in `_includes/`, and SCSS partials in `_sass/` with color skins under `_sass/skins/`. Static assets (images, fonts, scripts) reside in `assets/`. The primary entry points are `index.html`, `print.html`, and `blind.html`, each pulling shared sections through includes. Local container settings are captured in `docker-compose.yml`.

## Build, Test, and Development Commands
- `docker-compose up`: serve the site in a disposable container at `http://localhost:4000` with auto-regeneration.
- `bundle install`: install Ruby gems from the `Gemfile` before running any Jekyll command.
- `bundle exec jekyll serve --livereload`: run the development server directly on your machine with incremental rebuilds.
- `bundle exec jekyll build`: create the production `_site/` output and fail fast on Liquid, Markdown, or data errors.
- `bundle exec jekyll doctor`: scan for configuration and front matter issues that block GitHub Pages deployments.

## Coding Style & Naming Conventions
Use two-space indentation for Liquid, HTML, and YAML. Keep YAML keys lowercase with hyphen separators to match existing blocks in `_data/data.yml`. SCSS files follow a modular structure (`_base.scss`, `_utilities.scss`); add new rules as dedicated partials and import them from `_default.scss`. Name includes with descriptive kebab-case, limit complex Liquid logic inside templates, and prefer data-driven sections sourced from `_data/`.

## Testing Guidelines
Before committing, run `bundle exec jekyll build` (or watch the Docker logs) to ensure the site compiles cleanly. Execute `bundle exec jekyll doctor` after touching `_config.yml` or introducing new collections. For UI changes, review `index.html`, `print.html`, and `blind.html` in the browser to confirm consistent layouts.

## Commit & Pull Request Guidelines
Follow the conventional commit style already in history (`feat:`, `fix:`, `chore:`) using concise, imperative summaries. Group related edits together and avoid bundling content, styling, and tooling changes in a single commit. Pull requests should outline the change, reference related issues, and include before/after screenshots for visible updates. Highlight any new configuration flags or deployment steps so maintainers can adjust their GitHub Pages setup without surprises.

## Configuration Tips
Set the preferred hostname in `CNAME` when deploying to a custom domain. Adjust `baseurl` and theme options in `_config.yml`, and toggle palette variants by importing the desired skin from `_sass/skins/`. Keep secrets out of the repo—use environment overrides or GitHub Pages settings instead of committing sensitive values.

## Repository Origin
This repository was forked from the original Orbit theme project and customized to include the maintainer's personal résumé content.
