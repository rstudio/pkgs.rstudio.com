# pkgs.rstudio.com - RStudio's Open Source R Packages

This is the source repository for the website https://pkgs.rstudio.com. This website is a central place to find Open Source R packages from RStudio. 

Idea is that `https://pkgs.rstudio.com/<pkgname>` will lead you to the pkgdown website of the `<pkgname>` package. 

## How it works ? 

This website is hosted on Netlify and acts as a central redirect for other pkgdown websites hosted on netlify or other place (like `rstudio.github.io`).

* Main file is `_redirects` which contains the list of packages' website to redirect to
* The `index.Rmd` uses this information to build an index page present all explicit package in a table.

Currently, the url `https://pkgs.rstudio.com/` works for: 

* A few sets of website hosted on Netlify (mainly the one from the R Markdown Team)
* Any packages hosted on github pages in RStudio organisation, meaning where website is hosted to `https://rstudio.github.io/<pkgname>`. 

## How to add a package website in the main table on index page ? 

Open a PR to add a rule in `_redirect`. If the package is not hosted on `https://rstudio.github.io`, then the `index.html` will be correctly rebuild when merging the PR.

## Who to contact ? 

Christophe (@cderv) <cderv@rstudio.com>
