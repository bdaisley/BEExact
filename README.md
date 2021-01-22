<p align="center"><img src="https://github.com/bdaisley/BEExact/blob/master/BEExact_logo.jpg" width="700"></p>

# BEExact: a metataxonomic database tool for high-resolution inference of bee-associated microbial communities

## Update 

BEExact v1.0.2 is here! A lot of major improvements have been made to the database following the first set of revisions. Namely, it is no longer restricted for use to only <i>Apis mellifera</i>. It has now been expanded for use with all bee species (Hymenoptera:Apoidea:Anthophila). To do so, we not only added a long list of host-associated 16S rRNA gene sequences annotated at their lowest common rank (LCR) based on authorative type strains, but we also developed a novel approach for assigning phylogenetically consistent placeholder names to uncultivated microbial dark-matter. In effect, 618 placeholder labels were generated which should greatly enhances the ability to analyze associated microbial community structure and draw meaningful conclusions from routine 16S rRNA gene sequencing endeavours. 

More to come soon!


## Description

BEExact is a comprehensive, non-redudant, reference database that has been thoroughly curated for use with 16S rRNA gene-based sequencing on bee-associated microbial communities. 

The database will be updated frequently to incoporate annotations and reference sequences for novel bee host-associated taxa. All suggestions for improvement are welcomed, see contact info below. If there is enough interest, I will write up a wiki tutorial for microbiota analysis using exact ASVs as opposed to the traditional OTU-based methods. As a quick note, there are several advantages to using ASVs specifically relating to their precision in characterizing microbial communities as well as their consistency for cross-study compatibility. See the latest [DADA2 pipeline](https://benjjneb.github.io/dada2/tutorial.html) for more details on this. Also, an excellent article simplifying the workflow for valid statistical analysis on compositional datasets: [Microbiome Datasets Are Compositional: And This Is Not Optional](https://www.frontiersin.org/articles/10.3389/fmicb.2017.02224/full)


## Benchmark
In the pending publication, BEExact is benchmarked at classifying ~80-90% of ASVs at the species-level across 32 indepedent studies encompassing 50 bee species, whereas the leading existing databases enable classification of no more than ~30% for more bee types. Microbial communities from eusocial bee species generally have better classification rates because their microbiota has been more intensively characterized compared to many solitary species.

## Available  files for download:

The updated database for all variable regions will be avaiable shortly.


<b>BEExact full length database</b>
1. [BEEx-FL-refs](https://github.com/bdaisley/BEExact/blob/master/Datasets/BEEx-FL-refs.zip) (the complete database of all expected honey bee-specific 16S rRNA gene sequences)

<b>Ready to use pre-trained/formatted region-specific classifiers (coming shortly)</b>


## Creating your own region-specific training set
Other variable region-specific training sets can be generated using the full length BEExact database (<i>BEEx-FL-refs</i>)

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

<b>BEExact </b>
Paper currently under peer review, when published the reference details will be provided here.

"Daisley B.A. and Reid G. BEExact: a taxonomic database tool and reference source for high-resolution inference of honey bee-associated microbial communities. (2020)


## Contact information

All feedback welcomed. If you have any questions, please feel free to contact me. Sharing of information is also encouraged, especially for novel honey bee-associated species that have recently been discovered but not yet incorporated into the BEExact database. Teamwork makes the dreamwork.

Email:          bdaisley@uwo.ca

Twitter:        @bdaisley
