# Predicting _E. coli_ concentrations using limited qPCR deployments at Chicago

This repository is part of the working draft for an upcoming paper tentatively titled _Predicting _E. coli_ concentrations using limited qPCR deployments at Chicago_. It is an academic paper describing the methods and results of the City of Chicago [Clear Water](https://github.com/Chicago/clear-water) project.

## Document

This document uses [RMarkdown](http://rmarkdown.rstudio.com/) to format the paper, uses [knitr](https://yihui.name/knitr/) to compile it, and the `rticles` package to format the document. The simpliest way to compile the document is downloading the repo and opening the `predicting-e-coli-concentrations.Rproj` file in RStudio. Use the built-in knit button to compile the documentation. Before knitting the document, install the `rticles` package.

### Bibliography

This project uses [knitcitations](https://github.com/cboettig/knitcitations) to compile the project bibliography. Articles should be stored in a [Zotero library](https://www.zotero.org/groups/187068/city_of_chicago_data_science_team/items/collectionKey/RJJ5U3BC).

References from the Zotero library should be exported as BibTeX to `bibliography/zotero-references.bib`. The document should reference the BibTeX document, e.g., `r citep(biblio["whitman_summer_2008"])`.

Examples:

  * Parenthetical citation (e.g, (Whiteman, 2008)) by entry in `zotero-references.bib`.: `r citep(biblio["whitman_summer_2008"])`
  * Inline citation (e.g., Whiteman (2008)): `r citet(biblio["whitman_summer_2008"])`
  * Cite by entry position: `r citep(biblio[[2]])`
  * Cite multiple authors: `r citep(biblio[c("whitman_summer_2008","boehm_decadal_2002"])`
  
## Dependencies

This project has been tested using both [R](https://cran.r-project.org/) 3.4 and 3.5. Source code and version number for all R package dependencies is located in the `packrat` directory and managed using [Packrat](http://rstudio.github.io/packrat/). 

### Packrat

Some users have reported difficulty compiling R packages `data.table` and `rgdal` from source code on some systems, especially Mac OS X. `Packrat` will fail to complete loading all packages if any single package fails to compile. If you are having difficulty with a specific package, try removing the entry for the package in the file `packrat/packrat.lock`. Then once `Packrat` completes installing all the other packages, install the missing package as you normnally would outside `Packrat`.
