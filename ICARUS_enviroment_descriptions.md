<h2 align="center"> <b>Saved R objects in ICARUS enviroment </b></h2>

## Seurat R object
* "Final_Seurat_Object" - Seurat scRNA-seq dataset (post quality control filters, dimensionality reduction, clustering, data correction and cell type assignment, where applicable)
* "plot.data" - UMAP/tSNE plot of final seurat object

## Species 
* "msigdb" - Species input for Msigdb
* "orgDb" - Species input for orgDb
* "KEGG_species" - Species input for KEGG
* "REACTOME_species" - Species input for REACTOME
* "REACTOME_species2" - Species input for REACTOME

## Quality control objects (Dataset 1)
* "PostQC_dataset1" - Seurat scRNA-seq dataset post quality control filtering
* "type" - Does your scRNA-seq dataset contain a single or multiple samples
* "original_dataset1" - Seurat scRNA-seq dataset pre-quality control filtering
* "QC_nFeature_threshold1_dataset1" - Minimum number of nFeatures (number of unique genes lower threshold)
* "QC_nFeature_threshold2_dataset1" - Maximum number of nFeatures (number of unique genes higher threshold)
* "QC_nCount_threshold1_dataset1" - Minimum number of nCount (number of total molecules lower threshold)
* "QC_nCount_threshold2_dataset1" - Maximum number of nCount (number of total molecules higher threshold)
* "QC_percent.mt_threshold1_dataset1" - Minimum percentage of mitochondrial genes (lower threshold)
* "QC_percent.mt_threshold2_dataset1" - Maximum percentage of mitochondrial genes (higher threshold)
* "QC_percent.ribo_threshold1_dataset1" - Minimum percentage of ribosomal genes (lower threshold)
* "QC_percent.ribo_threshold2_dataset1" - Maximum percentage of ribosomal genes (higher threshold)

## Doublet Removal (Dataset 1)
* "Remove" - Detected doublets
* "Removed" - Was doublet removal performed?
* "doublesim" - Estimated percentage of doublets (user inputed)
* "plot.data.doublets" - UMAP/tSNE plot of doublets

## Quality control objects (Dataset 2)
* "PostQC_dataset2" - Seurat scRNA-seq dataset post quality control filtering
* "type2" - Does your scRNA-seq dataset contain a single or multiple samples
* "original_dataset2" - Seurat scRNA-seq dataset pre-quality control filtering
* "QC_nFeature_threshold1_dataset2" - Minimum number of nFeatures (number of unique genes lower threshold)
* "QC_nFeature_threshold2_dataset2" - Maximum number of nFeatures (number of unique genes higher threshold)
* "QC_nCount_threshold1_dataset2" - Minimum number of nCount (number of total molecules lower threshold)
* "QC_nCount_threshold2_dataset2" - Maximum number of nCount (number of total molecules higher threshold)
* "QC_percent.mt_threshold1_dataset2" - Minimum percentage of mitochondrial genes (lower threshold)
* "QC_percent.mt_threshold2_dataset2" - Maximum percentage of mitochondrial genes (higher threshold)
* "QC_percent.ribo_threshold1_dataset2" - Minimum percentage of ribosomal genes (lower threshold)
* "QC_percent.ribo_threshold2_dataset2" - Maximum percentage of ribosomal genes (higher threshold)

## Doublet Removal
* "Remove2" - Detected doublets
* "Removed2" - Was doublet removal performed?
* "doublesim2" - Estimated percentage of doublets (user inputed)
* "plot.data.doublets2" - UMAP/tSNE plot of doublets

## Dimensionality Reduction (Single sample)
* "variablefeatures" - Number of variable features used in analysis
* "SCTransformDR" - Was log normalisation or SCTransform used?

## Dimensionality Reduction (Multiple samples)
* "Combined.list" - Integrated Seurat scRNA-seq dataset 
* "VFintegrated" - Number of variable features used in analysis
* "integrationreduction" - Method of integration (CCA, RPCA, harmony)
* "kanchor" - Number of kanchors setting used for CCA and RPCA integration methods
* "SCTransformDR2" - Was log normalisation or SCTransform used?

