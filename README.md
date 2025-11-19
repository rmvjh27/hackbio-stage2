# Single-Cell RNA Sequencing Data Analysis using Scanpy
Identification of different cell types in a sample can be done via single-cell RNA sequencing. The analysis steps of single-cell data are as follows:
1. Importing the necessary libraries and data into the environment
   - Required libraries: scanpy, anndata, igraph, decoupler
   - scanpy: a powerful tool for single-cell RNA sequencing data analysis
   - anndata: provides the AnnData object—a common data structure used to store and manipulate single-cell data, often used in conjunction with scanpy
   - igraph: a package for creating and manipulating graphs, which is often used in single-cell analysis for tasks like clustering (e.g., Leiden algorithm)
   - decoupler: used for gene set enrichment analysis and inferring biological activities from omics data
   - Exploration of single-cell data to observe cell and gene metadata and identify the parameters that will be used
2. Quality control
   - Removal of cells with high counts of mitochondrial or ribosomal genes: Cells with a high proportion of mitochondrial reads (e.g., >10–20%) are likely stressed, apoptotic, or poorly captured. Ribosomal transcripts represent global transcriptional activity, not cell-type-specific biology.
   - Removal of doublets
3. Normalization
   - Normalization adjusts for sequencing depth differences between cells
   - Normalized (left) vs non-normalized (right) mean expressions of genes:
     ![normalization](https://github.com/rmvjh27/hackbio-stage2/blob/c5f1686104390feb65691aee6252b74a5c9468cb/download(1).png)
4. Dimensionality Reduction and Clustering
   - Principal component analysis (PCA) to reduce data complexity and highlight key variation patterns
   - Computation of the neighborhood graph of cells
   - UMAP (Uniform Manifold Approximation and Projection) to visualize high-dimensional data in 2 or 3 dimensions and identify distinct cell populations
   - Application of the Leiden clustering algorithm on the UMAP analysis result to identify cell clusters
5. Cell annotation
   In this example, marker gene sets from PanglaoDB are used to annotate types of cells found in the sample based on their highest-ranked marker genes.

