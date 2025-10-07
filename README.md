
# Introduction
This document outlines the workflow and methods used for analyzing a gene expression dataset with both supervised and unsupervised machine learning techniques. The analysis aims to classify samples based on gene expression levels and predict patient predisposition to invasive or non-invasive forms of cancer.

The following sections cover the methods for handling missing values, data reduction, clustering, and classification. The code provided can be replicated in R, and instructions for each step are included.

# Project Setup

```{r setup, include=FALSE}
# Load necessary libraries
library(caTools)
library(DMwR2)
library(tidyr)
library(dplyr)
library(MASS)
library(randomForest)
library(e1071)
library(caret)
library(class)
```

## 1. Data Preparation
Load the gene expression dataset and conduct an initial review:

1.Identify and handle missing values.

2.Use k-NN imputation for filling missing entries, as it produced the lowest misclassification error during model testing.

## 2. Dimensionality Reduction
To reduce the complexity of the dataset, we apply:

**Supervised Reduction:** Two-Sample T-test, reducing the dataset to significant genes.
**Unsupervised Reduction:** Variance method and t-SNE to capture high-variance genes and visualize low-dimensional clusters.

## 3. Unsupervised Learning Techniques
This project uses clustering techniques to group genes and patients:

**Principal Component Analysis (PCA):** Reduces dimensionality and visualizes data variability.
**K-means Clustering:** Groups data into clusters; optimal number determined by elbow method.
**Hierarchical Clustering:** Displays data relationships through hierarchical structure.

## 4. Supervised Learning Techniques
Multiple supervised learning models were evaluated for classification accuracy:

**Logistic Regression:** Predicts binary class (invasive/non-invasive).
**Linear Discriminant Analysis (LDA):** Separates classes by linear combination of features.
**Random Forest:** Ensemble learning model for higher accuracy in prediction.
**Support Vector Machine (SVM):** Finds an optimal boundary between classes.
**Naive Bayes:** Applies probabilistic classification.
**k-Nearest Neighbors (k-NN):** Non-parametric classifier with optimal k found by cross-validation.
Each model's performance is assessed by calculating misclassification errors using confusion matrices.

## 5. Model Evaluation and Conclusion
Each model's accuracy was compared, with k-NN showing the lowest misclassification error, making it the most suitable for this dataset.
Clustering information was also included in the k-NN model, though it did not significantly improve accuracy.

## References
DataCamp: Introduction to t-SNE
J. C. Avendano et al., "Application of Statistical Machine Learning Algorithms for Classification of Bridge Deformation Data Sets," IEEE, 2021.

## Appendix
This appendix includes general code snippets for each analysis part. Please refer to the PDF for complete details on hyperparameters and specific model settings.

