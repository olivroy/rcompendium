
# rcompendium <img src="man/figures/hexsticker.png" height="120" align="right"/>

<!-- badges: start -->

[![R-CMD-check](https://github.com/FRBCesab/rcompendium/workflows/R-CMD-check/badge.svg)](https://github.com/FRBCesab/rcompendium/actions)
[![CRAN
status](https://www.r-pkg.org/badges/version/rcompendium)](https://CRAN.R-project.org/package=rcompendium)
[![License: GPL (&gt;=
2)](https://img.shields.io/badge/License-GPL%20%28%3E%3D%202%29-blue.svg)](https://choosealicense.com/licenses/gpl-2.0)
[![LifeCycle](man/figures/lifecycle/lifecycle-stable.svg)](https://lifecycle.r-lib.org/articles/stages.html#stable)
[![Project Status:
Active](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
[![Dependencies](https://img.shields.io/badge/dependencies-15/80-red?style=flat)](#)
<!-- badges: end -->

The purpose of the package `rcompendium` is to make easier the creation
of R package/research compendium (i.e. a predefined files/folders
structure) so that user can focus on the code/analysis instead of
wasting time organizing files. A full ready-to-work structure is set up
with some additional features (versioning, GitHub repository creation,
GitHub Actions configuration to automatically check package integrity
and deploy website using [`pkgdown`](https://pkgdown.r-lib.org/)). This
package relies heavily on the packages
[`devtools`](https://devtools.r-lib.org/) and
[`usethis`](https://usethis.r-lib.org/).

**Mea culpa:** this project was largely inspired by the package
[`rrtools`](https://github.com/benmarwick/rrtools) developed by [Ben
Marwick](https://github.com/benmarwick).

## Overview

The strength of `rcompendium` is to create the whole structure in one
command line by using the function `new_package()` (or
`new_compendium()`). The default settings will produce the following
structure:

    .
    │
    ├── pkg.Rproj                 # (optional) Created by user 
    │
    ├── .git/                     # GIT tracking folder
    ├── .gitignore                # Specific to R packages
    |
    ├── .github/                  # (optional) GitHub Actions settings
    │   └── workflows/
    │       ├── pkgdown.yaml      # Configuration file to build & deploy website
    │       └── R-CMD-check.yaml  # Configuration file to check & test package
    │
    ├── _pkgdown.yaml             # (optional) User website settings
    │
    ├── R/                        # R functions
    │   └── pkg-package.R         # Dummy R file for package-level documentation
    │
    ├── man/                      # R functions helps (automatically updated)
    │   ├── pkg-package.Rd        # Package-level documentation
    │   └── figures/              # Figures for the README 
    │       └── hexsticker.png    # Template R package HexSticker
    │
    ├── inst/
    │   └── CITATION              # BiBTeX entry to cite the R package       [*]
    │
    ├── vignettes/
    │   └── pkg.Rmd               # (optional) Package tutorial              [*]
    │
    ├── DESCRIPTION               # Project metadata                         [*]
    ├── NAMESPACE                 # Automatically generated
    ├── .Rbuildignore             # Automatically generated
    │
    ├── LICENSE                   # (optional) If License = MIT
    ├── LICENSE.md                # Content of the chosen license
    │
    ├── README.md                 # GitHub README (automatically generated)
    ├── README.Rmd                # GitHub README (to knit)                  [*]
    /
    /
    ├── analysis/                 # Proposed compendium                      [¶]
    │   ├── data/                 # User raw data (.csv, .gpkg, etc.)
    │   ├── rscripts/             # R scripts (no functions) to run analyses
    │   ├── outputs/              # Outputs created by R scripts
    │   ├── figures/              # Figures created by R scripts
    │   └── paper/                # Article based on analyses
    │
    └── make.R                    # Master R scripts to run all analyses     [¶]


    [*] These files are automatically edited but user needs to add manually 
        some information.
    [¶] These folders/files are also created when using new_compendium()

## Installation

You can install the development version from
[GitHub](https://github.com/) with:

``` r
## Install < remotes > package (if not already installed) ----

if (!requireNamespace("remotes", quietly = TRUE)) {
  install.packages("remotes")
}


## Install dev version of < rcompendium > from GitHub ----

remotes::install_github("FRBCesab/rcompendium")
```

## Getting started

Please read the
[Vignette](https://frbcesab.github.io/rcompendium/articles/rcompendium.html)
and the documentation of the function
[`new_package`](https://frbcesab.github.io/rcompendium/reference/new_package.html).

## Citation

Please cite this package as:

> Casajus N. (2021) rcompendium: An R package to create a package or
> research compendium structure. Version 0.1,
> <https://github.com/FRBCesab/rcompendium>.

You can also run:

``` r
citation("rcompendium")

## A BibTeX entry for LaTeX users is:
## 
## @Manual{,
##   title = {{rcompendium}: {An} {R} package to create a package or research compendium structure},
##   author = {{Casajus N.}},
##   year = {2021},
##   note = {R package version 0.1},
##   url = {https://github.com/FRBCesab/rcompendium},
## }
```

## Contributing

You are welcome to contribute to the `rcompendium` project. Please read
our [Contribution
Guidelines](https://frbcesab.github.io/rcompendium/CONTRIBUTING.html).

Please note that the `rcompendium` project is released with a
[Contributor Code of
Conduct](https://frbcesab.github.io/rcompendium/CODE_OF_CONDUCT.html).
By contributing to this project, you agree to abide by its terms.