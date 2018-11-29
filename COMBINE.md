# Notes

## 10.26 COMBINE

1. Matthew DeMaere [![alt text][1.1]][2] "bin3C : Hi-C mediated retrieval of metagenome-assembled genomes (MAGs)
  - Bin3C [github repo](github.com/cerebis/bin3C)
  - Rates of observation of interacting loci
    - intra-chrom > inter-chrom > inter-cellular
  - Infomap [link](http://mapequation.org)
    - unsupervised
    - flow based clustering
    - no resolution limit
    - minimize description length (MDL) of random walker paths

2. Holly Whitfiled [![alt text][1.1]][3] "MicroRNA-Mediated Regulatory Networks within Breast Cancer Progression"
  - circRNA competing model (Competing endogenous RNAs absorb microRNA and affect regulation)
    - circRNA compete with miRNA as a sponge,
    - negative correlate with miRNA and positive correlate with miRNA target genes
  - Exon intron split analysis

3. Brendan Robert E Ansell Machine learning and protein structure prediction to support annotation of pathogen genomes
  - I-TASSER [link](https://doi.org/10.1093/gigascience/giy150)
  - using matching PFAM domains as a measure of confidence in matches
  - random forest classifier based on quality metrics. Model trained on Giardia data is effective for human proteins. Identified some high quality matches that don't have PFAM domains

4. Jamie-Lee Thompson Transcriptome-wide RNA sequencing analysis of immobilisation-induced muscle atrophy
  - remove top 10 overrepresented sequence from FastQC (because it skew GC content)
  - GSEA using clusterProfiler and ReactomePA
  - Cytoscape visualization (Reactome)

5. Peter Georgeson [![alt text][1.1]][4] Identifying and characterising high resolution mutational signatures from DNA mismatch repair deficient tumours
  - Existing cancer signatures don't include indels which are a sign of microsatellite instability
  - MSI cancer - colon, stomach, endometrial
  - Variant call in low complexity regulation
  - INDEL can be target for immune therapy
  - COSMIC mutational signatures 30
  - MSIseq [link](https://cran.r-project.org/web/packages/MSIseq/index.html) to detect and filter for MSI-H samples

6. Emma Gail "Systematic mapping of molecular interactions within the epigenetic modifier complex PRC2 provides a mechanistic framework for its functional diversity"
  - PRC2 complex
    - EZH2 catalytic
    - EED Regulatory
    - RBBP4 histone binding
    - SUZ12 scaffold
  - cofactors
  - crisscrosslinker package for XL-MS data analysis [github repo](https://github.com/egmg726/crisscrosslinker)

7. Jake Bradford [![alt text][1.1]][5] "A Performance Review of Computational Tools for CRISPR-Cas9 Guide Design"
  - spacer + PAM (3'-NGG sequence)
  - Benchmark [github repo](https://github.com/jakeb1996/SBS )
A simple method for launching a process and collecting system resource utilisation statistics

8. Katarina Stuart [![alt text][1.1]][6] "Evolution in invasive populations: using genomics to reveal drivers of invasion success in the Australian European starling (Sturnus vulgaris) introduction across Australia."
  - using Redundancy analysis (RDA) to find variability associated with predictors and identify candidate SNPs involved in evolution

9. Dharmesh Bhuva [![alt text][1.1]][7] dcanr software for simulating differential co-expression networks
  - dcanr package [github repo](https://github.com/davislaboratory/dcanr)
  - ENT entrophy based method
  - Z-score method is better than ENT
  - high degree nodes in differential network is often targets not DE

10. Vindhya Vasini Shatdarsanam
  - PLINK
  - BOOST
  - AntEpiseeker

11. Andrian Yang "Scavenger: A pipeline for recovery of unaligned reads utilising similarity with aligned reads"
  - Scavenger [github repo](https://github.com/vccri/scavenger)
  - increase reads for lowly expressed genes
  - for bulk ofter pseudogene
  - for single cell often protein coding
  - using metamorphic testing to evaluate aligners.
  - After added a chromosome made up of unaligned reads then realign unaligned reads

12. Mengbo Li [![alt text][1.1]][8] Using Omics Data to Guide Classification in Neuroimaging Studies of Brain Diseases
  - fMRI integrate with RNA-seq
  - combining gene expression from the human brain atlas, clinical fMRI imaging and annotation databases
  - sample matches by spatial region


[1.1]: http://i.imgur.com/tXSoThF.png (twitter icon with padding)
[2.1]: http://i.imgur.com/0o48UoR.png (github icon with padding)
[1]: http://www.twitter.com/_lazappi_
[2]: https://twitter.com/cerebis1
[3]: https://twitter.com/_hollywhitfield
[4]: https://twitter.com/petergeorgeson
[5]: https://twitter.com/jakebradfordqut
[6]: https://twitter.com/Katarina_Stuart
[7]: https://twitter.com/dhrmsh36
[8]: https://twitter.com/rylmb1
