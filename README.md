# RNA-seq Analysis of Matched Breast Cancer and Brain Metastasis Cell Lines

## Project Overview

This project focuses on RNA sequencing (RNA-seq) data from matched breast cancer and brain metastasis cell lines. The study investigates RNA expression in human-derived breast cancer cell lines and their brain-metastatic counterparts.

The project demonstrates a bioinformatics workflow involving sequencing quality control, read alignment, alignment file processing, and gene-level read counting.

## Dataset Information

- **Study Title:** RNA-seq of matched breast cancer and brain metastasis cell lines
- **Organism:** *Homo sapiens*
- **BioProject:** PRJEB91058
- **SRA Study:** ERP174054
- **Sequencing Platform:** Illumina
- **Library Strategy:** ssRNA-seq
- **Library Selection:** PolyA
- **Sequencing Layout:** Paired-end
- **Reference Genome:** Human GRCh38 (hg38)

### Selected Samples

- `ERR15159015`
- `ERR15159016`

## Project Objectives

- Assess sequencing quality using FastQC.
- Align paired-end RNA-seq reads to the human reference genome using HISAT2.
- Process, sort, and index alignment files using SAMtools.
- Generate gene-level read counts using featureCounts.
- Organize quality control reports and alignment statistics.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| FastQC | Quality assessment of sequencing reads |
| HISAT2 | Alignment of reads to the reference genome |
| SAMtools | Processing, sorting, and indexing alignment files |
| featureCounts | Gene-level read counting |
| Ubuntu / WSL | Command-line bioinformatics environment |

## Analysis Workflow

### 1. Quality Control

FastQC was used to generate reports for assessing sequencing read quality, GC content, sequence length, and other quality metrics.

### 2. Read Alignment

HISAT2 was used to align paired-end sequencing reads against the human reference genome (hg38). Alignment logs were retained to review mapping statistics.

### 3. Alignment Processing

SAMtools was used to process, sort, and index alignment files for downstream analysis.

### 4. Gene-Level Read Counting

featureCounts was used to assign aligned reads to annotated genes and generate gene-level read counts.

### 5. Output Organization

FastQC reports, HISAT2 alignment logs, and the featureCounts summary were organized into separate folders for documentation and review.

## Repository Structure

```text
RNA-seq-Gene-Expression-Analysis/
├── FastQC/
│   └── FastQC HTML and ZIP reports

├── Alignment_Logs/
│   └── HISAT2 alignment logs
├── Counts/
│   └── featureCounts summary
└── README.md
```

## Analysis Scope

This project documents the RNA-seq processing workflow, including sequencing quality control, reference genome alignment, and gene-level read counting.

Differential gene expression analysis was not performed. Differences between sequencing runs alone are not sufficient to establish differential gene expression. A valid comparison requires clearly defined biological groups, sample metadata, and an appropriate experimental design.

## Skills Demonstrated

- RNA-seq data processing
- Sequencing quality control
- Reference genome alignment
- SAM/BAM file processing
- Gene-level read counting
- Linux command-line operations
- Bioinformatics workflow documentation

## Data Source

NCBI Sequence Read Archive (SRA)

- **BioProject:** [PRJEB91058](https://www.ncbi.nlm.nih.gov/bioproject/PRJEB91058)
- **SRA Study:** [ERP174054](https://trace.ncbi.nlm.nih.gov/Traces/?study=ERP174054)
- **NCBI SRA:** [ERR15159016](https://www.ncbi.nlm.nih.gov/sra/ERR15159016)

## Data Availability

Large raw sequencing files

## Trimming 
Read trimming was not performed because the FastQC report showed acceptable adapter content. Therefore, adapter trimming was not considered necessary based on this quality control result.