## Clustering
* "NumberofPCs_GraphConstruction" - Number of PCs used for graph construction
* "k.param" - Number of k-nearest neighbours used for graph construction
* "n.trees" - Number of trees used for graph construction
* "ClusteringAlgorithm" - Which clustering algorithm was used? (Louvain, Leiden or SLM)
* "Resolution" - Resolution of clusters (high number indicates more clusters)
* "NumberofPCs_UMAP" - Number of PCs used for UMAP plot
* "knn_UMAP" - Number of k-nearest neighbours used for UMAP plot
* "min.dist_UMAP" - Minimum distance parameter for UMAP plot
* "NumberofPCs_tsne" - Number of PCs used for tSNE plot
* "Perplexity_tsne" - Perplexity parameter for tSNE plot
* "max.iterations_tsne" - Maximum number of iterations for tSNE plot
* "CellComposition" - Table of clustering outcome including the assigned Seurat cluster, cell type (if applicable) and sample origin
* "plot.data.original" - UMAP/tSNE plot of clustering outcome

## Data Correction
* "Regress_Confounder" - Which of the following were regressed from the scRNA-seq dataset (cell cycle phase, number of unique genes, number of molecules, ribosomal percentage, mitochondrial percentage)
* "Regress_genes" - Genes regressed from the dataset
* "Regress_pathway" - Gene pathway regressed from the dataset
* "GeneR" - Genes in gene pathway regressed from the dataset

## Cell labelling
* "new.cell.ids" - Cell type labels
* "reference_annotation" - Which cell type annoation method was used (sctype, singleR, custom)?
* "select2" - SingleR database
* "selecttissue" - Tissue type for sctype method

## Gene expression visualisation
* "GeneExpression_GeneInput" - Gene of interest for visualisation
* "GeneExpression_PathwayInput" - Gene pathway of interest for visualisation
* "GenePathwayNames" - Msigdb gene pathway information table

## MEGENA co-expression analysis
**Co-expression module construction settings:**
* "MEGENA_selectcluster" - Should analysis be performed on Seurat clusters or labelled cell types
* "MEGENA_samples" - Dataset input for MEGENA analysis 
* "variablegenesMEGENA" - Number of variable genes for MEGENA analysis
* "VF" - Variable genes for MEGENA analysis
* "g" - MEGENA co-expression module construction intermediate file
* "MEGENApval" - p-value threshold for MEGENA co-expression module construction
* "MEGENAmin.size" - Minimum gene module size
* "summary.output" - Computed MEGENA modules
* "n_MEGENA" - Downsample MEGENA module construction to X cells per cluster/cell type (randomly selected) 

**Cell cluster marker gene detection settings (for sunburst plot):**
* "log2FCMEGENA" - Log2 fold change threshold for marker gene detection
* "minMEGENA" - Only include genes which are expressed above the minimum percentage of cells within the clusters
* "pvalMEGENA" - p value threshold for marker gene detection
* "markersMEGENA" - Table of cluster markers

**Gene Ontology module analysis**
* "moduleGO_df" - Gene Ontology analysis for MEGENA modules

## SCENIC transcriptional regulatory network analysis
**SCENIC settings**
* "variablefeaturesSCENIC" <- Variable features for SCENIC analysis
* "SCENIC_selectcluster" - Should analysis be performed on Seurat clusters or labelled cell types
* "Top5_SCENIC" - Regulon construction limited to top X number of genes
* "n_SCENIC" - Regulon construction limited to X number of cells
* "SCENICdb" - SCENIC database used (human, mouse or fly)
* "SCENIC_samples" - Dataset input for SCENIC analysis
* "cellInfo" - Table of cell information including the assigned Seurat cluster, cell type (if applicable), number of unique genes, number of molecules, mitochondrial percentage, ribosomal percentage and sample origin
* "n_SCENIC" - Downsample SCENIC analysis to X cells per cluster/cell type (randomly selected)

**SCENIC output**
* "regulonAUC" - AUCell regulon activity
* "regulons" - Regulon information
* "regulonnames" - Regulon names
* "SCENICInput" - Regulon names

## MAGMA.celltyping GWAS associations
* "MAGMA_Final_Results" - MAGMA results table

