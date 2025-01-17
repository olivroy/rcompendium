## Resubmit comments

* Bug fixes
  * `get_deps_*()` better detects project dependencies and does not delete 
  packages called w/ `library("pkg")` or `library('pkg')`
  * `add_sticker()` now copies the sticker template for compendium

* And other minor changes


## Test environments

* Local
  * Arch Linux 6.5.8-arch1-1 install, R 4.3.1
* GitHub Actions
  * macOS 12.7 21G816, R-release (R 4.3.1)
  * Windows Server 2022 10.0.20348, R-release (R 4.3.1)
  * Ubuntu 22.04.3 LTS, R-devel, R-release (R 4.3.1), R-oldrel
* WinBuilder
  * r-devel
  * r-release
  * r-oldrel
* Rhub
  * Windows Server 2022, R-devel, 64 bit
  * Fedora Linux, R-devel, clang, gfortran
  * Ubuntu Linux 20.04.1 LTS, R-release, GCC

## R CMD check results

0 error | 0 warning | 1 note

* Days since last update: 2
  * Sorry for the short delay between this submission and the previous one. This 
  new version provides important bug fixes.

## Downstream dependencies

There are currently no downstream dependencies for this package.
