# Project1
Make gene alignment pipline from your own data and own scripts
to use in Compute Canada

#PLAN
- your script drafts can go in this project and you can move/run them in computecanada
- Can download a PAb and CAb (exp and cntrl Ab) dataset to your local and test that way (?)
    may be too slow
    can also use the terminal within VSCode

#PIPLINE OUTLINES
Mine: 
FASTQC quality check, then convert to SAM/BAM, then align 
(lol)

Gorini 2020
- QC: NGS-QC Toolkit
- Alignments: BWA
    - to hg18
- Filtering & file format conversions: SAMtools and bedtools
- Peaks idenified: MACS
    - from uniquely mapped reads without duplicates
    - P< 1e-5 and fold enrichment >7
    - DNA input control
- Data visualization: UCSC Genome Browser
- Normalized uniquely mapped reads: BamCompare tool in Deeptools suite
    - unique reads normalized over input 
    - log2 OG/input ratio
    - SES method as scaling factor
    - fixes any GC sequencing bias or DNA amount differences
- Metagene analysis: computeMatrix in Deeptools
- Heatmaps: plot Heatmap tools in Deeptools
- Signal profile plots: R 
    - from the matrices from computeMatrix