**Using own GWAS dataset settings**
* "MAGMA_samples2" - Dataset input for MAGMA analysis
* "textlabelMAGMA" - GWAS summary statistc trait
* "MAGMA_N" - Number of GWAS Individuals
* "GRCh" - Is genome build of GWAS dataset GRCh37 or GRCh38?
* "MAGMA_Pop" - GWAS population (European, African, Ad Mixed African, East Asian, South Asian)
* "MAGMA_selectcluster2" - Should analysis be performed on Seurat clusters or labelled cell types
* "n_MAGMA" - Downsample MAGMA analysis to X cells per cluster/cell type (randomly selected)

**Public GWAS dataset(s) settings**
* "MAGMA_samples" - Dataset input for MAGMA analysis 
* "MAGMA_GWAS" - Public GWAS dataset selected
* "meta" - Public GWAS datasets information
* "MAGMA_selectcluster" - Should analysis be performed on Seurat clusters or labelled cell types
* "n_MAGMA2" - Downsample MAGMA analysis to X cells per cluster/cell type (randomly selected)

## Trajectory analysis
* "TAselectedcells" - Root cells selected for trajectory analysis (lasso select)
* "TA_pickercluster" - Root cluster selected for trajectory analysis (cluster select)

## CellChat cell-cell communication analysis

**CellChat Settings**
* "Chatdb" - Use human or mouse database?
* "Chat_selectcluster" - Should analysis be performed on Seurat clusters or labelled cell types
* "Chat_number" - Filter out the cell-cell communication in groups with less than X cells
* "Chatpval" - p-value threshold for CellChat analysis
* "ChatChoose" - Select between single dataset analysis or comparison between two datasets

**Single dataset analysis**
* "cellchat" - CellChat object
* "ChatSample" - Dataset input for CellChat analysis

**Comparison between two datasets analysis**
* "cellchatM" - CellChat object
* "ChatMultiple1Sample" - Dataset input for CellChat analysis (Dataset 1)
* "ChatMultiple2Sample" - Dataset input for CellChat analysis (Dataset 2)

## Multimodal analysis
* "MM" - Multimodal data 

## Differential Expression Analysis

**General settings**
* "DifferentialExpression_comparison" - Select from DE analysis between samples or DE analysis between clusters 
* "pvalDE" - Only include genes above the p-value threshold
* "DifferentialExpression_log_threshold" - Log2 fold change threshold for DE analysis
* "DifferentialExpression_min.pct_threshold" - Only include genes which are expressed above the minimum percentage of cells within the clusters
* "DifferentialExpression_Table" - Differentially expressed genes table

**Differential Expression analysis between sample settings**
* "DifferentialExpression_clusters_BetweenSampleComparison" - Should analysis be performed on Seurat clusters or labelled cell types
* "DifferentialExpression_ClusterOfInterest_BetweenSampleComparison" - Cluster(s) being compared for DE analysis
* "DifferentialExpression_SampleOfInterest1_BetweenSampleComparison" - Dataset 1 input for DE analysis
* "DifferentialExpression_SampleOfInterest2_BetweenSampleComparison" - Dataset 2 input for DE analysis

**Differential Expression analysis between clusters settings**
* "DifferentialExpression_clusters_BetweenClustersComparison" - Should analysis be performed on Seurat clusters or labelled cell types
* "DifferentialExpression_SampleOfInterest1_BetweenClustersComparison" - Selected cluster 1 for DE analysis
* "DifferentialExpression_SampleOfInterest2_BetweenClustersComparison" - Selected cluster 2 for DE analysis

**Gene set enrichment**
* "DifferentialExpression_GeneSetEnrichmentInput" - Selected pathway enrichment method (Gene Ontology, Reactome, KEGG, Wikipathways)
* "GOlabelsDE" - Selected subontology for gene ontology pathway anaylsis
* "DifferentialExpression_GeneSetEnrichment_pvalue_threshold" - Gene set enrichment p-value threshold
* "DifferentialExpression_GeneSetEnrichment_padjust_method" - Gene set enrichment p-value adjustment method (holm, hochberg, hommel, bonferroni, BH, BY, fdr)
* "DifferentialExpression_GeneSetEnrichment_PATHWAY" - Table of enriched pathways

