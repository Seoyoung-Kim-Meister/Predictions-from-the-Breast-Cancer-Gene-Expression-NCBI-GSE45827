# Tumor vs Normal Predictions from the Breast Cancer Gene Expression Data NCBI GSE45827.
We use data from patients with primary invasive breast cancer (NCBI-GSE45827) to train a model making predictions.

## Project Overview

This project applies basic machine learning techniques to a real biological dataset — **GSE45827**, a gene expression microarray dataset containing tumor and normal samples. The goal is to build and evaluate a binary classifier that distinguishes **tumor vs normal tissue** using PyTorch, inspired by the fastai `04_mnist_basic` notebook.

The project focuses on:
- Loading and preprocessing real biological data  
- Training a simple linear classifier  
- Comparing optimizers (SGD vs Adam)  
- Understanding why accuracy alone can be misleading in biomedical ML  

---

## Dataset: GSE45827

**Source:** Gene Expression Omnibus (GEO)

- Accession: **GSE45827**
- Task: Binary classification (**Tumor = 1, Normal = 0**)
- Data type: Microarray gene expression
- Approximate shape:  
  - **Samples:** ~155  
  - **Features (genes):** ~30,000  

This dataset is commonly used in cancer genomics benchmarking because it is relatively clean and well-labeled.

---

## Data Access

You can download the dataset from GEO:

https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE45827

Alternatively, I included the file to this repository which can be found under the following name:

GSE45827_series_matrix.txt.gz
