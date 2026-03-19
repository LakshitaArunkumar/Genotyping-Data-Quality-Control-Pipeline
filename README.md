## Genotyping Data Quality Control Pipeline (GWASTools, SNPRelate)

This project implements a comprehensive quality control (QC) workflow for genotyping array data using R. The pipeline identifies and corrects data inconsistencies, removes low-quality variants, and ensures a high-confidence dataset for downstream genetic analyses.

---

## Project Overview

Genotyping data often contains technical artifacts, missing values, and annotation errors that can bias downstream analyses. This pipeline applies systematic QC procedures to evaluate sample quality, variant reliability, and population structure.

---

## Objectives

- Perform quality control on genotype and annotation data  
- Identify and correct sample-level inconsistencies  
- Filter low-quality SNPs based on multiple criteria  
- Evaluate relatedness and pedigree structure  
- Assess population structure using principal component analysis  

---

## Workflow Summary

### Data Exploration and Annotation

- Loaded genotype, SNP, and sample annotation data  
- Evaluated metadata including:
  - Sample counts  
  - Family relationships  
  - Sex distribution  
  - Population groups  
  - Chromosome coverage  

---

### Missingness Filtering

- Calculated SNP-level and sample-level missingness  
- Removed SNPs exceeding missingness thresholds  
- Verified sample-level data completeness  

---

### Sex Verification

- Compared reported sex with genotype-inferred sex  
- Used X/Y chromosome intensity and heterozygosity  
- Corrected mislabeled samples  

---

### BAF and LRR Analysis

- Examined allelic imbalance using:
  - B allele frequency (BAF)  
  - Log R ratio (LRR)  

- Identified structural abnormalities such as:
  - Copy number variation  
  - Loss of heterozygosity  

---

### Relatedness and Pedigree QC

- Estimated kinship using KING  
- Compared observed vs expected relationships  
- Identified:
  - Sample swaps  
  - Pedigree inconsistencies  

- Applied corrections to ensure data consistency  

---

### Population Structure Analysis

- Performed linkage disequilibrium pruning  
- Computed principal components  
- Visualized clustering of population groups  

---

### Duplicate Discordance

- Evaluated genotype consistency across duplicate samples  
- Identified unreliable SNPs based on discordance  
- Removed discordant variants  

---

### Hardy-Weinberg Equilibrium (HWE)

- Conducted HWE testing on founder samples  
- Identified SNPs deviating from equilibrium  
- Filtered variants based on statistical thresholds  

---

## Technologies Used

- R  
- GWASTools  
- SNPRelate  
- tidyverse  
- ggplot2  

---

## Key Features

- End-to-end genotype QC workflow  
- Multi-step filtering and validation  
- Pedigree and relatedness analysis  
- Population structure assessment  
- Integration of statistical and biological QC metrics  

---

## Key Skills Demonstrated

- Genotype data quality control  
- Statistical filtering and validation  
- Population genetics analysis  
- Data cleaning and annotation management  
- Reproducible analysis using R  

---

## Notes

- QC steps are applied sequentially to ensure data integrity  
- Multiple complementary metrics are used for robust filtering  
- The final dataset is suitable for downstream genetic association analyses  

---

## Author

Lakshita Arunkumar
