# ralferlebach GitHub Pages Theme

A small, privacy-friendly Jekyll remote theme for project documentation hosted on GitHub Pages.

## Goals

- visual continuity with `ralferlebach.de`
- one central theme for many project repositories
- keep each project's `README.md` as the single source of documentation
- no external fonts, CDN resources, cookies, analytics, or JavaScript dependencies
- responsive and keyboard-accessible
- good rendering of Markdown, tables, code blocks, screenshots, callouts, and badges
- safe for GitHub Project Pages below `/<repository>/`

## Repository structure

```text
.
├── _includes/
│   ├── head.html
│   ├── project-header.html
│   ├── site-footer.html
│   └── site-header.html
├── _layouts/
│   └── default.html
├── assets/
│   └── css/
│       └── style.scss
├── examples/
│   └── Moodle-ViMiPad-Plugins/
│       ├── _config.yml
│       └── index.md
├── .github/
│   └── workflows/
│       └── theme-check.yml
├── 404.html
├── Gemfile
├── _config.yml
└── README.md
```

## Use from a project repository

Copy the example `_config.yml` and `index.md` into the root of the project repository and adapt the metadata.

The important lines are:

```yaml
remote_theme: ralferlebach/github-pages-theme@main

plugins:
  - jekyll-remote-theme
```

`index.md` keeps `README.md` as the single source of project documentation:

```liquid
---
layout: default
---

{% include_relative README.md %}
```

The theme uses `relative_url` for its assets. Therefore it works both for a user site and for project sites such as:

```text
https://ralferlebach.github.io/Moodle-ViMiPad-Plugins/
```

## Local preview

Install Ruby and Bundler, then:

```bash
bundle install
bundle exec jekyll serve --livereload
```

Open `http://127.0.0.1:4000/`.

## Design tokens

Most visual choices are centralized in `assets/css/style.scss`. Several can also be overridden from a consuming project's `_config.yml`:

```yaml
brand:
  primary: "#162033"
  accent: "#0d6f73"
  accent_hover: "#09565a"
  surface: "#f5f7f8"
```

## Accessibility and privacy

The layout contains:

- a skip link
- semantic `header`, `nav`, `main`, and `footer`
- visible keyboard focus
- sufficient default contrast
- responsive tables and code blocks
- reduced-motion handling
- no third-party web fonts
- no third-party scripts
- no tracking

## License

No license is imposed by this starter. Add the license you want to use for the theme repository.
