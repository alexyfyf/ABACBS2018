
## 10.27 ABACBS DAY1

1. __KEYNOTE__ Maitreya Dunham [![alt text][1.1]][2] Drivers of aneuploidy and adaptation in yeast
  - open question about CNVs: causative? which gene important? cost and benefit?
  - Cumulative model and discrete driver Model
  - piecewise constant model (1D fused LASSO) vs Linear model (regression)
  - Notes from LukeZappia [![alt text][1.1]][1] ![image](https://pbs.twimg.com/media/Ds9uNUkUwAUu_3f.jpg)

2. Stephen Bent, Mutation signatures in the mitochondria of moth specimens preserved for up to 100 years
  - Acient DNA
  - mutational signatures in mitochondria
    - C - deanimation C->T
    - G - oxidation G->T

3. Yi Jin Liew, Epigenetic adaptation of a coral to ocean acidification: non-standard genomics in a non-model organism
  - github rep [link](https://github.com/lyijin/working_with_dna_meth)
  - coral methylation often in gene body
  - use delta median as a measure of methylation
  - typical mammal methy analysis kit
    - methylKit (logistic regression)
    - methylSig (beta nominal likelihood ratio test)
    - methylumi limma (linear model)

4. __KEYNOTE__ Michael Stumpf [![alt text][1.1]][3] "Reconstructing Gene Regulatory Networks from Single Cell Data"
  - mechanistic model: parametric model (logistic network, stochastic process ...)
  - Graphical model: (Bayesian network, Gaussian graphical model, Gaussian Process)
  - Purely data driven: (relevance network, clustering, correlation network)
  - Hybrid
  - DREAM5 competition: pooling over the emsemble seems to give better result
  - regression (eg. Artiva) and Mutual information method (eg. ARACNE) generally better
  - correlation method generally worse
  - High MI means Z faithfully reproduces the state of input X
  - But not enough to capture network structure (need conditional or multivariate information measures)
  - Problem and plan
    - Make MI robust and avoid over dependence of estimator
      - Bayesian blocks and ML shrinkage estimator for entrophy
    - make calculation Fast
      - Julia
    - multivariate generalization of MI
      - Partial information Decomposition
    - statistically score
      - Empirical Bayesian approach
  - InformationMeasures [link](https://github.com/Tchanders/InformationMeasures.jl)
  - NetworkInference [link](https://github.com/Tchanders/NetworkInference.jl)
  - EmpiricalBayes [link](https://github.com/Tchanders/EmpiricalBayes.jl)
  - PIDC paper [link](https://www.cell.com/cell-systems/pdf/S2405-4712%2817%2930386-1.pdf)

5. Belinda Phipson [![alt text][1.1]][4] "Kidneys in a dish: examining the reproducibility of organoid differentiation using transcriptomics"
  - Organoids from the same differentiation are very highly correlated, so are those from different vials in the same batch
  - But there are big differences between batches
  - Batch to batch variability can be explained by relative maturity of organoids.
  -  The same is probably true for other kinds of organoids

6. Yu Wan, A network approach for detecting horizontal co-transfer of antimicrobial resistance genes in bacteria
  - GeneMates [github](https://github.com/wanyuac/GeneMates)

7. __KEYNOTE__ Kim-An Do, PRECISE: Personalized Cancer specific integrated network Estimation
  - shinyapp [link](https://mjha.shinyapps.io/PRECISE)
  - Publication [link](https://www.nature.com/articles/s41598-018-32682-x)

8. Alex Tokolyi [![alt text][1.1]][5], "Plasmid classification and investigation through network analysis of co-occurring genes"

9. Ralph Patrick Decoding the identity and flux of cardiac cells in injury and homeostasis at single-cell resolution
  - inter cellular communication network: receptor - ligand network
  - weight derived from logFC for receptor and ligand, PPI score for ligand:receptor interactions
  - DPA: differential proportion analysis

10. Stefano Mangiola, Allowing differential tissue composition analyses with ARMET
  - Cell proportion deconvolution method
  - use hiearchy pre built
  - ARMET

11. Luke Zappia [![alt text][1.1]][1] Visualising trees to choose clusters for scRNA-seq data
  - slide [link](https://speakerdeck.com/lazappi/visualising-trees-to-choose-clusters-for-scrna-seq-data)
  - clustree [github](https://github.com/lazappi/clustree)

12. __KEYNOTE__ Leming Shi Quality control and standardization of omics and bioinformatics for precision medicine
  - Notes from LukeZappia [![alt text][1.1]][1] ![image](https://pbs.twimg.com/media/Ds-xtLxV4AAApib.jpg)
  - Y = f(X), Y patient score, X omics

13. Rebecca Poulos [![alt text][1.1]][6], Associations between mutational signatures and driver mutations in cancer reveal pathways toward cancer pathogenesis
  - Sigfit to find mutational siganture [github](https://github.com/kgori/sigfit)

14. Richard Edwards [![alt text][1.1]][7], Pseudodiploid pseudo-long-read whole genome sequencing and assembly of Pseudonaja textilis (eastern brown snake) and Notechis scutatus (mainland tiger snake)

15. Woo Jun Shim [![alt text][1.1]][8], Cell identity genes are predicted by absence of broad H3K27me3 domains
  - TRIAGE (Transcriptional Regulatory Inference Analysis form Gene Expression)
  - Broad histone markers H2K27me3 asscosiated with cell-specific TFs
  - use histone marker width to normalize gene expression especially for TFs, which usually have low abundance
  - Use public histone ChIP-seq data and generate a model to adjust for TF gene expression

16. Taiyun Kim, Impact of similarity metrics on single-cell RNA-seq data clustering
  - Correlation based distance metrics lead to scRNA-seq clustering that better matches predefined labels
  - scClustBench [github](https://github.com/taiyunkim/scClustBench)
  - distance based metrics is susceptible to data scaling and normalization
  - correlation based (eg. pearson correlation) are robust

17. __KEYNOTE__ Ann Maree Patch Identifying intra-tumor heterogeneity and mechanisms of therapy resistance from cancer sample sequencing
  - BattenBerg assess subclonal copy number [github](https://github.com/Wedge-Oxford/battenberg)
  - Nature (2105) paper

18 Anna Trigos [![alt text][1.1]][9] Genomic drivers of the fragmentation of co-expression modules regulating multicellularity in cancer
  - PNAS paper [link](http://www.pnas.org/content/114/24/6406)

19. Joseph Cursons [![alt text][1.1]][10] Methylation-induced silencing of tumour suppressor genes in liver cancer
  - EpiCRISPR
  - minfi, missMethyl (+SWAN normalization)
  - limma (DMPs) and bumphunter (DMRs)
  - CRISPR gRNA design [link](https://crispr.ml)
  - Azimuth (for targeting score) and Elevation (for putative off-targets)

20. Vivian Yeung, Primary and Metastatic Tumour Evolution

21. Christoffer Flensburg [![alt text][1.1]][11], Calling Somatic Copy Number Alterations From RNA-Seq
  - CNA copy number alteration in RNA-seq
  - superFreq: exome, but modified for RNA-Seq [github](https://github.com/ChristofferFlensburg/superFreq)

22. Anna Quaglieri [![alt text][1.1]][12], Correcting unwanted variation in RNA sequencing data derived from a multi-centre study of leukemia
  - ruv::RUVIII
  - tumor content can be a hiden factor and is unwanted variation


[1.1]: http://i.imgur.com/tXSoThF.png (twitter icon with padding)
[2.1]: http://i.imgur.com/0o48UoR.png (github icon with padding)

[1]: http://www.twitter.com/_lazappi_
[2]: https://twitter.com/DunhamLab
[3]: https://twitter.com/theosysbio
[4]: https://twitter.com/BelindaPhipson
[5]: https://twitter.com/AlexTokolyi
[6]: https://twitter.com/rebecca_poulos
[7]: https://twitter.com/cabbagesofdoom
[8]: https://twitter.com/WooJunShim3
[9]: https://twitter.com/anna_t_g
[10]: https://twitter.com/JoeCursons
[11]: https://twitter.com/CFlensburg
[12]: https://twitter.com/annaquagli
