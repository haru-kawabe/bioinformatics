# Bioinformatics Pipeline Portfolio

Hi there 👋  
This repository showcases my **bioinformatics pipelines**, focused on **short or long-read sequencing**, **variant calling**, and **RNA-seq alignment**.  
All workflows are designed to run in **Linux / Bash environment** without Python dependencies.

---

## 📌 Featured Workflows

### 1. short or Long-read Variant Calling Pipeline
- Map long reads using **minimap2**  
- Sort and index BAM files with **samtools**  
- Call variants using **bcftools**  
- Filter variants based on **MQ, DP, and ALT allele ratio** using `filter_vcf.sh`  

### 2. RNA-seq Alignment Workflow
- Align RNA-seq reads using **STAR** or **HISAT2**  
- Generate sorted BAM files for downstream analysis  
- Count reads per gene for expression analysis

---

## 🧰 Tools & Skills

- Linux / Bash scripting (workflow automation)  
- Long-read mapping: minimap2  
- BAM processing: samtools  
- Variant calling & filtering: bcftools  
- RNA-seq alignment: STAR, HISAT2  
- Workflow reproducibility and organization  
- Git / GitHub version control  

---

## ⚡ Example Commands

```bash
# Long-read mapping
minimap2 -ax map-ont ref.fasta reads.fastq | samtools sort -o aln.bam

# Variant calling
bcftools mpileup -f ref.fasta aln.bam | bcftools call -mv -Oz -o variants.vcf.gz

# VCF filtering
bash scripts/filter_vcf.sh variants.vcf.gz filtered.vcf 0.8

# Run full variant calling pipeline
bash scripts/run_variant_pipeline.sh ref.fasta reads.fastq sample1

# RNA-seq alignment
bash scripts/rna_seq_align.sh genome_index sample.fastq sample1
