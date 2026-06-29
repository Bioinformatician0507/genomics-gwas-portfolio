# Genomics GWAS Portfolio

End-to-end genomics pipelines built with PLINK2, bcftools, and Python.
Covers GWAS, variant calling, population stratification, and polygenic risk scoring.

**Author:** Iqra Nadeem | MSc Bioinformatics | University of Agriculture Faisalabad

---

## Project 1 — GWAS Pipeline

**Tools:** PLINK2, Python, matplotlib  
**Dataset:** Synthetic (500 samples, 50,000 SNPs)  
**Notebook:** [Open in Colab](https://colab.research.google.com/drive/1wx-VayEWBuPMsq3hy1CqZsNwRYpuzEz5#scrollTo=ifGNH3X0pMac)

### What I did
- Installed PLINK2 and generated a synthetic GWAS dataset
- Applied standard QC filters: genotype missingness (--geno 0.05),
  sample missingness (--mind 0.1), MAF (--maf 0.01), HWE (--hwe 1e-6)
- 47,974 variants passed QC from 50,000 input SNPs
- Ran Firth logistic regression association testing (binary phenotype:
  258 cases, 242 controls)
- Generated Manhattan plot and QQ plot (genomic inflation λ = 0.974)

### Key result
Well-calibrated pipeline with no genomic inflation. No false positives
on null synthetic data — correct behaviour confirming pipeline validity.

### Figures
![GWAS Plots](gwas_plots.png)

---

## Project 2 — Variant Calling Pipeline
*Coming soon*

## Project 3 — Population Stratification + PCA
*Coming soon*

## Project 4 — Polygenic Risk Score (PRS)
*Coming soon*
