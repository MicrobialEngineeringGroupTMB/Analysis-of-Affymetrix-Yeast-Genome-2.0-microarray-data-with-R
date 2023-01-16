# Analysis of Affymetrix Yeast Genome 2.0 microarray data with R

## Background
The R notebook stored in this repository contains the code used to process Affymetrix Yeast Genome 2.0 microarray data for the [Almeida et al (2023)](https://doi.org/10.3390/fermentation9010072) publication titled *Physiological and molecular characterization of yeast cultures pre-adapted for fermentation of lignocellulosic hydrolysate*. The purpose of this repository is three-fold: to archive the code, to contribute to reproducible science, and for the sake of education.  The code is made available as-is and will likely not recieve updates over time. The R notebook is hosted as a GitHub page [here](https://microbialengineeringgrouptmb.github.io/Analysis-of-Affymetrix-Yeast-Genome-2.0-microarray-data-with-R/). 

In many research fields, RNA sequencing (RNAseq) has become the go-to technology for transcriptome analysis, but microarray chips are at the time of writing still commercially available and are to some extent still used in research. More importantly, the available gene expression databases, such as NCBI's Gene Expression Omnibus ([GEO](https://www.ncbi.nlm.nih.gov/geo/)) store a substantial number of microarray datasets, and to be able to re-use these valuable datasets in future studies, it is crucial to preserve the knowledge about how to process them. This notebook shows one possible way of doing this for data from Affymetrix Yeast Genome 2.0 arrays (.CEL files). Please also consider looking at other guides and tutorials (see reference section below).

The data that is analyzed in this repository has been deposited at GEO accession number [GSE218764](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE218764). However, the general workflow presented in this R notebook is designed to work with any Affymetrix Yeast Genome 2.0 data.

The code relies on several existing R packages, many of which are bioinformatics packages available via Bioconductor. The key packages used in this analysis are Affy and Limma. Rstudio was used to write the code, and Rmarkdown and Knitr to produce the .html version of the notebook. References to packages and publications are below. If there is anything in this notebook that you found useful, please consider citing the [Almeida (2022) paper](https://doi.org/10.3390/fermentation9010072), but more importantly, please make sure to cite the R packages according to the instructions of the authors of each package. The packages available from Bioconductor typically state their desired way of citation on their Bioconductor page; see for instance examples for [Affy](https://www.bioconductor.org/packages/release/bioc/html/affy.html) and [Limma](https://bioconductor.org/packages/release/bioc/html/limma.html).  

## References
The code in this R notebook is the result of reading several publications, manuals, and threads on the Bioconductor forum related to microarray data analysis in R. If you use any of these packages in your own work, please remember to cite them accordingly. <br>

**Instructions to cite the different Bioconductor packages can be found on the following pages:**

https://www.bioconductor.org/packages/release/bioc/html/affy.html

https://bioconductor.org/packages/release/bioc/html/limma.html

https://bioconductor.org/packages/release/data/annotation/html/yeast2.db.html

https://bioconductor.org/packages/release/bioc/html/biomaRt.html

https://bioconductor.org/packages/release/bioc/html/EnhancedVolcano.html

**Information about the other R packages can be found on CRAN:**

https://cran.r-project.org/web/packages/ggrepel/index.html

https://cran.r-project.org/web/packages/patchwork/index.html

https://cran.r-project.org/web/packages/tidyverse/index.html

https://cran.r-project.org/web/packages/ggplot2/index.html

https://cran.r-project.org/web/packages/ggVennDiagram/index.html

**Publications:** 

Almeida, J.R.M., Wiman, M., Heer, D., Brink, D.P., Sauer, U., Hahn-Hägerdal, B., Lidén, G. and Gorwa-Grauslund, M.F. (2023). Physiological and molecular characterization of yeast cultures pre-adapted for fermentation of lignocellulosic hydrolysate. Fermentation. 2023; 9(1):72. [https://doi.org/10.3390/fermentation9010072](https://doi.org/10.3390/fermentation9010072)

Durinck, S., Moreau, Y., Kasprzyk, A., Davis, S., De Moor, B., Brazma, A., & Huber, W. (2005). BioMart and Bioconductor: a powerful link between biological databases and microarray data analysis. *Bioinformatics*, 21(16), 3439-3440.

Edgar, R., Domrachev, M., & Lash, A. E. (2002). Gene Expression Omnibus: NCBI gene expression and hybridization array data repository. *Nucleic acids research*, 30(1), 207-210.

Gautier, L., Cope, L., Bolstad, B. M., & Irizarry, R. A. (2004). affy—analysis of Affymetrix GeneChip data at the probe level. *Bioinformatics*, 20(3), 307-315.

Irizarry, R. A., Hobbs, B., Collin, F., Beazer‐Barclay, Y. D., Antonellis, K. J., Scherf, U., & Speed, T. P. (2003). Exploration, normalization, and summaries of high density oligonucleotide array probe level data. *Biostatistics*, 4(2), 249-264.

McCarthy, D. J., & Smyth, G. K. (2009). Testing significance relative to a fold-change threshold is a TREAT. *Bioinformatics*, 25(6), 765-771.

Ritchie, M. E., Phipson, B., Wu, D. I., Hu, Y., Law, C. W., Shi, W., & Smyth, G. K. (2015). limma powers differential expression analyses for RNA-sequencing and microarray studies. *Nucleic acids research*, 43(7), e47-e47.

**The Bioconductor forums can be found here:** 

https://support.bioconductor.org/

**Examples of other useful tutorials on microarrary data processing in R:**

https://wiki.bits.vib.be/index.php/Analyze_your_own_microarray_data_in_R/Bioconductor

https://dputhier.github.io/ASG/practicals/affynorm_td/index.html

https://genomicsclass.github.io/book/pages/using_limma.html
