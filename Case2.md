# Using BUSCOGO To Find Possible Trends of Duplicated BUSCO Genes GO Term across 4 Different Mite Species.

In this example, we will be utilizing BUSCOGO to find the Enriched GO Term that corresponds to BUSCO genes that are classfied as "Duplicated" in at least 3 out of 4 Inputs.

## 1. Input Data

We will be working with the BUSCO Table of a 4 different mite genome processed through BUSCO using the Arachnid lineage. The BUSCO Table used as input for this example can be found above. 

User can upload the BUSCO table into BUSCOGO through the "Upload File" button on the top left of the screen.

![image](https://user-images.githubusercontent.com/52098813/182615105-c08b14ee-cd07-4ae2-98a5-06980353d137.png)
## 2. Selecting our "Gene Of Interest"

### Viewing Our Input BUSCO Table Content

Once a BUSCO Table is uploaded, user can view the corresponding gene content of the BUSCO table. Below the "Gene of Interest" table we can see the statistics of the input BUSCO Table in our "Gene of Interest Stats".

From it, we can see that our 4 input contains 12105 total BUSCO genes, which 7732 of them is classifed as "Complete", 3495 of them are classifed as "Missing", 697 of them are classified as "Duplicated" and 181 of them are classified as "Fragmented".

![image](https://user-images.githubusercontent.com/52098813/182615182-a7ac1e72-95db-4836-8574-5cf6881ee335.png)


### Filtering Our "Gene of Interest"

For this example, we are only interested in observing BUSCO genes that are classfied as "Duplicated" in atleast 3 out of the 4 input BUSCO Table. When multiple files is detected, BUSCOGO will give the user the extra option of inputing a threshold filter for BUSCO Status. 

Therefore to select BUSCOGO genes that are "Duplicated" in at least 3 out of the 4 input files, we will utilize the "Gene of Interest Filter" and select the "Duplicated" BUSCO Status and enter "75%" in the duplicated percentage threshold.


![image](https://user-images.githubusercontent.com/52098813/182616141-101cba44-be32-4e72-bcd7-4dcde211320b.png)


Selecting a filter option will prompt BUSCOGO to automatically update the "Gene of Interest" Table. 

### Our Updated Gene of Interest 

Now we can see that the "Gene of Interest" Table only contains the 451 BUSCO genes that are classified as "Duplicated" in at least 3 out of 4 Input Files. 

![image](https://user-images.githubusercontent.com/52098813/182617107-9fe88c77-a14e-4876-b456-db8ad6d234e7.png)

### Starting Analysis

Once you are happy with your "Gene of Interest" list, we can perform Enrichment Analysis by pressing the "Start Analysis" Button on the top left of the screen.

## 3. Result Generation

BUSCOGO will generate Enrichment result for all three major Gene Ontology Classficition: Biological Process, Molecular Function and Cellular Component. 
Intepretation and explanation of the generated result is avaialble in our main "User Guide".


## Biological Process: Enriched Gene Ontology Terms Result
![image](https://user-images.githubusercontent.com/52098813/182617838-96b31b9a-1fd6-42aa-80f8-42a1f8d81be6.png)

## Cellular Component: Enriched Gene Ontology Terms Result
![image](https://user-images.githubusercontent.com/52098813/182617873-11e5f4bc-40a1-4acb-aee4-10cfe3894dc6.png)

## Molecular Function: Enriched Gene Ontology Terms Result
![image](https://user-images.githubusercontent.com/52098813/182617901-6efc2bbc-e672-4af1-bfe1-42a32ef9be1c.png)
