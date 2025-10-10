# Personal Resume Site

This repository hosts my personal resume, built with Jekyll on top of the Orbit theme by Xiaoying Riley. The layout, data model, and styling originate from the upstream project, while the content has been rewritten to describe my own professional experience.

## Local Preview

You can review and iterate on the site locally either with Docker or a native Ruby environment.

### Using Docker
- Requirements: Docker with the Compose plugin (v2) installed locally.
- Run: `docker compose up`
- View: Open `http://localhost:4000` in your browser. Content changes may take a few seconds to appear.
- Legacy note: If you still rely on the standalone Compose v1 binary, use `docker-compose up` instead.

### Using Ruby Directly
- Requirements: Ruby and Bundler available in your environment.
- Install dependencies: `bundle install`
- Start the server: `bundle exec jekyll serve`
- View: Browse to `http://localhost:4000` to inspect the local build.

## Editing Content
- `_data/data.yml` centralizes profile details, work history, education, and projects.
- Media assets live under `assets/`; update or add images and downloads here.
- Layout tweaks belong in `_layouts/` and `_includes/`, while style updates go into `_sass/` partials.

## Theme Customization
- Orbit color skins reside in `_sass/skins/`. Switch palettes by changing the import in `_sass/_default.scss`.
- Add bespoke styling by creating a new partial under `_sass/` and importing it from `_sass/_default.scss`.

## License and Credits
- Upstream theme: [Orbit by Xiaoying Riley](https://themes.3rdwavemedia.com/).
- This fork replaces the stock demo data with my personal resume content and adjusts supporting assets.
- All modifications comply with the repository's license; see `LICENSE.md` for details.
