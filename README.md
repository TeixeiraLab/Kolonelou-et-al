# Kolonelou-et-al
R-markdown file for Seurat pipeline analysis of sc-RNA-seq of zebrafish embryos (2dpf) injected with coated and uncoated DNA origami structures.

The R-markdown file takes files from the 10X Cell Ranger output (raw_feature_bc_matrix.h5) and loads these as Seurat objects. The pipeline is executed with Seurat functions and according to the Seurat pipeline.
Subsequent quality control, cell cycle analysis, and filtering is done to remove low quality cells and selected genes. 
Normalization, detection of variable features, scaling and dimentionality reduction is performed both prior and subsequent to integration of the two samples. 
Clustering (selectiong clusters at resolution 1.2) is performed and selected marker genes are plotted as a Feature map to aid in determination of cell type. Additional cell type predictions are done using a zebrafish atlas from Zebrahub (https://zebrahub.ds.czbiohub.org/data, 2dpf) and scPred. Precursor CNCCs are also identified by overlap of previously characterized marker genes (https://www.nature.com/articles/s41467-021-27594-w). 

Paramteres in the markdown file include: 
- path to h5 file for sample from coated structures
- path to h5 file for sample from uncoated structures
- path to zebrafish atlas used for scPred (before or after training of algorithm on atlas)
