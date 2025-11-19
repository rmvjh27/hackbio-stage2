# Single-Cell RNA Sequencing Data Analysis using Scanpy
Identification of different cell types in a sample can be done via single-cell RNA sequencing. The analysis steps of single-cell data are as follows:
1. Importing the necessary libraries and data into the environment
2. Quality control
   - Removal of doublets
   - Removal of cells with high counts of mitochondrial or ribosomal genes
3. Normalization
4. Dimensionality Reduction and Clustering
5. Cell annotation
   In this example, marker gene sets from PanglaoDB are used to annotate types of cells found in the sample based on their highest-ranked marker genes.

