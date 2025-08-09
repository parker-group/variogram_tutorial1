# Variogram Tutorial (R)

A short, self-contained tutorial for building experimental and fitted semivariograms in R using **gstat** and the built-in `meuse` dataset (no external files).

## What you'll learn
- Nugget, sill, range (what they mean and how to read them)
- Empirical semivariogram computation
- Model fitting (exponential example)
- Directional variograms (anisotropy check)

## Quick start

### A) View-only (no R)
Open the rendered HTML tutorial:
- `variogram_tutorial.html` (in this repo), or
- GitHub Pages link (once enabled in **Settings → Pages**)

### B) Hands-on (R installed)
In R:
```r
install.packages(c("gstat","sp","sf","rmarkdown"))  # first time
rmarkdown::render("variogram_tutorial.Rmd", output_format = "html_document")
