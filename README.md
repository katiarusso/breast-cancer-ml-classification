# **Machine Learning Across Breast Cancer Cell Lines**
*Katia Russo* - *Sofia Lambro* - *Enrico Adamo* - *Matteo Colantoni* - *Andrea Porta*

---
 
## **Introduction**

Hypoxia, a condition of reduced oxygen availability, plays a pivotal role in the progression of numerous diseases, including cancer. Understanding the transcriptional response of cells to hypoxic stress is essential for identifying biomarkers and therapeutic targets. In this project, we aim to classify single cells as normoxic or hypoxic based on their gene expression profiles. The data comprises single-cell RNA-sequencing (scRNA-seq) measurements from two human breast cancer cell lines (MCF7 and HCC1806), captured using two different technologies: Smart-seq and Drop-seq.  

This project aims to harness machine learning and statistical modeling to identify and validate a robust hypoxia signature from gene expression data. By integrating exploratory data analysis, unsupervised clustering, and supervised classification, we seek to develop predictive models capable of reliably detecting hypoxic tumor cells based on transcriptomic profiles.  

Throughout, we emphasize interpretability, reproducibility, and biological validity, aligning our workflow with best practices in computational biology and machine learning.

### **Folder Overview**

- `/Data/`: Contains all raw, filtered, and preprocessed data files.
  - `/SmartSeq/`: Includes metadata, unfiltered raw counts (for EDA/QC), and filtered/normalized datasets for training and testing.
  - `/DropSeq/`: Contains filtered and normalized training and test matrices only.
  - `buffa_hypoxia.gmt` : Buffa Signature of genes related with hypoxia, used for comparison.
  - `MSigDB_Hallmark.gmt` and `GO_BP.gmt` : used for biological enrichment analysis

- `/MCF7/`: Contains all Jupyter notebooks used in the analysis of MCF7 cell line.
  - `/Models/`: Stores trained machine learning models, scalers, and gene selectors in `.pkl` format for reproducibility.
  - `Predictions.tsv` : Final outputs containing predictions for the unlabeled test sets in `.csv` format.
  
- `/HCC1806/`: Identical structure applied to HCC1806.
  - `/Models/`
  - `Predictions.tsv`

### **Nootebooks Workflow per Cell-Line**

1. **Raw Exploration**: Performed only on Smart-seq unfiltered data to explore gene/cell quality and applied the filtering process.
2. **Unsupervised Learning**: Applied to the instructor-provided filtered training datasets (Smart-seq and Drop-seq), and explored the underlying structure of the dataset without labels.
3. **Supervised Learning**
Used Logistic with Elastic Net and Random Forests to select biologically and statistically informative genes. Compares multiple classifiers using cross-validation and saves the best models.
4. **Predictions**: Loads saved models and applies them to the test sets to produce prediction files. Explains predictions using model interpretability tools like SHAP.

> Each notebook is self-contained and focused on a specific step, enabling independent execution and review while ensuring a clear end-to-end pipeline from raw data to prediction.
