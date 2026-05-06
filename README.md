# Homework2

This repository contains the analysis workflow and results for a bisulfite sequencing methylation analysis performed on chromosome 20 samples.

## Goal of the project

The goal of this project was to analyze CpG methylation data from bisulfite sequencing and evaluate sample quality, coverage, and methylation-based clustering between tumour and non-tumour samples.

The analysis included:

- quality assessment of sequencing data,
- calculation of coverage statistics,
- duplication rate evaluation,
- Pearson correlation analysis,
- PCA analysis of methylation levels,
- comparison of different coverage filtering thresholds,
- visualization of coverage distribution across CpG sites.

---

# Repository structure

## `projektas2/`

Contains the R project used for the analysis.

Includes:
- R scripts / RMarkdown files,
- generated plots,
- methylation analysis workflow,
- PCA and correlation analysis code.

---

## `Grafikai/`

Contains all graphs generated in R, including:

- mapping rate plots,
- duplication rate plots,
- coverage distribution plots,
- CpG retention plots,
- Pearson correlation heatmap,
- PCA plots,
- genomic coverage visualizations.

---

## `Failai/`

Contains quality control and sequencing metric files.

Includes:
- FastQC HTML reports,
- Picard duplicate metrics files (`48metrics.txt`, `50metrics.txt`, etc.).

The metrics files were used to calculate duplication rates for each sample.

---

## `komandos2.txt`

Contains the terminal commands used during the workflow, including:
- alignment,
- duplicate marking,
- methylation extraction,
- quality control steps.

---

# Samples analyzed

| Sample ID | Condition |
|---|---|
| SRR11647648 | non_tumour |
| SRR11647650 | non_tumour |
| SRR11647658 | tumour |
| SRR11647660 | tumour |

---

# Main findings

- Coverage and total read counts were generally consistent across samples.
- SRR11647650 showed slightly lower quality due to:
  - lower read count,
  - higher duplication rate.
- Pearson correlation and PCA analyses showed separation between tumour and non-tumour samples based on methylation patterns.
- Increasing coverage filtering reduced noise but also removed a large number of CpG sites.

---

# Tools and packages used

## Main tools

- Bspam
- Picard MarkDuplicates
- FastQC
- samtools

## Main R packages

- data.table
- ggplot2
- pheatmap
- tidyverse
- patchwork
- readr

---

# Output

The project produces:
- QC summaries,
- methylation matrices,
- coverage statistics,
- clustering analyses,
- publication-style figures for interpretation of methylation patterns.
