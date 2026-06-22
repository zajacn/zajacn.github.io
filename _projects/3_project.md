---
layout: page
title: Method and Tool benchmarking
importance: 2
category: work
img: assets/img/benchmarking_chatgpt.png
related_publications: true
---

A very important aspect of studying evolutionary history of organisms using genomic data is using the right type of data and tools and understanding the data well enough not to interpret artefacts as biological information. I had the opportunity to learn that well while working as a bioinformatician at the Functional Genomics Center Zürich, a core facility shared between University of Zurich and ETH Zurich. 

At FGCZ I performed data analysis for research projects in the topics of population genomics, biodiversity genomics, experimental evolution and medical genomics. I specialized on long read sequencing (mostly PacBio but also Oxford Nanopore), bulk RNA sequencing, pooled sequencing (Pool-seq), 16S rRNA sequencing and shotgun metagenomics/metatranscriptomics. I have also been a contributor to the ezRun package: https://github.com/uzh/ezRun.

Working in a team of bioinformaticians from a wide variety of fields both in genomics and proteomics and being in close contact with people working in the wet lab allowed me to get a unique perspective. I had a chance to participate in a range of benchmarking studies - I find that type of work very important. We published two internal studies elucidating how technical sequencing decisions can influence biological conclusions.

<h3>Long vs short reads in single cell RNAseq </h3>
<img src="/assets/images/projects/scRNAseq.jpg" alt="Screenshot" style="width:80%; border-radius:8px;">
<p>Single-cell RNA sequencing is used for profiling gene expression differences between cells.It can be performed with short reads, which provide high-throughput and high-quality information at the gene level, or with long reads, which provide isoform resolution via preserving full-length transcripts. It is, however, unclear how comparable the data is between the two methods.  </p> 
<p>We investigated the types of bias introduced at the library preparation and the bioinformatic processing steps on the transcripts recovered from long- and short-read sequencing, and the effects of filtering, enabled by sequencing of full-length transcripts, on gene expression.For each sample, we sequenced the same 10x Genomics 3′ complementary DNA (cDNA) using Illumina short reads and Pacific Biosciences long reads and cross-compared each molecule matched through cell barcode and unique molecular identifier.</p>
<p>We find that both methods render highly comparable results and recover a large proportion of cells and transcripts. However, platform-dependent cDNA library processing and data analysis steps introduce biases. Short-read sequencing provided higher sequencing depth, but long-read sequencing allowed for retaining transcripts shorter than 500 bp and for removal of degraded cDNA contaminated by template switching oligos. Filtering of artefacts, identifiable only from full-length transcripts, reduces gene count correlation between the two methods.{% cite zajac2025comparison %}</p>


<h3> The impact of PCR duplication on RNAseq data generated with 4 different sequencers</h3>
 <div class="text-center">
  <img src="/assets/images/projects/RNAseq4seq.webp" alt="Screenshot" style="width:80%; border-radius:8px;">
</div>
<p>Transcriptome sequencing (RNA-seq) is a powerful technology for gene expression profiling. Selection of optimal parameters for cDNA library generation is crucial for acquisition of high-quality data. In this study, we investigate the impact of the amount of RNA and the number of PCR cycles used for sample amplification on the rate of PCR duplication and, in consequence, on the RNA-seq data quality.</p> 
<p>We sequenced the data on four short-read sequencing platforms: <strong>Illumina NovaSeq 6000</strong>, <strong>Illumina NovaSeq X</strong>, <strong>Element Biosciences AVITI</strong>, and <strong>Singular Genomics G4</strong>. The native Illumina libraries were converted for sequencing on AVITI and G4 to assess the effect of library conversion, containing additional PCR cycles. </p>
<p>We find that the rate of PCR duplicates depends on the combined effect of RNA input material and the number of PCR cycles used for amplification. For input amounts lower than 125 ng, 34–96% of reads were discarded via deduplication with the percentage increasing with lower input amount and decreasing with increasing PCR cycles. The reduced read diversity for low input amounts leads to fewer genes detected and increased noise in expression counts.</p>
<p>Data generated with each of the four sequencing platforms presents similar associations between starting material amount and the number of PCR cycles on PCR duplicates, a similar number of detected genes, and comparable gene expression profiles.{% cite zajac2025impact %}</p>


