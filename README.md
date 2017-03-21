
<!-- README.md is generated from README.Rmd. Please edit that file -->
assigner<img src="README_assigner_logo.png" align="right"/>
===========================================================

[![Travis-CI Build Status](https://travis-ci.org/thierrygosselin/assigner.svg?branch=master)](https://travis-ci.org/thierrygosselin/assigner) [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/thierrygosselin/assigner?branch=master&svg=true)](https://ci.appveyor.com/project/thierrygosselin/assigner) [![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/assigner)](http://cran.r-project.org/package=assigner) [![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active) [![DOI](https://zenodo.org/badge/14548/thierrygosselin/assigner.svg)](https://zenodo.org/badge/latestdoi/14548/thierrygosselin/assigner)

[![packageversion](https://img.shields.io/badge/Package%20version-0.4.2-orange.svg)](commits/master) [![Last-changedate](https://img.shields.io/badge/last%20change-2017--03--20-brightgreen.svg)](/commits/master)

------------------------------------------------------------------------

This is the development page of the **assigner** package for the R software. The name **assigner** |əˈsʌɪn| is rooted in the latin word *assignare*. It's first use in french dates back to XIIIe.

Next-generation sequencing techniques that reduce the size of the genome (e.g. genotype-by-sequencing (GBS) and restriction-site-associated DNA sequencing (RADseq)) produce huge numbers of markers that hold great potential and promises for assignment analysis. After hitting the bioinformatic wall with the different workflows you'll likely end up with several folders containing whitelist and blacklist of markers and individuals, data sets with various *de novo* and/or filtering parameters and missing data. This reality of GBS/RADseq data is quite hard on GUI software traditionally used for assignment analysis. The end results is usually poor data exploration, constrained by time, and poor reproducibility.

**assigner** was tailored to make it easy to conduct assignment analysis using GBS/RADseq data within R. Additionally, combining the use of tools like [R Notebook](http://rmarkdown.rstudio.com/r_notebooks.html), [RStudio](https://www.rstudio.com) and [GitHub](https://github.com) will make effortless documenting your workflows and pipelines.

Installation
------------

To try out the dev version of **assigner** 2 simple steps:

**Step 1:** Install process dependencies:

``` r
if (!require("devtools")) install.packages("devtools") # to install
source("https://bioconductor.org/biocLite.R") # for bioconductor dependencies
biocLite() # for bioconductor dependencies
```

**Step 2:** Install **assigner** and install [gsi\_sim](https://github.com/eriqande/gsi_sim) from source

``` r
devtools::install_github("thierrygosselin/assigner", build_vignettes = TRUE)  # to install WITH vignettes
assigner::install_gsi_sim(fromSource = TRUE) # to install gsi_sim from source
```

**Optimize speed by enabling parallel computing with OpenMP inside R** [randomForestSRC](http://www.ccs.miami.edu/~hishwaran/rfsrc.html) and [data.table](https://github.com/Rdatatable/data.table) packages (e.g. to do imputations in parallel). Follow the steps in this [vignette](https://github.com/thierrygosselin/stackr/blob/master/vignettes/vignette_imputations_parallel.Rmd). You don't need to do this when updating **assigner**.

**Notes**

-   **Problems during installation:** see this [vignette](https://github.com/thierrygosselin/stackr/blob/master/vignettes/vignette_installation_problems.Rmd)
-   I recommend using [RStudio](https://www.rstudio.com/products/rstudio/download/) to run **assigner**. The R GUI is unstable with functions using parallel.
-   **Windows users**: Install [Rtools](https://cran.r-project.org/bin/windows/Rtools/).

### [For assigner's features, documentation and vignettes](https://github.com/thierrygosselin/assigner/blob/master/vignettes/assigner_features.Rmd)
