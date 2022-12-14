### Protein language model rescue mutations highlight variant effects and structure in clinically relevant genes

This repo contains the scripts and metadata used in our work presented at NeurIPS 2022 Learning Meaningful Representation of Life (LMRL) workshop.

[Workshop website](https://www.lmrl.org/) | [Paper](https://arxiv.org/abs/2211.10000) 

**Abstract:** Despite being self-supervised, protein language models have shown remarkable performance in fundamental biological tasks such as predicting impact of genetic variation on protein structure and function. The effectiveness of these models on diverse set of tasks suggests that they learn meaningful representation of fitness landscape that can be useful for downstream clinical applications. Here, we interrogate the use of these language models in characterizing known pathogenic mutations in curated, medically actionable genes through an exhaustive search of putative compensatory mutations on each variant's genetic background. Systematic analysis of the predicted effects of these compensatory mutations reveal unappreciated structural features of proteins that are missed by other structure predictors like AlphaFold. While deep mutational scan experiments provide an unbiased estimate of the mutational landscape, we encourage the community to generate and curate rescue mutation experiments to inform the design of more sophisticated co-masking strategies and leverage large language models more effectively for downstream clinical prediction tasks. 

### Pretrained models

| Model                                                      |    Number of layers | Number of parameters   |    Training dataset    | Implementation in our work |
| ----------------------------------------------------------------------------------------------------- | :------------------: | :------------------: | :------------------: |:------------------: |
| [ESM-2](https://github.com/facebookresearch/esm#available-models)  | 33 | 650M | UR50/D | Single model with `wt-marginals` scoring strategy |
| [ESM-1v](https://github.com/facebookresearch/esm#available-models) | 33 | 650M | UR90/S | Ensemble of 5 models with the same scoring strategy as ESM-2 |
| [ESMFold](https://github.com/facebookresearch/esm#available-models)  | 48 | 690M | PDB + UR50 | Structure prediction for _BAG3_ |
| [AlphaFold2](https://www.alphafold.ebi.ac.uk/)  |  |  | | AlphaFold2 structural model prediction for _BAG3_ |
| [Cross-protein transfer](https://github.com/songlab-cal/CPT)  |  |  | | Zero-shot prediction scores for all 53 ACMG genes except _MAX_ and _HNF1A_ |


### Data on gene list and sequence variation

| Description                                                      |    Data source | 
| ----------------------------------------------------------------------------------------------------- | :------------------: | 
| List of clinically actionable genes  | [ACMG v3.1](https://www.gimjournal.org/article/S1098-3600(21)05076-0/fulltext#secst0025) |
| Allele frequency | [gnomAD v2 GRCh38 liftover](https://gnomad.broadinstitute.org/downloads#exac-variants) |
| ClinVar annotations | [Accessed on 09/17/2022](https://ftp.ncbi.nlm.nih.gov/pub/clinvar/vcf_GRCh38/) | 
| Multiple sequence alignments | [UCSC multiz-100 way CDS alignment](https://hgdownload.soe.ucsc.edu/goldenPath/hg38/multiz100way/alignments/) ([Placental mammals](https://hgdownload.soe.ucsc.edu/goldenPath/hg38/phyloP100way/)) | 


## Citation

If you find this work useful, please cite it as follows:

```bibtex
@misc{https://doi.org/10.48550/arxiv.2211.10000,
  doi = {10.48550/ARXIV.2211.10000},
  
  url = {https://arxiv.org/abs/2211.10000},
  
  author = {Soylemez, Onuralp and Cordero, Pablo},
  
  keywords = {Machine Learning (cs.LG), Genomics (q-bio.GN), FOS: Computer and information sciences, FOS: Computer and information sciences, FOS: Biological sciences, FOS: Biological sciences},
  
  title = {Protein language model rescue mutations highlight variant effects and structure in clinically relevant genes},
  
  publisher = {arXiv},
  
  year = {2022},
  
  copyright = {Creative Commons Attribution 4.0 International}
}

```

## Feedback

If you have any questions or comments, or would like to collaborate, please feel free to reach out. 
