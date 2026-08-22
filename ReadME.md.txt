Codes and Data for: Preservation and storage effects on river sediment microbiomes: Implications for community stability and ecological inference
---  
Raw sequence data are available at the NCBI Sequence Read Archive (SRA) under BioProject accession PRJNA1336108. The corresponding visualization data, processed amplicon datasets, metadata, and R codes used to generate the analyses and figures presented in the manuscript are deposited in this repository.

## Source Data
MS-Preservation-Methods_R-Codes.R                           # Main R script containing the workflow for microbial diversity, community composition, community stability, taxonomic response, and community assembly analyses, together with figure generation.
MS-Preservation-Methods_Supplementary-Tables.xlsx       # Sample metadata, sequencing summaries, statistical outputs, ASV tables, and supplementary datasets used throughout the study.
MS-Preservation-Methods_Supplementary-Information.docx  # Additional methodological descriptions and supplementary information.
src/
    bac.asv-table.tsv                                      # Processed bacterial (16S rRNA gene) ASV abundance table.
    euk.asv-table.tsv                                      # Processed eukaryotic (18S rRNA gene) ASV abundance table.
    bac.mco                                                # microeco object for bacterial communities containing ASV, abundances, taxonomy, metadata, and phylogenetic information.
    euk.mco                                                # microeco object for eukaryotic communities containing ASV, abundances, taxonomy, metadata, and phylogenetic information.
    bac.rareres                                            # Rarefaction analysis results for the bacterial dataset.
    euk.rareres                                            # Rarefaction analysis results for the eukaryotic dataset.
    null16_res_process.rds; null16_res_ses_betampd.rds     # Outputs from phylogenetic null-model analyses (16S dataset).
    null18_res_process.rds; null18_res_ses_betampd.rds     # Outputs from phylogenetic null-model analyses (18S dataset).

## Notes
The analyses were conducted in R v4.6.1 and primarily used the microeco framework for microbial community analyses and visualization. The provided microeco objects (bac.mco and euk.mco) contain the processed datasets used for most downstream analyses and figure generation, allowing users to reproduce results without repeating the full amplicon-processing workflow. Major packages used throughout the analyses include:

microeco
phyloseq
vegan
picante
ape

ggplot2
ggpubr
ComplexHeatmap
patchwork
ggh4x
ggcor
ggradar
aplot

dplyr
tidyr
magrittr
data.table
readxl
microViz

Additional packages may be required for specific analyses and visualizations (e.g., car, reshape2, textshape, DECIPHER, decontam, and others). 

## Contact
If there are issues with the code, analyses, or repository contents, please feel free to contact: joeselle.serrana@aces.su.se or joeselle.ms@gmail.com