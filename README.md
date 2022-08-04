
![logo1-removebg-preview](https://user-images.githubusercontent.com/52098813/182604827-df4fcc3a-185c-4c8c-9638-6a80a71c05fb.png)

# BUSCOGO: A BUSCO Specific GO Term Enrichment Analysis Tool

BUSCO (https://busco.ezlab.org/) is a widely used tool in genomics. BUSCO is built around searching for “universal single-copy orthologues” in a genome, transcriptome or proteome. These are genes that should be present in >90% species (“universal”) in the relevant taxonomic group and present only once in >90% species (“single copy”). This allows the user to identify the same gene (“orthologues”) in multiple genomes, which can then be used for downstream analysis, such as phylogenomics. The total recall of BUSCO genes can also be used to assess genome assembly completeness. (The “B” is for “benchmarking”.)

However, sometimes BUSCO genes do not behave as expected - they are either Duplicated or Missing from otherwise high-quality genomes. It can be biologically useful to know whether such deviations appear to be non-random.


The purpose of this tool is to explore such special cases where the deviations are non-random. BUSCOGO achieves this through the use of Gene Ontology and an Enrichment Analysis Test to calculate stastically signfiicant enriched gene ontology terms of BUSCO genes of interest. 


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

### How To Access BUSCOGO

### BUSCOGO Shiny App: Usage and Features

### BUSCOGO Command Line Tool: Usage and Features

### BUSCOGO Result Interpretation

### Vignette: A Scenario Based Tutorial

Vignette 1: Missing BUSCO Analysis

https://github.com/Awadewa/BUSCOGO/blob/main/Vignette%201:%20Missing%20BUSCO%20Analysis/Vignette_One.md

Vignette 2: Duplicated BUSCO in multiple species Analysis

https://github.com/Awadewa/BUSCOGO/blob/main/Vignette%202:%20Duplicated%20BUSCO%20in%20multiple%20species%20Analysis/Vignette_Two.md

Vignette 3: BUSCO genes of a specific sequence or location Analysis

https://github.com/Awadewa/BUSCOGO/blob/main/Vignette%203:%20BUSCO%20genes%20of%20a%20specific%20sequence%20or%20location%20Analysis/Vignette_Three.md

# Accessing BUSCOGO

BUSCOGO can be access using two diffenret user interface: a Shiny Web App or a Command Line Tool



## BUSCOGO Shiny Web App

BUSCOGO can be access through a Shiny Web interface through the following link

www.BUSCOGO.Shiny (Add actual link once deployed on server)



## BUSCOGO Command Line Tool

BUSCOGO can also be accessed through the use of an R-studio Terminal (Or regular terminal, if Rtusdio directory is configured)

Steps:
1. User downloads the BUSCOGO Rscript Directory from Github
2. User open BUSCOGO.R on Rstudio
3. Using Rstudio Terminal, user can enter the following command to run BUSCOGO
```
Rscript BUSCOGO.R --input input_file_name [options]
```

An in depth guide of the BUSCOGO Command Line tool is given below.
  
# What You Need To Get Started

BUSCOGO takes in an input in the format of a BUSCO Full Table.

BUSCO Full Table is the result output of the BUSCO Quality Control tool.

Workflow:
``` 
Nucleotide Fasta File    >>>   BUSCO QC Tool  >>>   BUSCO_Full_Table   >>>   BUSCOGO
``` 

BUSCO Full Table:
![image](https://user-images.githubusercontent.com/52098813/182605083-6d6e3a5c-eb9f-47a8-8213-310d9dfefefd.png)

# BUSCOGO Shiny Web-App: Features and Usage

## Upload FIle
User can upload  one or multiple BUSCO Full Table file using the "Browse File" button on the top left side of the screen. 

![image](https://user-images.githubusercontent.com/52098813/182605660-030dba18-3c8f-42ca-9c40-8e90e738b0dc.png)


## BUSCO Gene of Interest Table

Once Uploaded, all content from the input BUSCO Table will be displayed in the Gene of Interest Table. All Genes within the gene of interest table will be the list of genes being compared to the background during enrichment analysis tests.

![image](https://user-images.githubusercontent.com/52098813/182605422-aa27eb3a-f5a8-47f8-b761-b72f2bec6447.png)



## BUSCO Input Statistics 

In additation to the Gene Of interest Table, BUSCOGO will provide user with a statistcal output of the Gene of Interest that shows the number of Missing, Complete, Fragmented, Duplicated and Total genes of the input BUSCO Table.

![image](https://user-images.githubusercontent.com/52098813/182605459-031c1d47-cb46-40de-8ae1-60627f7336cc.png)

## BUSCO Gene of Interest Filter

User can select their desired subset of Gene list of interest through the use of the Gene of Interest Filter.

![image](https://user-images.githubusercontent.com/52098813/182605521-49aa4b83-9707-4fec-a739-2d14da8d6eaa.png)

### BUSCO Status Filter

Selects Genes of the respective status; Missing, Complete, Fragmented and Duplicated. Multiple status can be selected at once in combination.

### BUSCO Genome Range

When a input BUSCO Table is uploaded, BUSCOGO automatically updates the available genome range (coordiantes) of the input file for the user to select.

### BUSCO Specific Sequence/Scaffold

When a input BUSCO Table is uploaded, BUSCOGO automatically updates the available sequence/scaffold of the input file for the user to select.


### BUSCO Specific Strand

Allows user to only select BUSCO genes on the Sense (+) or Antisense (=) Strand



## BUSCO Custom Background

By default, all genes in the input BUSCO table is used as the Background Gene Universe within the Enrichment Analysis Test

However, BUSCOGO allows user to select the custom background option to specify custom set of genes to be included in the Background.
The selection process of the custom background follows the same method of selection of gene list of interest.

![image](https://user-images.githubusercontent.com/52098813/182605783-6df48bae-00a2-499f-ab4c-51bd6739c306.png)


### Once you are happy with the "Gene List of Interest" and/or "Background Genes" press the start analysis Button.




# Command Line Tool

BUSCOGO can also be access through a terminal, by opening the BUSCOGO Rscript in Rstudio.

## List of Available Option

User can see all available option using the command:
```
Rscript BUSCOGO.R --help
```
![image](https://user-images.githubusercontent.com/52098813/182609225-998573c9-1f7a-491f-9fa9-d167962bf146.png)



# BUSCOGO Enrichment Analysis

BUSCOGO utilizes the enrichment analysis package topGO, the details of which are published by Alexa et al (2006). topGO requires a set of genes of interest, a set of background or population genes that contain the gene set of interest (for example all BUSCO genes for the relevant taxonomic clade) and the gene ontology annotations for the background set of genes. BUSCOGO generates these gene sets based on the input provided by the user, and uses the gene ontology annotations provided by the OrthoDB (Zdobnov et al 2021) to build the background annotation. topGO then performs statistical analysis to determine if genes of interest are more often associated with certain biological functions than what would be expected in the background set of genes. You can use these results to determine if a set of BUSCO genes of interest is 'enriched’ for certain biological functions. 

### The Different Algorithms of topGO

The results of GO enrichment analysis are dependent on the treatment of the GO hierarchy. topGO provides several different algorithms that treat this hierarchy differently. BUSCOGO generates results using these different algorithms and they include;

### Classic: 
Classic does not take into account the hierarchy of GO, and tests each term independent of one another. 

### Weight: 
Weight algorithm compares the significance of the child and parent nodes in the GO hierarchy and includes the more significant. 

### Elim: 
Elim algorithm begins at the bottom (or least general) GO term, and if the term is significant below a certain cutoff, will discard all genes annotated with more general terms.  

### Weight01: 
A mixture between the Weight and Elim algorithms. 

### Parent Child: 
The parent child algorithm utilizes the parent terms of the GO terms.  

topGO also offers several different statistical tests to generate enrichment analysis results, and BUSCOGO uses the Fisher statistic. More information can be found in the topGO publication by Alexa et al (2006). The hierarchy itself is provided for enrichment analysis by topGO, which uses the GO.db package. 



# Result Interpretation 

BUSCOGO generates numerous different format of result. The segment below discuss each format in detail.

## The Three Gene Ontology Groups

BUSCOGO Generates result for each of the three main Gene Ontology Categories: Biolgogical Process, Molecular Function and Celullar Component. 

# Enriched GO Terms Results

## GO Term Enrichment Ranking
The GO Term Ranking Table is a table containing all of the GO terms annotated to genes within a set of genes list of interest and ranked by the different enrichment analysis algorithm. Each column contains the 

GO ID: GO Term ID
Description: A short descriptor of the GO term
Annotated: The number of genes annotated with the GO Term
Significant: The number of genes within the gene list of interest annotated with the GO Term.
Expected: The expected number of genes, anode of size "Annotated", if significant genes are randomly selected. 
Rank in Elim: 
Classic: P-value for Classic Algorithm 
Elim: P-value for Elim Algorithm
Weight: P-value for Weight Algorithm
Weight01: P-value for Weight01 Algorithm
Parentchild: P-value for Parentchild Algorithm

![image](https://user-images.githubusercontent.com/52098813/182606745-b9ae80af-df5d-4b17-bda3-9bb4c97033f6.png)

## Enrichment Score Ranking Plot 
This plot contains the gene ontology terms that have ‘Weight01’  p values of less than 0.05, and can therefore be inferred as significantly enrichmented terms. These GO terms are plotted against the ‘Enrichment Score”. The enrichment Score is the negative log 10 scale of their p- values. 

![image](https://user-images.githubusercontent.com/52098813/182606784-1aa77b64-89bd-497c-8875-064fc15f26d2.png)

## Enriched Gene Count Ranking Plot
This plot contains the gene ontology terms that have ‘Weight01’ p values of less than 0.05, and can therefore be inferred as significantly enrichmented terms. plot mas these GO Terms on the x axis, and on the y axis, it plots the corresponding gene counts, or how many genes were annotated with each GO term. The bars a coloured by the corresponding p-value of the GO Term, with red indicating a smaller p -value, and blue indicating larger. 

![image](https://user-images.githubusercontent.com/52098813/182606843-2dfe51c1-20c0-48ac-b6f8-057afcc445c1.png)

## Updated BUSCO Table

The updated BUSCO Table is a summarized result format which is in the same format as the input BUSCO tabel, hower it now contains two new columns, one being all the go terms annotated to the BUSCO gene, and the other column showing which GO term is enrichment above out cutoff of 0.05. 

![image](https://user-images.githubusercontent.com/52098813/182606923-df09dbc4-21c9-42f7-983d-2af2931b946d.png)

## Gene Ontology Heirachy Map
The GO hierarchy map shows the interaction of the gene ontology terms that have ‘Weight01’ p values of less than 0.05. These terms are shown as rectangles. The upper graph is the GO hierarchy generated by these significant terms, and demonstrates how the significant GO terms are distributed in the GO hierarchy. 

![save (4)](https://user-images.githubusercontent.com/52098813/182607040-63c625a5-308d-408f-abaf-391ed98aff90.png)

# Gene Ontology Term Explorer
![image](https://user-images.githubusercontent.com/52098813/182607263-504120e5-019c-4c9d-afaa-0ba70a8f88a4.png)

## Gene Ontology Term Description 
Uses the Gene Ontology API, to pull information regarding the specific go identifier’s description, definition, synonym. 

![image](https://user-images.githubusercontent.com/52098813/182607514-88f16aaa-620e-4ca3-bef6-914e133c0860.png)

## GO Term Reverse Annotation Table

The reverse gene ontology table contains all the genes present in the gene set of interest, and all of the GO terms annotated to the respective term. 

![image](https://user-images.githubusercontent.com/52098813/182607600-9fc61063-7968-4006-8940-c0e8d9cc115c.png)


