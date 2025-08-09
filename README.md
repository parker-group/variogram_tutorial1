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
- https://parker-group.github.io/variogram_tutorial1/

### B) Hands-on (R installed)
In R:
```r
install.packages(c("gstat","sp","sf","rmarkdown"))  # first time
rmarkdown::render("variogram_tutorial1.rmd", output_format = "html_document")
```

### C) Hands-on in your browser (no install)
Click to launch an interactive RStudio session with Binder:

[![Launch RStudio in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/parker-group/variogram_tutorial1/HEAD?urlpath=rstudio)

When RStudio opens in the browser:
1. In the Files pane, click `variogram_tutorial1.rmd`.
2. Click **Knit** to render, or use **Run ▶** to step through.

---

## Notes
- Binder setup files (`runtime.txt` and `install.R`) are included for reproducibility.
- First Binder launch may take 1–3 minutes while it builds the environment.
