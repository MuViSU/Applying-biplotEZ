# Applying biplotEZ

A Quarto website showcasing how the [biplotEZ](https://muvisu.github.io/biplotEZ/) R package is applied to interesting data sets, aimed at readers with no biplot background. Run within MuViSU, funded by NiTheCS.

## Structure

| Path | Purpose |
|---|---|
| `_quarto.yml` | Site configuration and navbar (About, Applications, Who we are) |
| `index.qmd` | Landing page: wordmark and Learn more button |
| `about.qmd` | About page |
| `applications.qmd` | Listing page that collects every post in `applications/` |
| `applications/<post>/index.qmd` | One application per folder |
| `applications/_template/index.qmd` | Copy this to start a new post (it is a draft, so it is not published) |
| `who-we-are.qmd` | MuViSU and the team |
| `theme.scss`, `styles.css` | Look and feel, colours from the logo |

## Adding an application

1. Copy `applications/_template` to `applications/<short-name>`.
2. Edit `index.qmd`: set the title, description, author, date and categories in the YAML header, and remove `draft: true`.
3. Write the post. Keep the R code in chunks; it is folded by default.
4. Preview with `quarto preview` and render with `quarto render`.

## Requirements

- [Quarto](https://quarto.org) 1.4 or later
- R with the `knitr`, `rmarkdown` and `ggplot2` packages
- The development version of biplotEZ from GitHub: `remotes::install_github("MuViSU/biplotEZ")`

## Rendering

```bash
quarto render
```

The site is written to `_site/`. Rendered R output is cached in `_freeze/`, so posts only re-execute when their source changes.
