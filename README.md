---
output: github_document
---

<!-- README.md is generated from README.Rmd. Please edit that file -->



# nlmixr: an R package for population PKPD modeling

<!-- badges: start -->
[![R build status](https://github.com/nlmixrdevelopment/nlmixr/workflows/R-CMD-check/badge.svg)](https://github.com/nlmixrdevelopment/nlmixr/actions)
[![Codecov test coverage](https://codecov.io/gh/nlmixrdevelopment/nlmixr/branch/master/graph/badge.svg)](https://codecov.io/gh/nlmixrdevelopment/nlmixr?branch=master)
<!-- badges: end -->

***

![nlmixr](logo.png)


`nlmixr` is an R package for fitting general dynamic models,
pharmacokinetic (PK) models and pharmacokinetic-pharmacodynamic (PKPD)
models in particular, with either individual data or population
data. The nlme and SAEM estimation routines can be accessed using a
universal user interface (UUI), that provides universal model and
parameter definition syntax and results in a fit object that can be
used as input into the `Xpose` package. Running nlmixr using the UUI
is described in the vignette:
https://github.com/nlmixrdevelopment/nlmixr/blob/master/vignettes/running_nlmixr.Rmd

Under the hood `nlmixr` has five main modules:  

1. `dynmodel()` and its mcmc cousin `dynmodel.mcmc()` for nonlinear
   dynamic models of individual data;
2. `nlme_lin_cmpt()`for one to three linear compartment models of
   population data with first order absorption, or i.v. bolus, or
   i.v. infusion using the nlme algorithm;
3. `nlme_ode()` for general dynamic models defined by ordinary
   differential equations (ODEs) of population data using the nlme
   algorithm;
4. `saem_fit` for general dynamic models defined by ordinary differential equations (ODEs) of population data by the Stochastic Approximation Expectation-Maximization (SAEM) algorithm;  
5. `gnlmm` for generalized non-linear mixed-models (possibly defined
   by ordinary differential equations) of population data by the
   adaptive Gaussian quadrature algorithm.

A few utilities to facilitate population model building are also included in `nlmixr`.

For a brief vignette describing the modules, please see:
https://github.com/nlmixrdevelopment/nlmixr/blob/master/inst/nlmixr-intro.pdf

The examples in the vignette can be run using VignetteDemo.R and the associated data files available at:
https://github.com/nlmixrdevelopment/nlmixr/tree/master/vignettes

For PKPD modeling (with ODE and dosing history) with
[Stan](http://mc-stan.org/), check out Yuan's package PMXStan:

## Installation

You can install the released version of nlmixr from [CRAN](https://CRAN.R-project.org) with:

``` r
install.packages("nlmixr")
```

And the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("nlmixrdevelopment/nlmixr")
```
## Example

