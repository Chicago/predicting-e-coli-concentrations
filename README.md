# Predicting _E. coli_ concentrations using limited qPCR deployments at Chicago

This repository is part of the working draft for an upcoming paper tentatively titled _Predicting _E. coli_ concentrations using limited qPCR deployments at Chicago_. It is an academic paper describing the methods and results of the City of Chicago [Clear Water](https://github.com/Chicago/clear-water) project.

## Document

This document uses [RMarkdown](http://rmarkdown.rstudio.com/) to format the paper and uses [knitr](https://yihui.name/knitr/) to compile it. The simpliest way to compile the document is downloading the repo and opening the `predicting-e-coli-concentrations.Rproj` file in RStudio. Use the built-in knit button to compile the documentation.

### Bibliography

This project uses [knitcitations](https://github.com/cboettig/knitcitations) to compile the project bibliography. Articles should be stored in a [Zotero library](https://www.zotero.org/groups/187068/city_of_chicago_data_science_team/items/collectionKey/RJJ5U3BC).

References from the Zotero library should be exported as BibTeX to `bibliography/zotero-references.bib`. The document should reference the BibTeX document, e.g., `r citep(biblio["whitman_summer_2008"])`.

Examples:

  * Parenthetical citation (e.g, (Whiteman, 2008)) by entry in `zotero-references.bib`.: `r citep(biblio["whitman_summer_2008"])`
  * Inline citation (e.g., Whiteman (2008)): `r citet(biblio["whitman_summer_2008"])`
  * Cite by entry position: `r citep(biblio[[2]])`
  * Cite multiple authors: `r citep(biblio[c("whitman_summer_2008","boehm_decadal_2002"])`
