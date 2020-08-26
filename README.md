<p align="center"><img src="https://github.com/bdaisley/BEExact/blob/master/BEExact_logo.jpg" width="700"></p>

# BEExact: a taxonomic database tool and reference source for high-resolution inference of honey bee-associated microbial communities

## Description
BEExact is a comprehensive, non-redudant, reference database that has been thoroughly curated for use with 16S rRNA gene-based sequencing of the honey bee (<i>Apis mellifera</i>) microbiota. Recent reports have pronounced the need to move beyond the long time standard of phylotype-level characterization of the honey bee microbiota (Ellegaard and Engel, 2019; Nature Communications). BEExact addresses this concern by allow species-level resolution of all core microbiota members as well as a number of other symbionts, pathobionts, and a wide variety of environmetnal taxa that, albeit being present at low levels, are commonly found transiently associated with honey bees. 

## Benchmark
In the pending publication, BEExact is benchmarked at classifying ~90% honey bee-derived V4 amplicon sequence variants (ASVs) at the species-level, which represents an approximate 6-fold improvement in comparison to the commonly used SILVA v138 database which classifies only ~14% of ASVs at the same level. 


## Available  databases for download:

<b>BEExact full length database</b>
1. <i>BEEx-FL-refs</i> (the complete database containing near full length references for all known honey bee-specific 16S rRNA gene sequences)

<b>Ready to use pre-trained/formatted V4 region-specific classifiers</b>

2. <i>IDTAXA-BEEx-V4-TS</i> (V4 classifier for IDTAXA) <- recommended, lowest optimal error rates during benchmarking
3. <i>DADA2-BEEx-V4-TS</i> (V4 classifier for DADA2)
4. <i>QIIME2-BEEx-V4-TS</i> (V4 classifier for QIIME2)


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
    --p-trunc-len 120 \
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
