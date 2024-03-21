# Formichetti et al., 2024 - A murine allelic series of *Ogt* catalytic hypomorphic mutants uncovers the requirement of O-GlcNAc for embryonic development

# Introduction

* This repository contains all code used to generate the figures and conclusions based on RNA-Seq data contained in paper "A murine allelic series of *Ogt* catalytic hypomorphic mutants uncovers the requirement of O-GlcNAc for embryonic development" ([Formichetti et al. 2024](link to biorxiv to add)).

* For each sequencing dataset, there is a subrepository with a self-explanatory name.

# General overview of the workflows

## Analysis of single copy genes

1. a Galaxy pipeline starting from fastq files to read counts, found in **src/galaxy**: which outputs:

* transcripts counts in the case of MEFs and placentae, summarized at gene level downstream in Rmd
* gene counts in the case of single blastocysts

<n>

2. different kinds of custom downstream analyses using the output of the pipeline and performed with R, all included in Rmd files with self-explanatory names, found in **src/Rmd** and **whose output is [here](https://boulardlab.github.io/Ogt_mouse_models_Formichetti2024/)**. Order for running the Rmd, if more than one and if not obvious, is specified in the main README of each subdirectory.

## Analysis of retrotransposons' expression

1. a custom snakemake pipeline, found in **snake-make/TE_RNASeq.Snakefile** of each subrepository. Config files for the pipeline are in config/ and conda environments are in env/conda

<n>

2. custom downstream analyses using the output of the pipeline and performed with R, all included in **src/Rmd/TE_analysis.Rmd** and **whose output is [here](https://boulardlab.github.io/Ogt_mouse_models_Formichetti2024/)**.

# Raw data

Sequencing data generated in our study are available at:

* [E-MTAB-13499: “Smart-Seq of female and male blastocysts from mothers bearing the OgtT931A and OgtT931del mutations”](https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-13499?key=4772105a-02c5-4875-9491-ede05d2130f8)
* [E-MTAB-13299: "mRNA-Seq of placentas bearing the OgtY851A mutation"](https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-13299?key=e2d8ae00-4772-440d-a33b-b1caa54d12e2)
* [E-MTAB-13297: "SMART-Seq of untreated and auxin-treated blastocysts for OGT degradation"](https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-13297?key=3a236f18-ae3f-4d75-8969-c602f88e68c2)
* [E-MTAB-13298: "mRNA-Seq of primary MEFs untreated or treated with auxin for OGT degradation"](https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-13298?key=ceafd6c8-154a-4645-bb8a-907a68126419)







