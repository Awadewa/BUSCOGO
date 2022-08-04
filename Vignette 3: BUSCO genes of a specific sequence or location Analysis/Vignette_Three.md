# Using BUSCOGO To Study BUSCO Genes of from a Specific Sequence/Location and Using A Custom Background. 

In this example, we will be utilizing BUSCOGO to find the Enriched GO Term that corresponds to BUSCO genes that exist on a specific sequence/location within the genome.

We will also be utilzing BUSCOGO's custom background option to filter out any genes that are classified as "Missing" from the background enrichment.

## 1. Input Data

We will be working with the BUSCO Table of a mite genome processed through BUSCO using the Arachnid lineage. The BUSCO Table used as input for this example can be found above. 

User can upload the BUSCO table into BUSCOGO through the "Upload File" button on the top left of the screen.

![image](https://user-images.githubusercontent.com/52098813/182611518-29c16dfd-003b-4e38-b81a-85a932bdf07c.png)

## 2. Selecting our "Gene Of Interest"

### Viewing Our Input BUSCO Table Content

Once a BUSCO Table is uploaded, user can view the corresponding gene content of the BUSCO table. Below the "Gene of Interest" table we can see the statistics of the input BUSCO Table in our "Gene of Interest Stats".

From it, we can see that our input contains 30003 total BUSCO genes, which 1929 of them is classifed as "Complete", 898 of them are classifed as "Missing", 131 of them are classified as "Duplicated" and 45 of them are classified as "Fragmented".

![image](https://user-images.githubusercontent.com/52098813/182619595-62f50b98-b37e-4cd7-862a-6f717f875655.png)

### Filtering Our "Gene of Interest"

For this example, we are only interested in observing BUSCO genes that are exist on the specifc sequence of "WNKI10000001.1" and within the genomic coordinate of ~3,000,000 and ~10,000,000 in our input BUSCO Table. 

Therefore, we will utilize the "Gene of Interest Filter" to select "WNKI10000001.1" in our sequence/scaffold list and ~3,000,000 and ~10,000,000 on our Genome Range.

![image](https://user-images.githubusercontent.com/52098813/182619694-5b1ed5d0-2998-439b-b682-fcffa3733ed3.png)

Selecting a filter option will prompt BUSCOGO to automatically update the "Gene of Interest" Table. 

### Our Updated Gene of Interest 

Now we can see that the "Gene of Interest" Table only contains the 435 "Complete", 31 "Duplicated" and 11 "Fragmented" BUSCO genes that exist on the specifc sequence of "WNKI10000001.1" and within the genomic coordinate of ~3,000,000 and ~10,000,000 in our input BUSCO Table. 

![image](https://user-images.githubusercontent.com/52098813/182619778-73efe3cf-301d-4944-9cdb-94346842b827.png)

## 3. Using A Custom Background.

In this example we will be using BUSCOGO's custom background option to filter out any genes that are classified as "Missing" from the background enrichment.

We will utilize the "Background Genes Filter" to only include non "Missing" genes from our background enrichment.

![image](https://user-images.githubusercontent.com/52098813/182619868-f742e6f0-3d91-4d31-bc74-7e44fbad1aa3.png)

We can see that our "Background Genes" Table now only contains the 1929 "Complete", 131 "Duplicated" and 45 "Fragmented" BUSCO genes.

![image](https://user-images.githubusercontent.com/52098813/182619913-eaa5ca44-275d-47d1-8072-d2360990dffe.png)


### Starting Analysis

Once you are happy with your "Gene of Interest" list, we can perform Enrichment Analysis by pressing the "Start Analysis" Button on the top left of the screen.

## 3. Result Generation

BUSCOGO will generate Enrichment result for all three major Gene Ontology Classficition: Biological Process, Molecular Function and Cellular Component. 
Intepretation and explanation of the generated result is avaialble in our main "User Guide".


## Biological Process: Enriched Gene Ontology Terms Result
![image](https://user-images.githubusercontent.com/52098813/182621830-e15e0860-9e0b-45e4-ab9f-7b5410ae39de.png)

## Cellular Component: Enriched Gene Ontology Terms Result
![image](https://user-images.githubusercontent.com/52098813/182621866-51cd3bc3-1602-4f6f-ab72-4ebe7dcba6c4.png)

## Molecular Function: Enriched Gene Ontology Terms Result
![image](https://user-images.githubusercontent.com/52098813/182621879-aa3a4caa-7730-4c1f-94d2-3626dc3998dc.png)
