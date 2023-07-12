# Novelist Hugo theme

Novelist is content focused, minimal theme for Hugo, suitable for fanfiction writings. It aims at a feature set similar to [Archive of Our Own](https://archiveofourown.org/).

Demo: [https://simplist-hugo.netlify.app/](https://simplist-hugo.netlify.app/)

![Theme screenshot](screenshot1.png)

![Theme screenshot](screenshot2.png)

## Fork notes

### TODO

- [ ] Housekeeping
    + [x] Clean up temp files
    + [x] Add `theme.toml`
    + [ ] Clean up layout code
    + [ ] Add i18n
    + [ ] Set up `exampleSite` \&\& deploy
- [ ] Style tweaks
    + [x] Centre the main tag
    + [ ] Adjust date format
    + [ ] Add rating system
- [ ] Add searching
- [ ] ...

### Rating system

Icons: [otwarchive/public/images/skins/iconsets](https://github.com/otwcode/otwarchive/tree/master/public/images/skins/iconsets)

Choose among default/low vision? All low vision?

## Features

- Minimalistic, clean and simple design
- Perfect for writers
- Content focused
- System fonts
- Anchor links
- NO JS!
- AAA, 100/100 scores on Lighthouse, Gmetrix and Webpagetest
- Responsive design
- Tags and tag pages
- Inline CSS
- Atom feed
- Json feed
- Related content (internal links)
- Sass
- SEO optimized (Twitter cards, Facebook Open Graph, Schema.org)

## Customisation

In `config.yaml`:

- `params.dateFormat` string: Enter any format of the date `Monday, Jan 2, 2006` that is compatible with [Go's Time Format function](https://pkg.go.dev/time#example-Time.Format). See [Hugo documentation](https://gohugo.io/functions/format/#hugo-date-and-time-templating-reference) for a list of simple examples.
