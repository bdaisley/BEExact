<p align="center"><img src="https://github.com/bdaisley/BEExact/blob/master/BEExact_logo.jpg" width="700"></p>

# BEExact: a metataxonomic database tool for high-resolution inference of bee-associated microbial communities

Original article in mSystems here: https://msystems.asm.org/content/6/2/e00082-21 <br />


## Update (30-January-2023)

BEExact v2023.01.30 is here! There have been many formal descriptions of novel bee-associated bacterial species come out since the last release, and excitingly, some of them have turned out to be exact matches to the predicted species previously designated with 'bxid' placeholder names. For example, Lacticaseibacillus sbxid5696 (old:BX004169) has been replaced by Lacticaseibacillus zhaodongensis (new:BX006585) and Frischella sbxid5676 (old:BX004348) has been replaced by Frischella japonica (new:BX006595). See *here* for the full list of changes.

Furthermore, additional pre-trained/pre-formatted classifiers are now available for [mothur](https://mothur.org), [LotuS2](https://lotus2.earlham.ac.uk), and [KRAKEN2](https://ccb.jhu.edu/software/kraken2) software.

## Quick links for available download files:
<div align="left">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | <sub>IDTAXA  </sub>             | <sub> DADA2 [RDP]</sub>          |  <sub> QIIME2 [NB] </sub>   | <sub> SINTAX </sub> | <sub> MOTHUR </sub>  | <sub> LOTUS2</sub>  | <sub> KRAKEN2</sub> 
:------------------------------------------|:--------------------:|:--------------------:|:-----------------------:|:----:|:----:|:----:|:----:
Bakt_341F `5'-CCTACGGGNGGCWGCAG-3'`</br>Bakt_805R `5'-GACTACHVGGGTATCTAATCC-3'`</br>    | [V3V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/idtaxa/BEEx_v2023.01.30___idtaxa_v3v4.RData)   | [V3V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/dada2/BEEx_v2023.01.30___dada2_v3v4.fasta.gz)  | [V3V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/qiime2/BEEx_v2023.01.30___qiime2_naive-bayes-classifier_v3v4.qza) | [V3V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/sintax/BEEx_v2023.01.30___sintax_v3v4.udb.gz) | [V3V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/mothur/v3v4.tar.gz) | [V3V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/lotus2/v3v4.tar.gz)  |  [V3V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/kraken2/BEEx_v2023.01.30___kraken2_v3v4.tar.gz)<tr></tr>
515F(Parada) `5'-GTGYCAGCMGCCGCGGTAA-3'`</br>806R(Apprill) `5'-GGACTACNVGGGTWTCTAAT-3'` | [V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/idtaxa/BEEx_v2023.01.30___idtaxa_v4.RData)| [V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/dada2/BEEx_v2023.01.30___dada2_v4.fasta.gz) | [V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/qiime2/BEEx_v2023.01.30___qiime2_naive-bayes-classifier_v4.qza)   | [V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/sintax/BEEx_v2023.01.30___sintax_v4.udb.gz)   | [V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/mothur/v4.tar.gz)   | [V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/lotus2/v4.tar.gz)    | [V4](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/kraken2/BEEx_v2023.01.30___kraken2_v4.tar.gz)<tr></tr> 
515F(Parada) `5'-GTGYCAGCMGCCGCGGTAA-3'`</br>926R(Quince) `5'-CCGYCAATTYMTTTRAGTTT-3'`  | [V4V5](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/idtaxa/BEEx_v2023.01.30___idtaxa_v4v5.RData)| [V4V5](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/dada2/BEEx_v2023.01.30___dada2_v4v5.fasta.gz) | [V4V5](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/qiime2/BEEx_v2023.01.30___qiime2_naive-bayes-classifier_v4v5.qza) | [V4V5](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/sintax/BEEx_v2023.01.30___sintax_v4v5.udb.gz) | [V4V5](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/mothur/v4v5.tar.gz) | [V4V5](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/lotus2/v4v5.tar.gz)  |  [V4V5](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/kraken2/BEEx_v2023.01.30___kraken2_v4v5.tar.gz)<tr></tr>  
799F-mod3 `5'-CMGGATTAGATACCCKGG-3'`</br>1115R(Kembel) `5'-AGGGTTGCGCTCGTTG-3'` | [V5V6](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/idtaxa/BEEx_v2023.01.30___idtaxa_v5v6.RData)   | [V5V6](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/dada2/BEEx_v2023.01.30___dada2_v5v6.fasta.gz)  | [V5V6](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/qiime2/BEEx_v2023.01.30___qiime2_naive-bayes-classifier_v5v6.qza) | [V5V6](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/sintax/BEEx_v2023.01.30___sintax_v5v6.udb.gz) | [V5V6](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/mothur/v5v6.tar.gz) | [V5V6](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/lotus2/v5v6.tar.gz) |  [V5V6](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/kraken2/BEEx_v2023.01.30___kraken2_v5v6.tar.gz)<tr></tr>  
Full-length 16S rRNA ref sequences  | [FL](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/idtaxa/BEEx_v2023.01.30___idtaxa_FL.RData) | [FL](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/dada2/BEEx_v2023.01.30___dada2_FL.fasta.gz) | [FL](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/qiime2/BEEx_v2023.01.30___qiime2_naive-bayes-classifier_FL.qza)   | [FL](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/sintax/BEEx_v2023.01.30___sintax_FL.udb.gz)   | [FL](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/mothur/full_length.tar.gz)   | [FL](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/lotus2/full_length.tar.gz)    | [FL](https://github.com/bdaisley/BEExact/raw/master/pre-formatted_classifier_downloads/kraken2/BEEx_v2023.01.30___kraken2_FL.tar.gz)

</div>

## Description

BEExact is a comprehensive, non-redudant, reference database that has been thoroughly curated for use with 16S rRNA gene-based sequencing on bee-associated microbial communities. 

The database will be updated frequently to incoporate annotations and reference sequences for novel bee host-associated taxa. All suggestions for improvement are welcomed, see contact info below. A wiki tutorial is also currently in the works and will cover microbiota analysis using exact ASVs as opposed to the traditional OTU-based methods. As a quick note, there are several advantages to using ASVs specifically relating to their precision in characterizing microbial communities as well as their consistency for cross-study compatibility. See the latest [DADA2 pipeline](https://benjjneb.github.io/dada2/tutorial.html) for more details on this. 

Also, an excellent article simplifying the workflow for valid statistical analysis on compositional datasets: [Microbiome Datasets Are Compositional: And This Is Not Optional](https://www.frontiersin.org/articles/10.3389/fmicb.2017.02224/full)


## Benchmark
Across 32 indepedent studies encompassing 50 bee species, BEExact is enabled classification of ~80-90% of ASVs at the species-level whereas the leading exisiting database classified no more than ~30% at the same level. We noted that microbial communities from eusocial bee species generally exhibited higher classification rates, likely owing to the fact that their microbiota has been more intensively characterized compared to many solitary bee species.


## Example of how to create your own region-specific training set
Other variable region-specific training sets can be generated using the [BEExact full database sequences](https://github.com/bdaisley/BEExact/raw/master/full_database/full_database.tar.gz).

An example using QIIME2 tools for making a V3-V4 specific training set:

Steps 1: Import sequence and taxonomy files as .qza 
```
  qiime tools import \
    --type 'FeatureData[Sequence]' \
    --input-path BEEx-FL-refs_sequences.fa \
    --output-path BEEx-FL-refs_sequences.qza

  qiime tools import \
    --type 'FeatureData[Taxonomy]' \
    --input-format HeaderlessTSVTaxonomyFormat \
    --input-path BEEx-FL-refs_taxonomy.txt \
    --output-path BEEx-FL-refs_taxonomy.qza
```

Steps 2: Trim to specific region of interest (V3-V4 in this case)

```
qiime feature-classifier extract-reads \
    --i-sequences BEEx-FL-refs_sequences.qza \
    --p-f-primer ACTCCTACGGGAGGCAGCAG \
    --p-r-primer GGACTACHVGGGTWTCTAAT \
    --p-min-length 100 \
    --p-max-length 400 \
    --o-reads BEEx-V3V4-refs_sequences.qza
```

Steps 3: Train the classifier
```
  qiime feature-classifier fit-classifier-naive-bayes \
    --i-reference-reads BEEx-V3V4-refs_sequences.qza \
    --i-reference-taxonomy BEEx-FL-refs_taxonomy.qza \
    --o-classifier QIIME2_BxV3V4TS.qza
```

Step 4: Classify reads with the q2-feature-classifier
```
    qiime feature-classifier classify-sklearn \
      --i-classifier QIIME2_BxV3V4TS.qza \
      --i-reads ASVs_query_sequences.qza \
      --p-confidence 0.5 \
      --o-classification QIIME2_BxV3V4TS_ASVs_out.qza
```


Step 5: Visualize files
```
    qiime metadata tabulate \
      --m-input-file QIIME2_BxV3V4TS_ASVs_out.qza \
      --o-visualization QIIME2_BxV3V4TS_ASVs_out.qzv
```

For user-friendly conversion, drag and drop "<i>QIIME2_BxV3V4TS_ASVs_out.qzv</i>" to https://view.qiime2.org


## Reference details

If you find the database helpful, please cite the following: 



Daisley B.A. and G. Reid (2020). BEExact: a metataxonomic database tool for high-resolution inference of bee-associated microbial communities. <i>mSystems</i> 6(2):e00082-21 

https://doi.org/10.1128/mSystems.00082-21


## Contact information

All feedback welcomed. If you have any questions, please feel free to contact me. Sharing of information is also encouraged, especially for novel bee-associated species that have recently been discovered but not yet incorporated into the BEExact database. Teamwork makes the dreamwork.

Email:          bdaisley@uwo.ca

Twitter:        @bdaisley
