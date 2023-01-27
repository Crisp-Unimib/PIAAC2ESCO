# PIAAC2ESCO - An AI-driven classification of the PIAAC Background questionnaire onto the ESCO Skills Pillar

### What is PIAAC2ESCO?
PIAAC2ESCO provides a characterisation of the [PIAAC background questionnaire](https://www.oecd-ilibrary.org/sites/53c2f904-en/index.html?itemId=/content/component/53c2f904-en) on the base of the [ESCO Skills Pillar](https://esco.ec.europa.eu/en/escopedia/skills-pillar). In practice it associates a list of ESCO skills (v1.0.8) to questions of the PIAAC background questionnaire (version 2010), based on their similarity. We use the section F to I of the PIAAC background questionnaire, from which we select the relevant questions (73 questions out of 84) and all the ESCO skills (13600 items). The validated dataset covers 21 PIAAC questions and the mapped ESCO skills, which are enriched using alternative labels.

### How does PIAAC2ESCO work?
The linkage is done using AI in a framework that combines various methods: embeddings, selection of the best embedding, taxonomy alignment and experts' validation. A description of the adopted methodology is available in the [Technical Annex](https://github.com/Crisp-Unimib/PIAAC2ESCO/blob/master/piaac2esco_technicalAnnex.pdf).

The training dataset of the embedding is the representative sample of the job ads collected by Eurostat and Cedefop as part of the [Web Intelligence Hub - Online Job Advertisements (WIH-OJA)](https://www.cedefop.europa.eu/it/about-cedefop/public-procurement/towards-european-web-intelligence-hub-european-system-collection-and-analysis-online-job) project. A representative sample is provided as part of the natural language processing (NLP) dataflow and can therefore be used as a benchmark to replicate our results. The sample is made of job ads that include title and description. The sample is designed to provide a balanced coverage of occupation, type of contract, salary, working time, education, economic activity and experience.

### Structure of the dataset 
The  PIAAC2ESCO dataset is made of the following variables:

| Variable name | Description |
|:--|:--|
|PIAAC_QuestionId| PIAAC question Name |
|PIAAC_QuestionDescription| PIAAC question Label |
|ESCO_skill_conceptURI| Associated ESCO skill |
|ESCO_skill_en| Associated ESCO skill - English label |
|ESCO_version| ESCO version of the mapping |

The file is stored in the output folder: [PIAAC2ESCO.csv](https://github.com/Crisp-Unimib/PIAAC2ESCO/blob/master/output/PIAAC2ESCO.csv)

### Contributors
PIAAC2ESCO was developed in the framework of the European Union's Horizon 2020 [*Pillars - Pathways to inclusive labour markets*](https://www.h2020-pillars.eu). The main objective of PILLARS is to study the development of skills and their demand, to inform policies on how to revise education and training systems to create the opportunities to acquire them. The contributors are:

- **Fabio Mercorio** (Dept of statistics and quantitative methods - University of Milano-Bicocca, [Interuniversity Research Centre on Public Services (CRISP)](https://crispresearch.it)): supervision, methodology, conceptualisation; 
- **Mario Mezzanzanica** (Dept of statistics and quantitative methods - University of Milano-Bicocca, [Interuniversity Research Centre on Public Services (CRISP)](https://crispresearch.it)): Project administrator, funding acquisition, supervision. 
- **Filippo Pallucchini** (Dept of statistics and quantitative methods - University of Milano-Bicocca, [Interuniversity Research Centre on Public Services (CRISP)](https://crispresearch.it)): resources, data curation, validation
- **Francesco Trentini** (Dept of statistics and quantitative methods - University of Milano-Bicocca, [Interuniversity Research Centre on Public Services (CRISP)](https://crispresearch.it)): methodology, formal analysis, investigation, validation
- **Yuchen Guo** ([Katholische Universität Eichstätt-Ingolstadt (KU)](https://www.ku.de), ifo Institute Munich): validation
- **Christina Langer** ([Katholische Universität Eichstätt-Ingolstadt (KU)](https://www.ku.de), ifo Institute Munich, Harvard Kennedy School): validation

### Contacts
If you want to have more information or to report works that use PIAAC2ESCO to be listed on this page, please [write us an email](mailto:francesco.trentini@unimib.it).

### Related Publications
[Guo, Y., Langer, C., Mercorio, F., Trentini F. (2022) Skills Mismatch, Automation, and Training: Evidence from 17 European Countries Using Survey Data and Online Job Ads. EconPol Forum 23 (5), 11-15. CESifo, Munich, 2022](https://www.cesifo.org/en/publications/2022/article-journal/skills-mismatch-automation-and-training)
