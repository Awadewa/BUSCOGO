# Using BUSCOGO To Determine the Enriched GO Term of "Missing" BUSCO Genes

In this example, we will be utilizing BUSCOGO to find the Enriched GO Term that corresponds to BUSCO genes that are classfied as "Missing" from our input. 

## 1. Input Data

We will be working with the BUSCO Table of a mite genome processed through BUSCO using the Arachnid lineage. The BUSCO Table used as input for this example can be found above. 

User can upload the BUSCO table into BUSCOGO through the "Upload File" button on the top left of the screen.

![image](https://user-images.githubusercontent.com/52098813/182611518-29c16dfd-003b-4e38-b81a-85a932bdf07c.png)

## 2. Selecting our "Gene Of Interest"

### Viewing Our Input BUSCO Table Content

Once a BUSCO Table is uploaded, user can view the corresponding gene content of the BUSCO table. Below the "Gene of Interest" table we can see the statistics of the input BUSCO Table in our "Gene of Interest Stats".

From it, we can see that our input contains 30003 total BUSCO genes, which 1929 of them is classifed as "Complete", 898 of them are classifed as "Missing", 131 of them are classified as "Duplicated" and 45 of them are classified as "Fragmented".

![image](https://user-images.githubusercontent.com/52098813/182611631-d9408a79-51eb-405e-94ec-cdc530a34fda.png)

### Filtering Our "Gene of Interest"


For this example, we are only interested in observing BUSCO genes that are classfied as "Missing" in our input BUSCO Table. Therefore, we will utilize the "Gene of Interest Filter" and select the "Missing" BUSCO Status to only select "Missing" BUSCO.


![image](https://user-images.githubusercontent.com/52098813/182611646-cedcc098-889d-4790-97bf-e88551c0fc86.png)

Selecting a filter option will prompt BUSCOGO to automatically update the "Gene of Interest" Table. 

### Our Updated Gene of Interest 

Now we can see that the "Gene of Interest" Table only contains the 898 BUSCO genes that are classified as "Missing". 


![image](https://user-images.githubusercontent.com/52098813/182611681-510ff31a-8727-402a-bdd2-9b9881f101f6.png)

### Starting Analysis

Once you are happy with your "Gene of Interest" list, we can perform Enrichment Analysis by pressing the "Start Analysis" Button on the top left of the screen.

## 3. Result Generation

BUSCOGO will generate Enrichment result for all three major Gene Ontology Classficition: Biological Process, Molecular Function and Cellular Component. 
Intepretation and explanation of the generated result is avaialble in our main "User Guide".

## Biological Process: Enriched Gene Ontology Terms Result
![image](https://user-images.githubusercontent.com/52098813/182612238-ad9b49f2-a668-44e3-bff5-5404d0b6501d.png)


## Cellular Component: Enriched Gene Ontology Terms Result
![image](https://user-images.githubusercontent.com/52098813/182612269-585ac670-7044-4e78-a80c-a0f1e2a7c722.png)


## Molecular Function: Enriched Gene Ontology Terms Result
![image](https://user-images.githubusercontent.com/52098813/182612292-10292d64-b98f-42d1-bd86-06642f4941ac.png)
