FROM bioconductor/bioconductor_docker:RELEASE_3_11 
 
#install additional packages
RUN install2.r \
   -d TRUE \
   -r "https://cran.rstudio.com" \
   RColorBrewer \
   ggplot2 \
   devtools \
   rmarkdown \
   httr \
   knitr 


#install the Bioconductor packages expected to be useful
RUN R -e 'BiocManager::install(c("GEOQuery","ComplexHeatmap","biomaRt","GEOmetadb","limma","edgeR","BiocGenerics"))'
RUN R -e 'BiocManager::install(c("kableExtra","GSEABase","GSVA","BiocStyle", "BiocParallel"))'
