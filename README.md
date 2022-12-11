# pkg_template

A repository to be used as template for creating new packages

## Links for building the package and the documentation (to be removed at some point)

https://pkgdown.r-lib.org/articles/pkgdown.html

https://bookdown.org/yihui/rmarkdown/rticles-bookdown.html

https://sahirbhatnagar.com/blog/2020/03/03/creating-a-website-for-your-r-package/

## Code to build the package template

This code helps to build the package backbone (including all documentation and github links) for this package and website.

```r
usethis::create_package("pkg_template")
usethis::use_readme_md()
usethis::use_gpl3_license()
usethis::use_news_md(open = FALSE)
usethis::use_vignette("package_intro")
usethis::use_git()
gitcreds::gitcreds_set()
usethis::use_github()
usethis::use_github_action_check_release()
usethis::use_lifecycle_badge("experimental")
usethis::use_pkgdown_github_pages()
pkgdown::build_site()
```

This other code is to build and install with vignettes for the documentation of the package and not only to the pkgdown website.

```r
devtools::build(vignettes = TRUE)
devtools::install(build_vignettes = TRUE)
```


