---
layout: project
title: 'Data Mining Final Project'
caption: Classification of HRneg / Tneg Breast Cancer and Survival Analysis of Breast Cancer Patients
description: >
  Classification of HRneg / Tneg Breast Cancer and Survival Analysis of Breast Cancer Patients
date: 1 Dec 2020
image: 
  path: /assets/img/projects/data_mining_title.PNG
  srcset: 
    1920w: /assets/img/projects/data_mining_title.PNG
    960w:  /assets/img/projects/data_mining_title.PNG
    480w:  /assets/img/projects/data_mining_title.PNG
sitemap: false
---

## Data Mining Final Project

## 1. Introduction

These days, prognosis of breast cancer is widely done by measuring concentration of Hormone Receptor, HR. Whether the hormone receptor is over-expressed or not is the main standard of prognosis of breast cancer. However, there are subtypes of breast cancer which does not show any over-expression of those HR genes including HER2 and ErbB2. If there is no over-expression of HER2, we call them “HR-Negative breast cancer”-HRneg- and if there is no over-expression of both HER2 and ErbB2 genes, we call them “Triple-Negative breast cancer”-Tneg-. The reason why classification and identification of HRneg/Tneg breast cancer is important is because prognosis of those subtypes is not widely commercialized even though they could show severe cancerous symptoms.

As a result, we decided to classify subtypes of breast cancer including HRneg and Tneg using genome data of patients. Using the results of classification, we would identify some primal genes determining HRneg/Tneg breast cancer. There is phenotype information of each patients given in genomic matrix, so classification is done by supervised learning which each patient is marked by their subtypes of breast cancer. Also, since subtypes of cancer is quite imbalanced-HR positive/ErbB2 positive patients are less than 40-, we wanted to check whether undersampling or oversampling could increase the classification performance.

In addition, DMFS (Distant Metastasis Free Survival) time data per each breast cancer patients are given. DMFS is time from start point of anti-cancer therapy to metastasis of cancer to other organs or lymph nodes. We wanted to know whether we could identify meaningful interaction between genes and DMFS, so we tried survival analysis between gene data and
DMFS data for breast cancer patients.

In summary, two main goals of our project is to – 1. Classify subtypes of breast cancer, and 2. Prediction of DMFS time using survival regression method.

## 2. Data Description

We used datasets from UCSC Xena: Breast Cancer provided by Yau, 2010. There are two datasets which is GenomicMatrix and Phenotype. There were no NA value for all variables in Genomic Matrix and Phenotype.

### 2.1. GenomicMatrix (microarray)

GenomicMatrix data is consisted of probe-level median-normalized and log10-transformed microarray data from 683 breast cancer patients. There are total 9169 genes, so the size of genomic matrix is 9169*683.

### 2.2 Phenotype

Phenotype data is consisted of 1) types of tumor cells, 2) subtypes of breast cancer 3) whether there was metastasis to other organs 4) DMFS per each patient. We would only use 2) subtypes of breast cancer for the section 3 and 4) DMFS for section 4.

### 2.3. EDA

There are 4 types of breast cancer – ERneg_ERBB2neg , ERneg_ERBB2pos, ERpos_ERBB2neg, ERpos_ERBB2pos. For the first goal of our project, we checked the distribution of the types of breast cancer.

![data_mining_fig1](/../assets/img/projects/data_mining_fig1.PNG){:.lead width="600" height="70" loading="lazy"}

Distribution of 4 types of Breast Cancer
{:.figcaption}

For the second goal of our project, we checked boxplot of DMFS time for each type of breask cancer. As shown in Figure 2, it seems there is no relationship between the type of cancer and DMFS time.


![data_mining_fig2](/../assets/img/projects/data_mining_fig2.PNG){:.lead width="800" height="100" loading="lazy"}

Boxplot of DMFS time
{:.figcaption}


