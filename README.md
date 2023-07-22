# Novelist Hugo theme

[![Netlify Status](https://api.netlify.com/api/v1/badges/87c7da96-8f24-4277-bb4d-6202b039ebdc/deploy-status)](https://app.netlify.com/sites/hugo-novelist/deploys)

Novelist is content focused, minimal theme for Hugo, suitable for fanfiction writings. It aims at a feature set similar to [Archive of Our Own](https://archiveofourown.org/). **Not production-ready yet.**

Demo: [https://hugo-novelist.netlify.app/](https://hugo-novelist.netlify.app/)

![Theme screenshot](screenshot1.png)

![Theme screenshot](screenshot2.png)

## Building guides

### Local

Build your own site: (path: `/your-site/`)

```sh
hugo server --buildDrafts --disableFastRender
```

Build the example site: (path: `/hugo-novelist/`)

```sh
cd exampleSite
hugo serve --buildDrafts --disableFastRender --themesDir .. --theme .
```

### Netlify

Example `netlify.toml`:

Build your own site: (from your own site repo)

```toml
[build]
publish = "public"
command = "hugo --gc --minify"

[context.production.environment]
HUGO_VERSION = "0.115.2"
HUGO_ENV = "production"
HUGO_ENABLEGITINFO = "true"
```

Build the example site: (from this repo) see [`./netlify.toml`](https://github.com/loikein/hugo-novelist/blob/main/netlify.toml)


## Fork notes

### TODO

- Hugo
    + [x] Clean up temp files
    + [x] Add `theme.toml`
    + [x] Clean up layout code
    + [x] Set up `exampleSite` \& deploy
    + [ ] Add i18n
    + [ ] Better archetypes
- Site features
    + [x] Add rating system
        * [ ] Fix rating focus style
    + [x] Add multi-chapter support
        * [x] Section permalink shenanigan
    + [x] Taxonomies: fandoms, relationships, characters
    + [x] Add age warning modal for M \& E rated writings
    + [x] Add archive pages (achieved by restoring section lists)
    + [ ] Add full-text search
    + [ ] Support multi-line summary
- Style
    + [x] Centre the main tag
    + [x] Adjust date format
    + [x] Custom `<hr>` glyph
    + [ ] Dark mode
    + [ ] Do something about multi-line summary style \(and all summary style\)
- Layout
    + [ ] Add series layout
    + [ ] Add prev/next page buttons (maybe only for multi-chapter)
    + [ ] Add beginning notes and end notes
- Meta tags
    + [x] Add jump link to external sources
- Others
    + [ ] (a11y) Add jump to main button
    + [ ] Get the extra privacy version of the social shortcodes
- Probably won't
    + Add pagination
    + Do something about the code fence styling
    + Support LaTeX


## Features

- Minimalistic, clean and simple design
- Perfect for writers
- Content focused
- System fonts
- Anchor links
- ~~NO JS!~~ This is voided by the addition of age warning modals. Readers can still disable JS which skips the modal, but nothing else will be affected.
- ~~AAA, 100/100 scores on Lighthouse, Gmetrix and Webpagetest~~ \(Untested\)
- Responsive design
- Tags and tag pages
- ~~Inline CSS~~
- Atom feed
- Json feed
- ~~Related content (internal links)~~
- ~~Sass~~ SCSS
- SEO optimized (Twitter cards, Facebook Open Graph, Schema.org)


## Site customisation

You can customise the favicon by creating a `favicon.png` file under `/site/static/`.

Customisation options in `config.yaml`:

- `params.customCSS` bool: Turn on/off site-specific custom CSS. All `.css` files located under `/site/assets/css/` will be included. See the example site folder for an example (not turned-on).
- `params.enableRatings` bool: Site-wide switch for turning on/off the AO3 rating system. Only controls the display. You can still save the ratings for your own reference purpose.
- `params.description` string: The subtitle under your site title.
- `params.dateFormat` string: Enter any format of the date `Monday, Jan 2, 2006` that is compatible with [Go's Time Format function](https://pkg.go.dev/time#example-Time.Format). See [Hugo documentation](https://gohugo.io/functions/format/#hugo-date-and-time-templating-reference) for a list of simple examples.
- `params.showSummary` bool: Controls whether the article lists automatically show the beginning of the article (140 characters) or not.
- `params.lowVisionSymbols` bool: Controls whether to use the low vision version of ratings symbols or not.
- `params.hrGlyph` string: Glyph used for the `<hr>` element. The quotation marks are required. Also, if you want to use Unicode Characters, you must type an extra slash like this: `"\\2756"`.


## Pages customisation

In addition to the [usual markdown front matter](https://gohugo.io/content-management/front-matter/) \(note certain entries are not supported such as `categories` and `weight`\), you can also specify fandoms, relationships, characters, tags, ratings and 1 external link.

For an all-in-one example, see [`./exampleSite/content/writing/markdown-syntax.md`](https://github.com/loikein/hugo-novelist/blob/main/exampleSite/content/writing/markdown-syntax.md).

### `ratings`

For each writing \(for multi-chapters only the `_index` file counts\), you can choose from: \(Quotation marks are required. Can be single quote if you want.\)

- rating:
    + `"general-audience"`
    + `"teen"`
    + `"mature"`
    + `"explicit"`
    + `"no"`
- warning: 
    + `"choosenotto"`
    + `"yes"`
    + `"no"`
- category:
    + `"femslash"`
    + `"het"`
    + `"gen"`
    + `"slash"`
    + `"multi"`
    + `"other"`
    + `"no"`
- complete:
    + `"no"`
    + `"yes"`

YAML example:

```yaml
ratings:
  rating: "general-audience"
  warning: "choosenotto"
  category: "slash"
  complete: "yes"
```

TOML example:

```toml
[ratings]
rating = "teen"
warning = "choosenotto"
category = "femslash"
complete = "no"
```


## License/copyright acknowledgements

### Upstream codebase

This theme was originally authored by Ronalds Vilciņš and distributed under the MIT License \([ronv/simplist: Content focused, minimal theme for Hugo](https://github.com/ronv/simplist)\).


### This repo

This repository is distributed under the GNU General Public License v2.0 or any later version \([per compatibility matrix of GNU licenses](https://www.gnu.org/licenses/gpl-faq.en.html#AllCompatibility)\).


### Age warning modal

This theme uses the adult caution message from the [otwarchive repository](https://github.com/otwcode/otwarchive/) under the GNU General Public License v2.0 only, no changes made.


### Rating system

[`./exampleSite/content/rating-description.md`](https://github.com/loikein/hugo-novelist/blob/main/exampleSite/content/rating-description.md):

This theme uses the symbol system from the [otwarchive repository](https://github.com/otwcode/otwarchive/) under the GNU General Public License v2.0, with the following changes:

- Removing the external work mark and the completion status unknown mark \(because presumably all the works that you post here are your originals, and you know whether they are completed or not\);
- Enlarging the "Other relationships" icon to make it the same size with others.
