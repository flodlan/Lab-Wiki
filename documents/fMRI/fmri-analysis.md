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

## Analysis
### Univariate Analysis (First- and Higher-Level Analysis)

If you are already familiar with performing univariate analysis at the single/first level, the following resource provides you with a great overview of all the relevant terms you will be employing if you decide to make use of FSL: [First-Level Analysis](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/task_fmri/feat/user_guide?id=first-level-analysis)

Similarly, if you are interested in performing univariate analysis at the group level, this resource contains the most importa information when using FSL: [Higher-level Analysis](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/task_fmri/feat/user_guide?id=higher-level-analysis)

If both of these resources feel a bit too specific for you, the following page contains general information on performing analysis on task-based fMRI data (which tends to be what most lab members are concerned with): [Task Based fMRI](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/task_fmri/index).

Lastly, if these resources feel too advanced or if you would like to refresh your memory on these different analysis, check the [fMRI Resources page]({% link documents/fMRI/fmri-resources.md %}) for different learning materials. 

{: .note}
> We like FSL in particular, as it’s a mature and well-maintained package, free and open-source, and provides both a graphical interface and a command line interface for most of its tools.

_Of course, there are other libraries you can use to perform univariate analysis. Here, we are only highlighting the resources currently used by lab members and that have proven to be easier to use._

### Multivariate Analysis
This section will cover some more advanced analysis that can be performed using fMRI data. For a lot of these methodologies, Python is the preferred programming language. Hence, this section will mostly be **Python Based**. If you are not comfortable with using Python, you can 
1. Search for a different package that performs the same analysis
2. Check out the [Programming Language Section]({% link documents/technical-help/software/programming_languages.md %}) and get up to speed with Python!

Before getting started with specific analysis, we recommend reading this paper:
* [Machine learning for neuroimaging with scikit-learn](https://www.frontiersin.org/journals/neuroinformatics/articles/10.3389/fninf.2014.00014/full)

It walks you through the core concepts that you will need to know when performing multivariate/more complicated analysis to your brain data. 

Additionally, this notebook will be mainly referencing the [NiLearn Python Package](https://nilearn.github.io/stable/index.html). This was developed for appying statistical learning techniques (from GLMs to multivariate “decoding” and connectivity techniques) to neuroimaging data. The great thing about it is that it contains instructive documentation (allowing you to fetch publicly available data and performing analysis on this), as well as working with an open community. 

As a first step, it is a great idea to:
1. Read through their [user manual](https://nilearn.github.io/stable/user_guide.html) and get a good understanding of the types of analyses you can do using NiLearn
2. Look at the different [examples of analyses](https://nilearn.github.io/stable/auto_examples/index.html) you can perform using this package

Now, we will provide links for the important types of analyses you might be interested in performing:

* [Decoding and MVPA: Predicting from Brain Images](https://nilearn.github.io/stable/decoding/index.html) - This page contains thorough explanations of the different analysis you can perform as well as code examples and important notions to consider.
  * [PyMVPA](http://www.pymvpa.org/) - another open source free alternative to perform MVPA analysis (not restricted to the neuroimaging domain using a Python base) 
* [Functional Connectivity and Resting State Analysis](https://nilearn.github.io/stable/connectivity/index.html) - Similarly as the previous one, this page also includes information on quite advanced statistical analysis that you can perform when analyzing brain images.
* [Representational Similarity Analysis](https://rsatoolbox.readthedocs.io/en/latest/index.html) - This is not part of NiLearn, but rather a toolbox (and tutorials) on how to perform RSA. This is a very useful technique especially when wanting to compare data of different modalities (_e.g.,_ behavioral, neuroimaging, AI). The developers of this method created their own website containing useful documentation for it. 

## Brain Visualization

An important part of performing your analysis is to be able to display the information you obtained. This is not a trivial task and some forms of visualization are more intuitive and informative than others (depending on the goal of your study)

This page contains information on how to perform different visualizations by making use of the NiLearn package: [Visualizing Neuroimaging Data using NiLearn](https://nilearn.github.io/stable/plotting/index.html)


