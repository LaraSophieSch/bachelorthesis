# Bachelorthesis - Epigenetic and transcriptional changes in relapsed pediatric Acute Lymphoblastic Leukemia
This repository contains a comprehensive R-based workflow for the analysis of RNA-Seq and WGBS methylation data, focusing on the comparison between diagnosis and relapse in patient samples. The project integrates differential expression analysis, PCA, enrichment analysis, and analysis of treatment-associated genes.

# Contents:
The analysis is organized into the following R Markdown files:

1. RNAseq Basic Analysis.Rmd:
  Performs the basic analysis of RNA-Seq data using DESeq2, including normalization, differential expression testing, and result export.

2. PCA for Expression.Rmd:
  Conducts principal component analysis (PCA) on gene expression data to identify patterns across sample groups.

3. Volcano Plots Expression.Rmd:
  Generates volcano plots to visualize differential gene expression (log2 fold change vs. adjusted p-value) across conditions.

4. Enrichment Analysis.Rmd:
  Runs Gene Ontology (GO) and/or Reactome enrichment analysis based on DE genes, using the clusterProfiler package.

5. PCA for DMRs.Rmd:
  Performs PCA on methylation data (differentially methylated regions), visualizing grouping based on diagnosis/relapse and age.

6. Methylation.Rmd:
  Analyzes DNA methylation data, identifies differentially methylated regions (DMRs), and links them to genes.

7. HeatMaps.Rmd:
  Creates expression and methylation-based heatmaps for selected genes or DMRs to highlight clustering and expression shifts.

8. Treatments with Volcano and Fisher.Rmd:
  Investigates gene correlations with treatment response and overlaps with DE genes using Fisher’s Exact Test. Visualizes treatment-relevant gene sets via volcano plots.

# Dependencies
Key R packages used in this project:

- DESeq2

- ggplot2, EnhancedVolcano

- clusterProfiler, org.Hs.eg.db

- pheatmap, ComplexHeatmap

- GenomicRanges, rtracklayer

- tidyverse, dplyr, tibble

Make sure to install the required Bioconductor and CRAN packages before running the scripts.
<pre>
  if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install(c("DESeq2", "clusterProfiler", "org.Hs.eg.db", "GenomicRanges", "rtracklayer"))
install.packages(c("ggplot2", "EnhancedVolcano", "pheatmap", "ComplexHeatmap", "tidyverse"))
</pre>

# License
This project is part of a bachelor's thesis and is intended for academic and illustrative purposes only. The provided code is not designed for production use but rather for inspection and understanding. Commercial use is not permitted.

If any part of the content or code is used in your own work, please give appropriate credit.



