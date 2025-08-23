# Variogram Tutorial (R)

A short, self-contained tutorial for building experimental and fitted semivariograms in R using **gstat** and the built-in `meuse` dataset (no external files).

## What you'll learn
- Nugget, sill, range — what they mean and how to read them
- Empirical semivariogram computation
- Model fitting (exponential example)
- Directional variograms (anisotropy check)

## Quick start

### A) View-only (R script shown, but already run for you)
Open the rendered HTML tutorial:
- `variogram_tutorial.html` (in this repo)
- https://parker-group.github.io/variogram_tutorial1/

### B) Hands-on (R installed on your computer - you run the script)
In R:
```r
install.packages(c("gstat", "sp", "sf", "rmarkdown"))  # first time
rmarkdown::render("variogram_tutorial1.rmd", output_format = "html_document")
```

### C) Hands-on in your browser (no install - you run R from your browser)
Click to launch an interactive RStudio session with Binder:

[![Launch RStudio in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/parker-group/variogram_tutorial1/HEAD?urlpath=rstudio)

When RStudio opens in the browser:
1. In the **Files** pane, click `variogram_tutorial1.rmd`
2. Click **Knit** to render, or use **Run ▶** to step through

---

## Reproducing directly from the README in R
If you want to quickly reproduce the example without opening the `.Rmd` file, copy/paste this into your R console:
```r
# Install required packages (skip if already installed)
install.packages(c("gstat", "sp"))

# Load libraries
library(sp)
library(gstat)

# Load the example data
data(meuse)
coordinates(meuse) <- ~x+y

# Compute experimental variogram
v_exp <- variogram(log(zinc)~1, meuse)
plot(v_exp)

# Fit an exponential model
v_model <- fit.variogram(v_exp, model=vgm(psill=0.6, model="Exp", range=900, nugget=0.05))
plot(v_exp, v_model)
```
This minimal example runs the core variogram workflow without needing any extra files.

---

## Notes
- Binder setup files (`runtime.txt` and `install.R`) are included for reproducibility.
- First Binder launch may take 1–3 minutes while it builds the environment.
