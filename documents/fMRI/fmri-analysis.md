---
layout: default
title: fMRI Analysis
parent: fMRI
nav_order: 2
---

# BIDS Documentation 
[BIDS](http://bids.neuroimaging.io/) describes a format to organize neuroimaging and behavioural data (_i.e.,_ a folder structure, naming structure, etc.) It is mandatory for members of the Predictive Brain Lab to use this format. The raw DICOM data can be automaticallt converted into the BIDS format using the [bidscoin tool](https://github.com/Donders-Institute/bidscoin). 

## BIDScoin
This is employed to convert the raw (DICOM) data to the BIDS format. BIDScoin is available on the DCCN cluster. For an extensive tutorial on how to use BIDScoin, see [here](https://github.com/Donders-Institute/bidscoin#bidscoin-tutorial).

This [document]({% link documents/fMRI/bids-coin.md %}) highlights the steps to conver the raw (DICOM) data into the BIDS format.:)

# fMRI Analysis

Once you have converted the raw data files to NIFTI using BIDScoin, you can proceed with the data processing steps.
This section will provide valuable insights into analyzing fMRI experiments. It includes a collection of resources compiled by various lab members over the years, which they found useful for analyzing this type of data. 

## Preprocessing with fmriprep
