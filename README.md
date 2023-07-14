# Novelist Hugo theme

[![Netlify Status](https://api.netlify.com/api/v1/badges/87c7da96-8f24-4277-bb4d-6202b039ebdc/deploy-status)](https://app.netlify.com/sites/hugo-novelist/deploys)

Novelist is content focused, minimal theme for Hugo, suitable for fanfiction writings. It aims at a feature set similar to [Archive of Our Own](https://archiveofourown.org/).

Demo: [https://simplist-hugo.netlify.app/](https://simplist-hugo.netlify.app/)

![Theme screenshot](screenshot1.png)

![Theme screenshot](screenshot2.png)

## Fork notes

### TODO

- Housekeeping
    + [x] Clean up temp files
    + [x] Add `theme.toml`
    + [x] Clean up layout code
    + [ ] Add i18n
    + [x] Set up `exampleSite` \&\& deploy
- Style tweaks
    + [x] Centre the main tag
    + [x] Adjust date format
    + [x] Add rating system
    + [ ] Do something about the code fence styling
- New functionalities
    + [x] Add multi-chapter support
    + [ ] Add age confirmation modal for M \& E rated writings
    + [ ] Add prev page next page buttons
    + [ ] Add archive pages
    + [x] More taxonomies \(fandoms, characters\)
    + [ ] Dark mode
    + [ ] Add jump to main button
    + [ ] Get the extra privacy version of the social shortcodes
    + [ ] Add searching
- Fix new bugs
    + [ ] Section permalink shenanigan
- ...

### Rating system

Copyright acknowledgement: [`./exampleSite/content/rating-description.md`](https://github.com/loikein/hugo-novelist/blob/main/exampleSite/content/rating-description.md)

```md
This theme follows the [symbol system used on AO3](https://archiveofourown.org/help/symbols-key.html), with the following changes:

- Removing the external work mark and the completion status unknown mark \(because presumably all the works that you post here are your originals, and you know whether they are completed or not\);
- Enlarging the "Other relationships" icon to make it the same size with others.

All the graphics \(default large and lvy versions\) and words below and within all tagging areas were taken from the [otwarchive repository](https://github.com/otwcode/otwarchive/), used under GNU General Public License v2.0. All rights reserved by the Organization for Transformative Works.
```

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

YAML front matter example:

```yaml
ratings:
  rating: "general-audience"
  warning: "choosenotto"
  category: "slash"
  complete: "yes"
```

TOML front matter example:

```toml
[ratings]
rating = "teen"
warning = "choosenotto"
category = "femslash"
complete = "no"
```

## Features

- Minimalistic, clean and simple design
- Perfect for writers
- Content focused
- System fonts
- Anchor links
- NO JS!
- ~~AAA, 100/100 scores on Lighthouse, Gmetrix and Webpagetest~~ \(Untested\)
- Responsive design
- Tags and tag pages
- ~~Inline CSS~~
- Atom feed
- Json feed
- ~~Related content (internal links)~~
- ~~Sass~~ SCSS
- SEO optimized (Twitter cards, Facebook Open Graph, Schema.org)

## Site Customisation

In `config.yaml`:

- `params.description` string: The subtitle under your site title.
- `params.dateFormat` string: Enter any format of the date `Monday, Jan 2, 2006` that is compatible with [Go's Time Format function](https://pkg.go.dev/time#example-Time.Format). See [Hugo documentation](https://gohugo.io/functions/format/#hugo-date-and-time-templating-reference) for a list of simple examples.
- `params.showSummary` bool: Controls whether the article lists show the beginning of the article (140 words) or not.
- `params.lowVisionSymbols` bool: Controls whether to use the low vision version of ratings symbols or not.
