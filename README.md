# Statistical-Analysis-Gene-Expression

# Gene Expression Analysis using Supervised and Unsupervised Machine Learning

## Introduction
This document outlines the workflow and methods used for analyzing a gene expression dataset with both supervised and unsupervised machine learning techniques.  
The analysis aims to classify samples based on gene expression levels and predict patient predisposition to invasive or non-invasive forms of cancer.

The following sections cover the methods for handling missing values, data reduction, clustering, and classification.  
The code provided can be replicated in **R**, and instructions for each step are included.

---

## Project Setup

### Load Necessary Libraries
```r
library(caTools)
library(DMwR2)
library(tidyr)
library(dplyr)
library(MASS)
library(randomForest)
library(e1071)
library(caret)
library(class)
