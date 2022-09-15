# PIAAC2ESCO - An AI-driven classification of the PIAAC Background questionnaire onto the ESCO Skills Pillar


{{TOC}}

## What is PIAAC2ESCO?
PIAAC2ESCO provides a characterisation of the [PIAAC background questionnaire](https://www.oecd-ilibrary.org/sites/53c2f904-en/index.html?itemId=/content/component/53c2f904-en) on the base of the [ESCO Skills Pillar](https://esco.ec.europa.eu/en/escopedia/skills-pillar). In practice it associates a list of ESCO skills (v1) to questions of the PIAAC background questionnaire (version 2010), based on their similarity. We use the section F to I of the PIAAC background questionnaire, from which we select the relevant questions (73 questions[^F_Q02a, F_Q02b, F_Q02c, F_Q02d, F_Q02e, F_Q03a, F_Q03b, F_Q03c, F_Q04a, F_Q04b, F_Q05a, F_Q05b, F_Q06b, F_Q06c, F_Q07a, G_Q01a, G_Q01b, G_Q01c, G_Q01d, G_Q01e, G_Q01f, G_Q01g, G_Q01h, G_Q02a, G_Q02b, G_Q02c, G_Q02d, G_Q03b, G_Q03c, G_Q03d, G_Q03f, G_Q03g, G_Q03h, G_Q04, G_Q05a, G_Q05c, G_Q05d, G_Q05e, G_Q05f, G_Q05g, G_Q05h, H_Q01a, H_Q01b, H_Q01c, H_Q01d, H_Q01e, H_Q01f, H_Q01g, H_Q01h, H_Q02a, H_Q02b, H_Q02c, H_Q02d, H_Q03b, H_Q03c, H_Q03d, H_Q03f, H_Q03g, H_Q03h, H_Q04a, H_Q05a, H_Q05c, H_Q05d, H_Q05e, H_Q05f, H_Q05g, H_Q05h, I_Q04b, I_Q04d, I_Q04h, I_Q04j, I_Q04l, I_Q04m] out of 84 questions) and all the ESCO skills (13600 items ==descriviamo uso delle alternative labels?==)

## How does PIAAC2ESCO work?
The linkage is done using AI in a framework that combines various methods: embeddings, selection of the best embedding and taxonomy alignment (Giabelli et al, 2022)[^The framework designed in WETA (Web Taxonomy Embedding Alignment) relies on distributional semantic and context information to perform taxonomy alignment, blending a hierarchical approach based on cosine similarity and a machine learning classification task that uses the embeddings as input features. Moreover, it performs an intrinsic evaluation of the selected embedding model based on the structure of the taxonomy itself.] and experts' validation.
The training dataset of the embedding is the description of Online Job Advertisements (OJAs), which provides richer information compared to other embedding methods presented in the literature. ==Examples==. 

Our dataset is the representative sample of the job ads collected by Eurostat and Cedefop as part of the Web Intelligence Hub - Online Job Advertisements (WIH-OJA) project. A representative sample is provided as part of the natural language processing (NLP) dataflow and can therefore be used as a benchmark to replicate our results. The sample is made of 504 job ads that include title and description. The sample is designed to provide a balanced coverage of occupation, type of contract, salary, working time, education, economic activity and experience. Each cell has a size of 50 records [^ Languages for which less than 50 ads for each category are not part of the sample, e.g. Ukrainian, Russian and Flemish. For more information visit the [WIH wiki page](https://webgate.ec.europa.eu/fpfis/wikis/display/TSS/OJA-NLP+dataflow).]

## Structure of the dataset 
The dataset is made of the following variables:

| Variable name | Description |
|:--|:--|
|Isco_Level_2 | ISCO08 Sub-major group occupation Name |
|preferredLabel| ISCO08 Sub-major group occupation Label|
|Question Id| PIAAC question Name |
|Question Description| PIAAC question Label |


## Use cases


## @ Notes - temp

The proposal presented in this research advances a new methodology. But its purpose is much wider, though.  In a fast-developing field of research, the scientific community must lay down the soundest principles on which to develop its enterprises. 
One of the main issues in our society is the increasing value of data and the decreasing value of theories to explain them. 
Indeed, new research in the field is currently based on privately produced data, which lack accountability in terms of full disclosure of the methodology with which they are produced. This fact impinges on the possibility to replicate the results of research based on this data. Datasets of online job ads originated by Eurostat and Cedefop, which bear the standard of official statistics, should constitute the benchmark for any other study. Data sources whose origin is not auditable by the research community should then be compared with the standard benchmark provided by the official statistical offices.

## References
[Giabelli, A., Malandri, L., Mercorio, F., & Mezzanzanica, M. (2022). WETA: Automatic taxonomy alignment via word embeddings. Computers in Industry, 138, 103626.](https://www.sciencedirect.com/science/article/pii/S0166361522000215)