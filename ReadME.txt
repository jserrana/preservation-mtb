MS-Preservation-Methods
Overview

This repository contains the R code, processed amplicon sequencing datasets, metadata, and intermediate analysis objects required to reproduce the microbial community analyses, statistical tests, null-model analyses, and figures reported in the associated manuscript.

The repository includes:

Analysis and visualization scripts written in R.
Sample metadata and supplementary datasets.
Processed bacterial and eukaryotic amplicon sequencing data.
Microeco objects used for downstream analyses and figure generation.
Precomputed rarefaction and null-model outputs to facilitate reproducibility.
Repository Structure
MS-Preservation-Methods/
│
├── README.md
├── MS-Preservation-Methods_R-Codes.R
├── MS-Preservation-Methods_Supplementary-Information.docx
├── MS-Preservation-Methods_Supplementary-Tables.xlsx
│
├── src/
│   ├── bac.asv-table.tsv
│   ├── bac.mco
│   ├── bac.rareres
│   ├── euk.asv-table.tsv
│   ├── euk.mco
│   ├── euk.rareres
│   ├── null16_res_process.rds
│   ├── null16_res_ses_betampd.rds
│   ├── null18_res_process.rds
│   └── null18_res_ses_betampd.rds
│
└── output/

Data Description
Supplementary Tables

MS-Preservation-Methods_Supplementary-Tables.xlsx

This file contains the metadata and supporting datasets required for reproducing the analyses described in the manuscript. These tables include sample information, treatment design, environmental metadata, and other information used during downstream community analyses and statistical testing.

Supplementary Information

MS-Preservation-Methods_Supplementary-Information.docx

Provides additional methodological details, parameter settings, workflow descriptions, and supplementary explanations supporting the manuscript.

Amplicon Sequencing Data
Bacterial ASV Table

bac.asv-table.tsv

Amplicon Sequence Variant (ASV) abundance table for bacterial communities.

Rows correspond to ASVs and columns correspond to samples. This table can be used for downstream community ecology analyses such as diversity estimation, ordination, differential abundance analysis, and community assembly investigations.

Eukaryotic ASV Table

euk.asv-table.tsv

Amplicon Sequence Variant (ASV) abundance table for eukaryotic communities.

Rows correspond to ASVs and columns correspond to samples.

Microeco Objects

The analyses were primarily conducted using the R package microeco.

bac.mco

Processed bacterial microeco object containing:

ASV abundance data
Taxonomic annotations
Sample metadata
Derived community-analysis structures
euk.mco

Processed eukaryotic microeco object containing:

ASV abundance data
Taxonomic annotations
Sample metadata
Derived community-analysis structures

These objects allow direct reproduction of most analyses and figures without repeating the complete preprocessing workflow.

Rarefaction Results
bac.rareres

Rarefaction results generated from the bacterial community dataset.

euk.rareres

Rarefaction results generated from the eukaryotic community dataset.

These objects were used to evaluate sequencing-depth sufficiency and sampling completeness.

Community Assembly and Null-Model Outputs

The repository includes precomputed null-model results used to investigate deterministic and stochastic community assembly processes.

null16_res_process.rds

Community assembly process estimates generated under Null Model 16.

null16_res_ses_betampd.rds

Standardized Effect Size (SES) βMPD results generated under Null Model 16.

null18_res_process.rds

Community assembly process estimates generated under Null Model 18.

null18_res_ses_betampd.rds

Standardized Effect Size (SES) βMPD results generated under Null Model 18.

These files contain intermediate and final analytical outputs and are included to facilitate reproducibility and verification of manuscript results.

Analysis Workflow

The primary workflow is contained in:

MS-Preservation-Methods_R-Codes.R


The script includes:

Import of metadata and processed datasets.
Loading of microeco objects.
Community diversity analyses.
Beta-diversity calculations and ordinations.
Statistical hypothesis testing.
Community assembly analyses.
Generation of publication figures and tables.
Software Requirements

Analyses were conducted in R (version 4.0 or higher).

Primary packages include:

microeco
tidyverse
vegan
ape
picante
ggplot2
ggpubr
patchwork
reshape2
data.table
readxl


Additional package dependencies are loaded within the R scripts.

Reproducing the Results
Step 1

Download or clone the repository while preserving the directory structure.

Step 2

Install all required R packages.

Step 3

Open the main R script:

MS-Preservation-Methods_R-Codes.R

Step 4

Set the working directory to the repository root.

Example:

setwd("MS-Preservation-Methods")

Step 5

Run the script sequentially to reproduce analyses and figures.

source("MS-Preservation-Methods_R-Codes.R")


Generated outputs may be saved to the output/ directory.

Reproducibility Notes
All analyses rely on the metadata provided in the Supplementary Tables.
Processed microeco objects are provided to avoid repeating computationally intensive preprocessing steps.
Null-model outputs are included to allow direct verification of community assembly results.
Maintaining the original folder structure is necessary for successful execution of the scripts.
Citation

If you use these data, scripts, or derived outputs, please cite the associated manuscript and acknowledge this repository as the source of the analytical workflow and processed microbial community datasets.

Contact

For questions regarding the datasets, scripts, or reproducibility of analyses, please contact the corresponding author listed in the associated manuscript.