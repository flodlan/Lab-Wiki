---
layout: default
title: fMRI Analysis
parent: fMRI
nav_order: 2
---

# BIDS Documentation 
The data that results from neuroimaging experiments is complex and can be structured in many different ways. For quite some time, there was a lack of consensus on how to organize and share this type of data. The major problem of this unstructured approach is that it would lead to misunderstandings and time wasted on re-structuring data or re-writing scripts (contradicting efforts of making neuroscience more reproducible). [BIDS](http://bids.neuroimaging.io/) describes a format to organize neuroimaging and behavioural data (_i.e.,_ a folder structure, naming structure, etc.), solving the problems described above. 

Given the benefits of using this structure for sharing data and information with other labs and researchers, it is mandatory for members of the Predictive Brain Lab to use this format. 

#### What tool can we use to do this?
To conver the raw data (DICOM) automatically to the BIDS format, you can use the [Bidscoin tool](https://github.com/Donders-Institute/bidscoin). Their website contains information on how exactly you can do this. 

# fMRI Analysis
Once you have converted the raw data files to NIFTI using BIDScoin, you can proceed with the data processing steps.

## Preprocessing with fmriprep
The first step in fMRI analysis is preprocessing the data. The standard tool at the DCCN to pre-process fMRI data is [fMRIprep](https://fmriprep.org/en/stable/). 

#### Why do we use this tool?
fMRIprep is a data preprocessing **pipeline** that offers a user-friendly, state-of-the-art interface. It is robust to variations in scan protocols, requires minimal user input, and provides clear, comprehensive error and output reporting.
It reduces researcher degrees of freedom and aligns with the reproducibility goals followed by the lab. 

#### What preprocessing steps does it perform?
It is mostly concerned with performing the _basic preprocessing_ steps when looking at fMRI data:

* Coregistration
* Normalization
* Unwarping
* Noise Component Extraction
* Segmentation
* Skull-stripping

However, the specific steps performed will depend on the type of MRI data you are feeding the pipeline as well as the meta-data included. To get a better overview, you can check [this page](https://fmriprep.org/en/stable/workflows.html#bold-preprocessing)

The output obtained from preprocessing your data in this way should be easily submittable to many different group level analysis, such as task-based or resting-state fMRI, graph theory measures, and surface or volume-based statistics. 

#### How does fMRIprep work?
It combines tools from well-known software packages for analyzing this type of data (_e.g.,_ FSL, ANTs, FreeSurfer, and AFNI), selecting the best software implementation for the different stages of the preprocessing. 

The advantage of using this tool is that developers are constantly optimizing the pipeline. Modifying the preprocessing steps for it to match with the software that currently performs these steps as best as possible. Additionally, it automatizes and parallelizes processing steps, which provides a significant speed-up from manual processing or shell-scripted pipelines.

## Standard Analysis
### Univariate Analysis (First- and Higher-Level Analysis)

If you are already familiar with performing univariate analysis at the single/first level, the following resource provides you with a great overview of all the relevant terms and matrices you will be employing if you decide to make use of FSL: [First-Level Analysis](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/task_fmri/feat/user_guide?id=first-level-analysis)

Similarly, if you are interested in performing univariate analysis at the group level, this resource contains the most importa information when using FSL: [Higher-level Analysis](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/task_fmri/feat/user_guide?id=higher-level-analysis)

If both of these resources feel a bit too specific for you, the following page contains general information on performing analysis on task-based fMRI data (which tends to be what most lab members are concerned with): [Task Based fMRI](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/task_fmri/index).

Lastly, if these resources feel too advanced or if you would like to refresh your memory on these different analysis, check the [fMRI Resources page]({ % link documents/fMRI/fmri-resources.md %}) for different learning materials. 
