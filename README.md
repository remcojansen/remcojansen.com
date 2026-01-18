# remcojansen.com

Personal website built with [Hugo](https://gohugo.io) and the
[Congo](https://jpanther.github.io/congo/) theme (profile layout), installed as a Hugo Module.

## Requirements

- [Hugo](https://gohugo.io/installation/) (extended version)
- [Go](https://go.dev/dl/) (required by Hugo Modules to fetch the theme)

## Local development

```bash
hugo server -D
```

Visit `http://localhost:1313/`. The server watches content, config, and asset changes and
reloads automatically.

## Building

```bash
hugo
```

Outputs the static site to `public/`. Use `hugo --minify` for a minified production build.

## Project structure

- `content/` — site pages (`about.md`, `projects.md`, `skills.md`, homepage `_index.md`)
- `config/_default/` — Congo theme configuration (site, menus, params, languages, markup)
- `assets/img/` — profile photo used on the homepage
- `assets/css/custom.css` — small CSS override (badge layout fix); see file header for details
- `static/` — favicons, `site.webmanifest`, and `CNAME` (custom domain for GitHub Pages)
- `go.mod` / `go.sum` — Hugo Modules dependency manifest (pins the Congo theme version)

## Updating the theme

```bash
hugo mod get -u
hugo mod tidy
```
