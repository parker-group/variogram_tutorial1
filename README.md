Variogram Tutorial (R)

A short, self-contained tutorial for building experimental and fitted semivariograms in R using gstat and the built-in meuse dataset (no external files).

What you'll learn

Nugget, sill, range — what they mean and how to read them

Empirical semivariogram computation

Model fitting (exponential example)

Directional variograms (anisotropy check)

Quick start

A) View-only (no R)

Open the rendered HTML tutorial:

variogram_tutorial.html in this repo, or

GitHub Pages link

B) Hands-on (R installed)

In R:

install.packages(c("gstat", "sp", "sf", "rmarkdown"))  # first time
rmarkdown::render("variogram_tutorial1.rmd", output_format = "html_document")

C) Hands-on in your browser (no install)

Click to launch an interactive RStudio session with Binder:



When RStudio opens in the browser:

In the Files pane, click variogram_tutorial1.rmd.

Click Knit to render, or use Run ▶ to step through.

Notes

Binder setup files (runtime.txt and install.R) are included for reproducibility.

First Binder launch may take 1–3 minutes while it builds the environment.

