# Bioinformatics

This repository contains bioinformatics analysis workflows
focused on long-read sequencing and variant analysis.

## Main topics
- Read mapping (minimap2, STAR, hisat2)
- BAM processing (samtools)
- Variant calling and filtering (bcftools)
- Custom VCF filtering scripts

## Environment
- Linux
- Bash / Python / R

## Example
```bash
minimap2 -ax map-ont ref.fasta reads.fastq | samtools sort -o aln.bam

