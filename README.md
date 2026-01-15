# Tumor vs Normal Predictions from the Breast Cancer Gene Expression Data NCBI GSE45827.
This repository explores the application of Neural Networks and Dimensionality Reduction (PCA) to classify breast cancer subtypes using gene expression data from the NCBI Gene Expression Omnibus (GEO).

## Project Overview

This project applies basic machine learning techniques to a real biological dataset — **GSE45827**, a gene expression microarray dataset containing tumor and normal samples. The goal is to build and evaluate a binary classifier that distinguishes **tumor vs normal tissue** using PyTorch and scikit-learn.

The project focuses on:
- Loading and preprocessing real biological data  
- Training a simple linear classifier 
- Comparing optimizers (SGD vs Adam)
- Improving the linear classifier by adding non-linear layers (ReLU) 
- Understanding why accuracy alone can be misleading in biomedical ML  

## Dataset: GSE45827

**Source:** Gene Expression Omnibus (GEO)

- Accession: **GSE45827**
- Task: Binary classification (**Tumor = 1, Normal = 0**)
- Data type: Microarray gene expression
- Approximate shape:  
  - **Samples:** ~155  
  - **Features (genes):** ~30,000  

The dataset contains expression profiles for primary invasive breast cancer. The goal is to classify samples into their respective biological subtypes:

Basal-like (Triple-negative)

HER2-positive

Luminal A

Luminal B

Normal-like tissue and cell lines.

## The "Small-n, Large-p" Challenge

In bioinformatics, we often face the challenge of having a very small number of samples (n≈150) but a massive number of features (p~30,000 gene probes).

This project serves as a transparent case study on the difficulties of training Deep Learning models on small biological datasets. Current models may perform near or below the mean baseline accuracy due to:

High Variance: Small validation sets can lead to inconsistent accuracy metrics.

Overfitting: The model easily "memorizes" the specific 150 samples rather than learning general biological patterns.

Class Imbalance: Significant differences in the number of samples per subtype (e.g., 41 Triple-negative vs. 11 Normal).

## Data Access

You can download the dataset from GEO:

https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE45827

Alternatively, I included the file to this repository which can be found under the following name:

GSE45827_series_matrix.txt.gz
