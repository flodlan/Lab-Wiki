---
layout: default
title: Preregistration and Reproducibility
parent: Standard Operating Procedures
grand_parent: Lab Basics
nav_order: 3
---

## Preregistration and Reproducibility
For the Predictive Lab's stance on Open Science practices and preregistration please refer to our [handbook](https://drive.google.com/file/d/1RMTpcPl8lwJ6Ozf3QIlTaehedsL_tSUC/view)

Any project analysis script should be easily reproducible by other lab members or external parties. Hence, we try to always write code with the assumption that someone else will have to reproduce it without assistance. If you require a nudge on how to organize your code, look at [the writing code section]({% link documents/technical-help/software/reproducible_code.md %}) of the wiki on efficient coding practices. 

The research data for members of the DCCN should be findable and accessible. This can largely be achieved by actively archiving and publishing data via the Radboud Data Repository (RDR), under an appropriate license and access level, and by annotating the data with rich metadata. A major goal of the Donders Institute is to preserve and share research data for the long term. Hence, every researcher at the DCCN is nudged to make their data publicly available ([exceptions exist](https://www.ru.nl/rdm/vm/policy-documents/)). 

The regulations on Research Data Management from the Radboud University can be found [here](https://www.ru.nl/rdm/vm/policy-documents/) and those specific for members of the DCCN [here](https://intranet.donders.ru.nl/index.php?id=6467).



### UNDER CONSTRUCTION
When finalizing a study, the raw data, stimulus material, experiment scripts and analysis scripts should be uploaded to a Data Sharing Collection (DSC). For more information on research data management see here and here. When preparing a manuscript for publication, you should include a link to the DSC in a data availability statement within the manuscript.

Preprint: You should include a general statement that the data and code will be shared. Example: "Data and code will be made available on the Donders Institute for Brain, Cognition and Behavior repository (https://data.donders.ru.nl/)."

Journal submission: Switch the status of the DSC to "reviewable external". Then include the reviewer link in the data availability statement of the manuscript before submitting to a journal. Example: "Data and code are available from the Donders Institute for Brain, Cognition and Behavior repository at https://data.donders.ru.nl/login/reviewer-68224366/4OBcpDMRsC8DhYPM-C4Pk5B4GAw1eB5R6Ac76OfiFsl." Note that this link is not meant for sharing the data for research purposes, but only for review.

Upon Acceptance: Switch the status of the DSC to "published" (not reversible!). Then exchange the reviewer link in the data availability statement with the persistent identifier of the published DSC. Example: "Data and code are available from the Donders Institute for Brain, Cognition and Behavior repository at http://hdl.handle.net/11633/di.dccn.DSC_3018029.03_140."





# Preregistration


In the lab we use two different platforms to preregister our studies:
1. [As Predicted](https://aspredicted.org/)
2. [Open Science Framework (OSF)](https://osf.io/)

with **As Predicted** following a specific structure and **OSF** providing more freedom to your structure. 

The current page provides you with guidance on the information you might want to include in your pre-registration document: 

1. The title of your project.
2. Whether any data have been collected for the study already.
3. The research questions and the hypotheses.
- What are the questions you want to answer with the current study?
- What are your hypotheses?
4. The variables and conditions in your study
- What is the dependent variable?
- What are the independent variables?
- What conditions do you have?
- Is the design event-related or blockwise (for fMRI studies)
5. Primary analyses
- What are the most important analyses you are going to perform?
- How are you going to perform these analyses?
- On which effects are you focusing to answer your main questions?
- How are you going to define your ROIs (for fMRI studies)?
6. Secondary analyses
- What other analyses are you going to perform?
7. Sample size
- How many participants will you test?
- How do you justify this sample size? (see also your PPM)
8. Quality check of your data
- How do you determine whether the data quality is good?
- When will you exclude a participant?
- i.e. if they missed more than …% of all trials.
- i.e. if they showed excessive motion during scanning.
9. Other
- Are there any other aspects of the study you would like to preregister?


The following three links are examples of pre-registered studies in the lab using the OSF:
* Matthias Fritsche - [The role of feature-based attention for serial dependence in perceptual decision making](https://osf.io/q7gj3/)
* Chuyao Yan - [Predicting groups of objects in the visual ventral stream](https://osf.io/s59p6)
* Jonas Karolis Degutis - [Laminar fMRI at 3T: A replication attempt of top-down and bottom-up laminar activity in the early visual cortex](https://osf.io/txuye/)
