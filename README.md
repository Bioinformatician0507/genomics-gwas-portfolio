# Project 1 — GWAS Pipeline

## Overview
End-to-end GWAS pipeline on a synthetic dataset using PLINK2 and Python.

## Tools
- PLINK2 v2.00a5.10
- Python (pandas, numpy, matplotlib)

## Pipeline Steps
1. Generated synthetic dataset: 500 samples, 50,000 SNPs, binary phenotype
2. Quality control filters:
   - Genotype missingness: --geno 0.05
   - Sample missingness: --mind 0.1  
   - Minor allele frequency: --maf 0.01
   - Hardy-Weinberg equilibrium: --hwe 1e-6
   - Result: 47,974 variants passed QC
3. Association testing: Firth logistic regression (258 cases, 242 controls)
4. Visualization: Manhattan plot + QQ plot

## Results
- Genomic inflation factor λ = 0.974 (well-calibrated, no inflation)
- 0 genome-wide significant hits (expected — synthetic null data)
- Pipeline validated on null data before application to real datasets

## Figures
![GWAS Results](gwas_plots.png)

## How to Run
Open `project1_gwas_pipeline.ipynb` in Google Colab (free T4 GPU recommended).
**Notebook:** [Open in Colab](https://colab.research.google.com/drive/1wx-VayEWBuPMsq3hy1CqZsNwRYpuzEz5#scrollTo=ifGNH3X0pMac)

All dependencies install in the first cell.
