# 📓 Variable Tracking – AI Lab Notebook

This file keeps track of all important variables and datasets used throughout the notebook.

&nbsp;


## SmartSeq - MCF7
| Variable Name       | Step                 | Description                                  | Shape         |
|---------------------|----------------------|----------------------------------------------|---------------|
| `mcf_meta`          | - Given              | Information on the cells                     | (383, 8)      |
| `dfs_mcf_unfiltered`| - Given              | Unfiltered gene expression matrix            | (22934, 383)  |
| `dfs_mcf_filtered`  | - Given              | Filtered gene expression matrix              | (18945, 313)  |
| `dfs_mcf_train`     | - Given              | Dataset to use for training                  | (3000, 250)   |
| `dfs_mcf_test`      | - Given              | Dataset to use for testing                   | (3000, 63)    |
| `cell_stats_mcf`    | Cell Stat (2.2.1)    | Dataset with stats about cells of unfiltered | (383, 7)      |
| `gene_stats_mcf`    | Gene stat (2.2.2)    | Dataset with stats about genes of unfiltered | (22934, 3)    |
| `dfs_mcf_f1`        | Filtering (2.5)      | Noise / uninformative entries removed        | (18946, 312)  |
| `dfs_mcf_norm`      | Normalization (2.7)  | Normalized total counts per cell             | (18946, 312)  |
| `dist_summary_mcf`  | Dist diagnostic (2.8)| Skewness and Kurtosis per gene               | (18946, 4)    |
| `dfs_mcf_log`       | Log-Transformation   | Log1p applied to reduce skw and kurt         | (18946, 312)  |
| `dfs_mcf_hvg`       | Top 3000 (2.9)       | Highly Variable Genes based on dispersion    | (3000, 312)   |
| `dfs_mcf_hvg2`      | Top 3000 (2.9)       | HVG without correlation                      | (3000, 312)   |
| `dfs_mcf_zscore`    | Z-Score (2.10)       | Standardization to each gene                 | (3000, 312)   |


&nbsp;


## SmartSeq - HCC1806
| Variable Name       | Step                 | Description                                  | Shape         |
|---------------------|----------------------|----------------------------------------------|---------------|
| `hcc_meta`          | Metadata             | Information on the cells                     | (243, 8)      |
| `dfs_hcc_unfiltered`| - Given              | Unfiltered gene expression matrix            | (23396, 243)  |
| `dfs_hcc_filtered`  | - Given              | Filtered gene expression matrix              | (19503, 227)  |
| `dfs_hcc_train`     | - Given              | Dataset to use for training                  | (3000, 182)   |
| `dfs_hcc_test`      | - Given              | Dataset to use for testing                   | (3000, 45)    |
| `cell_stats_mcf`    | Cell Stat (2.2.1)    | Dataset with stats about cells of unfiltered | (383, 7)      |
| `gene_stats_mcf`    | Gene stat (2.2.2)    | Dataset with stats about genes of unfiltered | (22934, 3)    |
| `dfs_mcf_f1`        | Filtering (2.5)      | Noise / uninformative entries removed        | (18946, 312)  |
| `dfs_mcf_norm`      | Normalization (2.7)  | Normalized total counts per cell             | (18946, 312)  |
| `dist_summary_mcf`  | Dist diagnostic (2.8)| Skewness and Kurtosis per gene               | (18946, 4)    |
| `dfs_mcf_log`       | Log-Transformation   | Log1p applied to reduce skw and kurt         | (18946, 312)  |
| `dfs_mcf_hvg`       | Top 3000 (2.9)       | Highly Variable Genes based on dispersion    | (3000, 312)   |
| `dfs_mcf_hvg2`      | Top 3000 (2.9)       | HVG without correlation                      | (3000, 312)   |
| `dfs_mcf_zscore`    | Z-Score (2.10)       | Standardization to each gene                 | (3000, 312)   |


&nbsp;


## DropSeq - MCF7
| Variable Name       | Step             | Description                                  | Shape         |
|---------------------|------------------|----------------------------------------------|---------------|
| `dfd_mcf_train`     | - Given          | Dataset to use for training                  | (3000, 14682) |
| `dfd_mcf_test`      | - Given          | Dataset to use for testing                   | (3000, 3671)  |


&nbsp;


## DropSeq - HCC1806
| Variable Name       | Step             | Description                                  | Shape         |
|---------------------|------------------|----------------------------------------------|---------------|
| `dfd_hcc_train`     | - Given          | Dataset to use for training                  | (3000, 21626) |
| `dfd_hcc_test`      | - Given          | Dataset to use for testing                   | (3000, 5406)  |