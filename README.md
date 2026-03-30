# MAG Reconstruction and Taxonomic Classification Pipeline

This pipeline performs reconstruction of metagenome-assembled genomes (MAGs) from shotgun metagenomic data, followed by quality assessment and taxonomic classification. It integrates read mapping, binning, genome quality evaluation, and genome taxonomy assignment.

---

## Workflow

1. Mapping reads to assembled contigs (BWA, SAMtools)
2. Generation of contig coverage depth (jgi_summarize_bam_contig_depths)
3. Genome binning (MetaBAT2)
4. Quality assessment of bins (CheckM)
5. Filtering of high-quality MAGs
6. Extraction of high-quality genomes (HQ MAGs)
7. Taxonomic classification (GTDB-Tk)

---

## Tools Used

- BWA
- SAMtools
- MetaBAT2
- CheckM
- GTDB-Tk

---

## Input

- Assembled contigs (contigs.fasta)
- Paired-end sequencing reads (FASTQ files)

---

## Output

- Sorted BAM files
- Contig depth file (depth.txt)
- Genome bins (MetaBAT2 output)
- Quality assessment reports (CheckM)
- High-quality MAGs (HQ_MAGs)
- Taxonomic classification results (GTDB-Tk output)

---

## Usage

Run the pipeline using:

```bash
bash mag_pipeline.sh
