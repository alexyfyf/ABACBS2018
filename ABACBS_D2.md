
## 10.27 ABACBS DAY1

1. __KEYNOTE__ Chris Saunders [![alt text][1.1]][2] Improving sequence analysis to increase the clinical value of whole genome sequencing.
  - Notes from LukeZappia [![alt text][1.1]][1]![image](https://pbs.twimg.com/media/DtC2cSOU4AAy0cg.jpg)
  - strelka2: germline and somatic __small variant__ caller [github](https://github.com/Illumina/strelka)
  - Indel calling: strelka2 > GATK4 ~ GATK4 wo/BQSR > FreeBayes
  - Extract parameterized error distribution for SNVs
  - Extract per-sample and joint-sample error properties from as set od tumor samples and a normal control
  - In liqued tumor, normal sample is frequently contaminated, such as AML
  - tumor/nomal somatic calling: strelka2 > mutect2 > vardict
  - manta: __Structural variant (SV)__ and indel caller for mapped sequencing data [github](https://github.com/Illumina/manta)
  - canvas: __Copy number variant (CNV)__ calling from DNA sequencing data [github](https://github.com/Illumina/canvas)
  - ExpansionHunter: A tool for estimating repeat sizes, __repeated expansion__ [github](https://github.com/Illumina/ExpansionHunter)
  - paragraph: __graph based genotyping__ Graph realignment tools for structural variants [github](https://github.com/Illumina/paragraph)
  - Polaris: Data and information about the Polaris study __population sequencing resources__ [github](https://github.com/Illumina/Polaris)


2. Amali Thrimawithana [![alt text][1.1]][3], Manuka genome and beyond - a case of hybrid technologies and methodologies to unravel the plant genome

3. James Hogan, Fast Clustering of Very Large Sequence Collections
  - ParKTree: parallel k-tree clustering for biological sequences using topological signatures [github](https://github.com/tchappell/parktree)
  - SigClust: k-means clustering for biological sequences using topological signatures [github](https://github.com/tchappell/SigClust)

4. Charity Law A data-driven approach to characterising intron signal in RNA-seq data
  - unable to make it due to unwellness
  - read bioRxiv [link](https://www.biorxiv.org/content/early/2018/06/21/352823)

5. Momeneh Foroutan [![alt text][1.1]][4], Single sample scoring of molecular phenotypes
  - singscore [Bioconductor](https://bioconductor.org/packages/release/bioc/html/singscore.html) or [github](https://github.com/DavisLaboratory/singscore)
  - more robust compare to ssGSEA, GSVA, PLAGE, z-score
  - all other 4 tools need to normalize through all samples, ssGSEA also normalize through all gene sets
  - singscor real single sample scoring

6. __KEYNOTE__ Nick Hamilton [![alt text][1.1]][5] Modelling, predicting and understanding kidney development using microscopy imaging
  - visualisation of kidney development as a tree, reconstructed from imaging data
  - discordance metric: measures distance
  - inclusion metric: measures overlap
  - mean balance is uniform across lobes
  - hald-delay model to mimic the asymmetric of a real kidney

7. Thomas Boudier [![alt text][1.1]][6], WEHI imaging
  - 3D ImageJ Suite [link](http://imagejdocu.tudor.lu/doku.php?id=plugin:stacks:3d_ij_suite:start)
  - image processing: RAW -> Filter -> Object -> Infomation
  - Process -> segmentation -> quantification
  - one threshlod per Object
  - ML on shape of different cell cycle stage to classify and denoise
  - Dictionaty learning
  - Radomness: G-fucntion and F-fucntion

8. Damien Hicks, Maps of variability in cell lineage trees

9. Clare Sloggert, Reduct: interactive visualisation of high-dimensional data
  - [reduct.org](http://reduct.org)
  - [github](https://github.com/claresloggett/reduct)
  - include: PCA, MDS, tSNE, UMAP

10. __KEYNOTE__ Nancy Zhang Transfer Learning in Single Cell Transcriptomics
  - Note from LukeZappia [![alt text][1.1]][1] ![image](https://pbs.twimg.com/media/DtEEBpuVsAAUZYx.jpg)
  - saver: Single-cell RNA-seq Gene Expression Recovery [github](https://github.com/mohuangx/SAVER)
  - human cell atlas [link](https://preview.data.humancellatlas.org)
  - mouse cell atlas [link](http://bis.zju.edu.cn/MCA)
  - saver trained on mouse and human single cell datasets (autoencoder network): SAVER-X
  - single cell RNA-seq data with UMI can be modeled by Poisson sampling with cell specific sampling efficiency
  - SAVER independent evaluated [here](https://f1000research.com/articles/7-1740/v1) by Tallulah S. Andrews [![alt text][1.1]][7] and Martin Hemberg [![alt text][1.1]][8]
  - SAVER remove techinical noise, keep biological variation without introducing spurious structure
  - transfer learning harness existing data to denoise new data: healthy to disease, cross-species
  - SAVER-X: [link](https://singlecell.wharton.upenn.edu/saver-x/)

11. Victoria Jackson Uncovering the genetic basis of speech through sequencing of probands with childhood apraxia of speech
  - GRIDSS: the Genomic Rearrangement IDentification Software Suite [github](https://github.com/PapenfussLab/gridss)
  - exSTRa: Expanded STR algorithm for Illumina sequencing data [github](https://github.com/bahlolab/exSTRa)
  - STRetch: Method for detecting STR expansions from short-read sequencing data [github](https://github.com/Oshlack/STRetch)
  - FARVAT: FARVAT: a family-based rare variant association test [link](http://healthstat.snu.ac.kr/software/farvat/)

12. Yingxin Lin, scMerge: Integration of multiple single-cell transcriptomics datasets leveraging stable expression and pseudo-replication
  - [github](https://github.com/SydneyBioX/scMerge)

13. Kevin Wang, RUV-Pro: Remove Unwanted Variation in prospective omics experiments

14. Regan Hayward, Epigenetic changes in Chlamydia-infected host cells
  - FAIRE-seq
  - consensus peaks

15. __KEYNOTE__ Eleni Giannoulatou Improving the genetic diagnosis of congenital heart disease
  - GATK vs Platypus
  - GATK:
      - logistic regression to model base error;
      - HMM to compute read likelihood;
      - naive Bayes classification to identify variants;
      - Gaussian mixture model with hand-crafted features capturing common error modes to filter false positive
  - Platypus:
      - generation of candidate variant;
      - local assembly and haplotype generation;
      - HMM to calculate read likelihood given haplotype;
      - population haplotype frequency fitted to a diploid segregation model;
      - variant are called by first calling haplotype then marginalisation over secondary variation
  - DeepVariant

16. David Humphreys, Ularcirc: Visualisation and enhanced analysis of circular RNAs via back and canonical forward splicing
  - all existing circRNA tools no visualization
  - Ularcirc [github](https://github.com/VCCRI/ularcirc)

17. Matthew Field, Comparison of predicted and actual consequences of missense mutations

18. Eleni-Maria Michanetzi, GidB: A Mutational Hotspot for Streptomycin Resistance in Tuberculosis

19. Ellis Patrick [![alt text][1.1]][9], Differential correlation across ranked samples for single-cell RNA-sequencing data
  - DCARS: [github](https://github.com/shazanfar/DCARS)




























[1.1]: http://i.imgur.com/tXSoThF.png (twitter icon with padding)
[2.1]: http://i.imgur.com/0o48UoR.png (github icon with padding)

[1]: http://www.twitter.com/_lazappi_
[2]: https://twitter.com/ctsa11
[3]: https://twitter.com/AThrimawithana
[4]: https://twitter.com/S_Foroutan
[5]: https://twitter.com/DoktrNick
[6]: https://twitter.com/ThomasBoudier1
[7]: https://twitter.com/talandrews
[8]: https://twitter.com/m_hemberg
[9]: https://twitter.com/TheEllisPatrick
