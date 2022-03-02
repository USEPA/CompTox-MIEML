# Code for Predicting MIEs from Gene Expression and Chemical Target Labels with Machine Learning (MIEML)

## Installation

### System Requirements

This package provides scripts in R.  For training models in the R package Caret, only R is required.

#### R Install

All code in this package has been tested on R 3.6.0, but any version of R 3.x should be sufficient. 
Package versions may have an impact due to changes in functionality or API.  
The following R libraries are also required to use all features of the R code:

+ [caret](https://cran.r-project.org/web/packages/caret/index.html) - Required for training binary classifiers. Code has been tested with v6.0-83
+ [data.table](https://cran.r-project.org/web/packages/data.table/index.html) - Required for internal data handling. Code has been tested with v1.12.2
+ [dplyr](https://cran.r-project.org/web/packages/dplyr/index.html) - Required for internal data handling. Code has been tested with v0.8.3.
+ [rlist](https://cran.r-project.org/web/packages/rlist/index.html) - Required for internal data handling. Code has been tested with v0.4.6.1.
+ [cmapR](https://bioconductor.org/packages/3.14/bioc/html/cmapR.html) - Required for importing LINCS L1000 gene expression data internally. Code has been tested with vcmapR_1.0.1.
+ [parallel](https://cran.r-project.org/web/packages/parallel/index.html) - Required for parallelizing model training. Code has been tested with v3.6.0.
+ [doParallel](https://cran.r-project.org/web/packages/doParallel/index.html) - Required for parallelizing model training. Code has been tested with v1.0.15.
+ [foreach](https://cran.r-project.org/web/packages/foreach/index.html) - Required for parallelizing model training. Code has been tested with v1.4.7.


#### Additional Datasets

Classifier training relies on several publicly available data sets:

+ [LINCS L1000 Phase 1 release](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE92742) - GEO entry for LINCS phase 1 
+ [LINCS L1000 Phase 2 release](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE70138) - GEO entry for LINCS phase 2 
+ [RefChemDB Supplemental Information](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6784312/bin/NIHMS1537541-supplement-Supplement1.xlsx) - RefChemDB table - supplemental table 12 should be exported and converted to .csv
+ [MSigDB gene sets](https://data.broadinstitute.org/gsea-msigdb/msigdb/release/7.1/c2.cp.v7.1.symbols.gmt) - MSigDB gene sets required if training classifiers using GSEA and pathway scoring - this file should be converted to .txt.



### Installing the MIEML package

Currently, it is recommended to clone the entire repo to a user or analysis directory by running:
```bash
git clone https://github.com/USEPA/CompTox-MIEML.git (/path/to/analysis)
```

### Installing the HTTr_pathway package

This is only recommended if users wish to train classifiers using pathway scores. Currently, it is recommended to clone the entire repo to a user or analysis directory by running:
```bash
git clone https://github.com/USEPA/CompTox-httrpathway.git (/path/to/analysis)
```


## Running an Analysis

Vignette is located at `mieml/notebooks/ML_functions_vignette.Rmd`
Modules are in: `mieml/scripts/`

## Version History

**(12/20/21)**

+ Created new (current) branch for public release of MIEML version used to generate code in initial project-associated publication.

**(2/17/22)**

+ Revised vignette and primary MIEML functions for ease of use

**(3/2/22)**

+ Revised README and vignette for public repo

## Contributors

+ **[Logan J. Everett](mailto:everett.logan@epa.gov)**
+ **[Joseph L. Bundy](mailto:bundy.joseph@epa.gov)**
