
![logo1-removebg-preview](https://user-images.githubusercontent.com/52098813/182604827-df4fcc3a-185c-4c8c-9638-6a80a71c05fb.png)

# BUSCOGO: A BUSCO Specific GO Term Enrichment Analysis Tool

BUSCO (https://busco.ezlab.org/) is a widely used tool in genomics. BUSCO is built around searching for “universal single-copy orthologues” in a genome, transcriptome or proteome. These are genes that should be present in >90% species (“universal”) in the relevant taxonomic group and present only once in >90% species (“single copy”). This allows the user to identify the same gene (“orthologues”) in multiple genomes, which can then be used for downstream analysis, such as phylogenomics. The total recall of BUSCO genes can also be used to assess genome assembly completeness. (The “B” is for “benchmarking”.)

However, sometimes BUSCO genes do not behave as expected - they are either Duplicated or Missing from otherwise high-quality genomes. It can be biologically useful to know whether such deviations appear to be non-random.


The purpose of this tool is to explore such special cases where the deviations are non-random. BUSCOGO achieves this through the use of Gene Ontology and an Enrichment Analysis Test to calculate stastically signfiicant enriched gene ontology terms of BUSCO genes of interest. 


# The Concept of a "Benchmarking Universal Single Copy Ortholog (BUSCO)"

The BUSCO sets are collections of nearly universally distributed (90%) single-copy orthologous genes found within species at a specific phylogenetic level. Originally these sets represented arthropods, vertebrates, metazoans, fungi, and eukaryotes, but additional genome sequences have made it possible to create BUSCO sets at a finer scale.

These sets are determined by analysis of species in the OrthoDB database. The theory is that genes belonging to these sets are evolving under “single-copy control” where something about their necessity and dosage constraints maintains them at a single copy within the genome.

If a newly assembled genome or transcriptome is missing genes from the corresponding BUSCO set, something may have gone wrong with sequencing/assembly/annotation/etc, and other genes may also be missing.


# The Four BUSCO Status

BUSCO attempts to provide a quantitative assessment of the completeness in terms of expected gene content of a genome assembly, transcriptome, or annotated gene set. The results are simplified into categories of Complete and single-copy, Complete and duplicated, Fragmented, or Missing BUSCOs.

### Complete

If found to be complete, the BUSCO matches have scored within the expected range of scores, matches a single-copy, and within the expected range of length alignments to the BUSCO profile.

### Duplicated

If found to be duplicated, the BUSCO matches have scored within the expected range of scores, matches a multiple copies, and within the expected range of length alignments to the BUSCO profile.

### Fragmented

If found to be fragmented, the BUSCO matches have scored within the range of scores but not within the range of length alignments to the BUSCO profile.

### Missing

If found to be missing, there were either no significant matches at all, or the BUSCO matches scored below the range of scores for the BUSCO profile.



# What is in this User Guide


# Accessing BUSCOGO

# What You Need To Get Started
![image](https://user-images.githubusercontent.com/52098813/182605083-6d6e3a5c-eb9f-47a8-8213-310d9dfefefd.png)

# Shiny Web-App
# Features 

## Upload FIle
![image](https://user-images.githubusercontent.com/52098813/182605660-030dba18-3c8f-42ca-9c40-8e90e738b0dc.png)



## BUSCO Gene of Interest Table
![image](https://user-images.githubusercontent.com/52098813/182605422-aa27eb3a-f5a8-47f8-b761-b72f2bec6447.png)



## BUSCO Input Statistics 

![image](https://user-images.githubusercontent.com/52098813/182605459-031c1d47-cb46-40de-8ae1-60627f7336cc.png)

## BUSCO Gene of Interest Filter
![image](https://user-images.githubusercontent.com/52098813/182605521-49aa4b83-9707-4fec-a739-2d14da8d6eaa.png)

## BUSCO Custom Background
![image](https://user-images.githubusercontent.com/52098813/182605783-6df48bae-00a2-499f-ab4c-51bd6739c306.png)


### Start Analysis


Explanation of result is given here: link



# Command Line Tool

## List of Available Option
```
Rscript BUSCOGO.R --help
```
![image](https://user-images.githubusercontent.com/52098813/182609225-998573c9-1f7a-491f-9fa9-d167962bf146.png)

## 
```
Rscript BUSCOGO.R --input busco_table_file --missing --duplicated
```

# Result Interpretation 

## The Three Gene Ontology Groups

# Enriched GO Terms Results

## GO Term Enrichment Ranking
![image](https://user-images.githubusercontent.com/52098813/182606745-b9ae80af-df5d-4b17-bda3-9bb4c97033f6.png)

## Enrichment Score Ranking Plot 
![image](https://user-images.githubusercontent.com/52098813/182606784-1aa77b64-89bd-497c-8875-064fc15f26d2.png)

## Enriched Gene Count Ranking Plot
![image](https://user-images.githubusercontent.com/52098813/182606843-2dfe51c1-20c0-48ac-b6f8-057afcc445c1.png)

## Updated BUSCO Table
![image](https://user-images.githubusercontent.com/52098813/182606923-df09dbc4-21c9-42f7-983d-2af2931b946d.png)

## Gene Ontology Heirachy Map

![save (4)](https://user-images.githubusercontent.com/52098813/182607040-63c625a5-308d-408f-abaf-391ed98aff90.png)

# Gene Ontology Term Explorer
![image](https://user-images.githubusercontent.com/52098813/182607263-504120e5-019c-4c9d-afaa-0ba70a8f88a4.png)

## Gene Ontology Term Description 
![image](https://user-images.githubusercontent.com/52098813/182607514-88f16aaa-620e-4ca3-bef6-914e133c0860.png)

## GO Term Reverse Annotation Table
![image](https://user-images.githubusercontent.com/52098813/182607600-9fc61063-7968-4006-8940-c0e8d9cc115c.png)

## GO Term Distribution
![image](https://user-images.githubusercontent.com/52098813/182607682-e57bdf2d-ca3c-4d82-b46f-4eb9a6e9894b.png)


