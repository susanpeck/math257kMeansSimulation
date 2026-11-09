# Comparing Multivariate and Univariate k-Means Clustering

A simulation study for SJSU Math 257 Multivariate Data Analysis, Project 1.

**Author:** Susan Peck
**Date of submission:** November 8, 2026

## Overview

This project compares multivariate analysis to univariate analysis using simulated data and k-means clustering. Data are simulated so that the true group membership is known. When can clustering using a single variable recover all three true clusters? When does a multivariate approach work better than a univariate? Three scenarios, each with 3 true clusters of 200 observations and 3 variables, differ in how the variables carry information about the clusters:

1. Every variable separates all three clusters.
2. Each variable isolates one cluster.
3. Only Variable 1 carries signal, and Variables 2 and 3 are noise.

Each scenario is run at five within-cluster standard deviations (2, 3, 4, 5 and 6) with 500 simulated datasets per combination. Each clustering is scored against the true groups with the adjusted Rand index.

## Files in this repository

| File | Description |
|---|---|
| `Math257_Project1_kmeans_simulation_v1.2.Rmd` | R Markdown source for the report. Contains all code, which is hidden in the knit output |
| `Math257_Project1_kmeans_simulation_v1.2.pdf` | The knit PDF report |
| `references.bib` | BibTeX file with the references for the report |
| `README.md` | This file |

There is no data folder because all data are simulated inside the R Markdown file.

## How to reproduce the report

1. Install R and RStudio, plus a LaTeX installation so that R Markdown can produce a PDF (for example, the R package `tinytex`).
2. Install the R packages used: `rmarkdown`, `knitr`, `mclust`, and `bookdown`.
3. Open `Math257_Project1_kmeans_simulation_v1.2.Rmd` and knit it to PDF.

Random seeds are set inside the file (1 for the example figure, and 101, 102 and 103 for the three simulations), so a knit reproduces the same numbers. The simulations run 15 combinations of scenario and standard deviation, each with 500 datasets and 4 k-means fits per dataset, so knitting takes a while.

## Data

All data are simulated by the code in the R Markdown file using R's random number generator. There is no external data source, and no dataset license applies.

## External resources and use of LLMs

Claude was used to check for typos and grammar, consistency, to write formulas in LaTeX, to rewrite code chunks with new values, remember how to reference figures in R Markdown, write code to make a nicely formatted table, create a references.bib file, and propose multiple project titles for me to reject and create my own.

## References

Full references are in `references.bib` and in the References section of the report.