**Volcano plot settings**
* "DifferentialExpression_volcano_Foldchange_threshold1" - Volcano plot log2 fold change minimum threshold
* "DifferentialExpression_volcano_Foldchange_threshold2" - Volcano plot log2 fold change maximum threshold
* "DifferentialExpression_volcano_pvalue" - Volcano plot p-value threshold
* "DifferentialExpression_volcano_markers" - Volcano plot

## Pathway Analysis
* "SelectPathwayAnalysis" - Selected pathway enrichment method (Gene Ontology, Reactome, KEGG, Wikipathways)
* "PathwayAnalysis_pvalue_adjustment_method" - Gene set enrichment p-value adjustment method (holm, hochberg, hommel, bonferroni, BH, BY, fdr)
* "PathwayAnalysis_pvalue" - Gene set enrichment p-value threshold
* "GOlabelsPA" - Selected subontology for gene ontology pathway anaylsis
* "PathwayAnalysis_GeneSetEnrichment" - Enriched pathways
* "PathwayAnalysis_GeneSetEnrichment2" - Enriched pathways
* "geneListPathway" - Enriched gene sets

## Gene-Drug Analysis
* "markersDRUG" - Differentially expressed genes input into gene-drug analysis
* "DRUGdf" - Result of DGIdb database look up of differentially expressed genes

## Custom Differential Expression Analysis

**General settings**
* "selectedcells_lasso1" - Lasso selected cells for comparison group 1
* "selectedcells_lasso2" - Lasso selected cells for comparison group 2
* "CustomDifferentialExpression_log_threshold" - Log2 fold change threshold for DE analysis
* "CustomDifferentialExpression_min.pct_threshold" - Only include genes which are expressed above the minimum percentage of cells within the clusters
* "pvalSDE" - Only include genes above the p-value threshold
* "CustomDifferentialExpression_Table" - Differentially expressed genes table

**Gene set enrichment**
* "CustomDifferentialExpression_GeneSetEnrichmentInput" - Selected pathway enrichment method (Gene Ontology, Reactome, KEGG, Wikipathways)
* "GOlabelsSDE" - Selected subontology for gene ontology pathway anaylsis
* "CustomDifferentialExpression_GeneSetEnrichment_pvalue_threshold" - Gene set enrichment p-value threshold
* "CustomDifferentialExpression_GeneSetEnrichment_padjust_method" - Gene set enrichment p-value adjustment method (holm, hochberg, hommel, bonferroni, BH, BY, fdr)
* "CustomDifferentialExpression_GeneSetEnrichment_PATHWAY" - Table of enriched pathways

**Volcano plot settings**
* "CustomDifferentialExpression_volcano_Foldchange_threshold1" - Volcano plot log2 fold change minimum threshold
* "CustomDifferentialExpression_volcano_Foldchange_threshold2" -Volcano plot log2 fold change maximum threshold
* "CustomDifferentialExpression_volcano_pvalue" - Volcano plot p-value threshold
* "CustomDifferentialExpression_volcano_markers" - Volcano plot

## Custom Pathway Analysis
* "SelectCustomPathwayAnalysis" - Selected pathway enrichment method (Gene Ontology, Reactome, KEGG, Wikipathways)
* "CustomPathwayAnalysis_pvalue_adjustment_method" - Gene set enrichment p-value adjustment method (holm, hochberg, hommel, bonferroni, BH, BY, fdr)
* "CustomPathwayAnalysis_pvalue" - Gene set enrichment p-value threshold
* "GOlabelsSPA" - Selected subontology for gene ontology pathway anaylsis
* "CustomPathwayAnalysis_GeneSetEnrichment" - Enriched pathways
* "CustomPathwayAnalysis_GeneSetEnrichment2" - Enriched pathways
* "geneList_CustomPathway" - Enriched gene sets

## Custom Gene-Drug Analysis
* "markersDRUG2" - Differentially expressed genes input into gene-drug analysis
* "DRUGdf2" - Result of DGIdb database look up of differentially expressed genes
