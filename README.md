# racenteno.github.io

Personal academic website for Raquel Centeno, built with [Jekyll](https://jekyllrb.com)
and served by GitHub Pages at <https://racenteno.github.io>.

The design follows the [academicpages](https://github.com/academicpages/academicpages.github.io)
template (itself derived from [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes)
by Michael Rose): a masthead nav, a sticky author profile sidebar, and a single
content column. Nothing is pulled in from a theme gem — every layout, include,
and stylesheet lives in this repository, so anything can be edited directly.

## Editing the site

| What you want to change | File |
| --- | --- |
| Name, bio, sidebar links, CV link, site metadata | `_config.yml` |
| Which pages appear in the top nav | `_data/navigation.yml` |
| Home page text | `index.md` |
| CV / Research / Teaching / Public Writing pages | `_pages/*.md` |
| Colors, fonts, spacing | the `:root` variables at the top of `assets/css/main.css` |
| Page skeleton (head, masthead, sidebar, footer) | `_layouts/`, `_includes/` |

### Adding a page

Create a markdown file in `_pages/` with front matter:

```yaml
---
title: "Publications"
subtitle: "Optional line under the title"
permalink: /publications/
author_profile: true
---
```

Then add it to `_data/navigation.yml` so it shows up in the nav.

### Adding an image

Put the file in `images/` and use the figure include:

```liquid
{% include figure.html img="my-photo.jpg" alt="Description" caption="Optional caption." width="300px" %}
```

`class="align-right"` or `class="align-left"` floats the figure beside the text.

### Sidebar links

The sidebar renders only the fields that are filled in under `author:` in
`_config.yml`. Three are currently blank and need real values:
`googlescholar`, `orcid`, and `bluesky`. Delete any you don't want.

Icons come from [Font Awesome 6](https://fontawesome.com/icons) via CDN; the
`fa-...` class names in `_includes/author-profile.html` can be swapped for any
other icon in that set.

## Running locally

```bash
bundle exec jekyll serve
# or, without a Gemfile:
jekyll serve
```

The site then builds to `_site/` and is served at <http://localhost:4000>.
Pushing to `main` is enough to publish — GitHub Pages builds it automatically.

## Credits

Content © Raquel Centeno, licensed [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
Design after [academicpages](https://github.com/academicpages/academicpages.github.io)
and [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) (MIT).
