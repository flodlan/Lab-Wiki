---
layout: default
title: M/EEG Analysis
parent: M/EEG
nav_order: 2
---

# M/EEG Analysis

This section will provide you with information and resources to perform M/EEG analysis. We will mostly highlight the different analysis commonly performed by lab members and links towards relevant resources for them.

## Preprocessing

{: .note }
> Given that most members use MEG, we will focus on the analysis of this type of data. However, keep in mind that it will be fairly similar to EEG. If you want more basic information about M/EEG analysis in general, software to use or other resources check the [MEG Resources]({% link documents/MEG/meeg-resources.md %}) page. 

{: .important }
> Fieldtrip is the **default software** being used for most M/EEG given that it is developed at the Donders and they provide support for it. Hence, most of the analysis described below will have links directing you to tutorials using this software. If you want alternative to this, please refer to the [MEG Resources]({% link documents/MEG/meeg-resources.md %}) page. 


For the preprocessing of MEG data, we follow several general steps:

1. Load the raw participant data
2. Define the trials (usually based on the triggers of your experiment code) -- use `ft_definetrial`
3. (_Optional_) Remove any trials that should be excluded from your main analysis (_e.g.,_ practice trials, incorrect trials, or trials from a specific type)
4. (_Optional_) 3rd order gradient correction (use `ft_denoise_synthetic`): this helps to remove noise from a source outside of the brain/head and possibly from the environment
5. Demean data (use `ft_preprocessing` with `cfg.demean = ‘yes’`)
6. Reject trials with high MEG variance (use `ft_rejectvisual` and select trials manually) – main purpose is to remove SQUID jump artifacts
7. (_Optional_) Reject trials with high muscle activity
8. (_Optional_) Resample data at a lower sampling frequency to reduce data size (use `ft_resampledata`) – **Note**, resampling can change the time axis in undesired ways, in many cases it can be useful to manually define a time axis to which to resample your data so that the data are centered at zero
9. Run ICA analysis to identify and reject components related to eye movements and heart beat (use `ft_componentanalysis`)
10. Save preprocessed and cleaned data to disk

In the following [link](https://www.fieldtriptoolbox.org/tutorial/#reading-and-preprocessing-data) you can find a series of Fieldtrip based tutorials to perform all of the preprocessing steps mentioned.

## Overview of Analysis Type
Analyses of MEG data can broadly be divided into sensor-level and source-level analyses. The former are done on the level of the MEG sensors, while the latter use some sort of source reconstruction technique to estimate activity and specific **source locations**.

### Sensor Level Analysis 

#### Event-related fields (ERFs) for MEG and Event-Related Potentials (ERPs) for EEG
A major goal when analyzing M/EEG data is to examine the modulation of brain activity linked to a specific event. However, due to the large amount of intrinsic and extrinsic noise in the signals, it is nearly impossible to get any data from single trials. A very common approach is to repeat events in your experiment and average the corresponding neural signals over several trials, thus increasing your singal-to-noise ratio (SNR). The main assumption is that the noise is independent from the events and thus reduced when averaging, while the effect of interest stays in place. 

The following links will direct you towards lectures and tutorials on how to perform these analysis for M/EEG data

- Event Related Fields (ERFs) for MEG: [A Fieldtrip Tutorial](http://www.fieldtriptoolbox.org/tutorial/eventrelatedaveraging/)
  - [Important Document with Planar Gradient Information at the DCCN](./Gradients_MEG.pdf)
- Event Related Potentials for EEG: [A Fieldtrip Tutorial](http://www.fieldtriptoolbox.org/tutorial/preprocessing_erp/)
- Parametric and Non-parametric Statistics on Event Related Fields/Potentials: [A Fieldtrip Tutorial](http://www.fieldtriptoolbox.org/tutorial/eventrelatedstatistics)
  - [Lecture from Donders MEG Toolkit on Parametric and Non-parametric Statistics](https://www.youtube.com/watch?v=x0hR-VsHZj8)
- Cluster Based Permutations on ERF/ERPs: [A FieldTrip Tutorial](http://www.fieldtriptoolbox.org/tutorial/cluster_permutation_timelock)

#### Time Frequency Analysis 

Oscillatory components contained in the ongoing EEG or MEG signal often show power changes relative to experimental events. These signals are not necessarily phase-locked to the event and will not be represented in event-related fields and potentials. The goal of this section is to compute and visualize event-related changes by calculating time-frequency representations (TFRs) of power. 

The following links will direct you towards lectures and tutorials on how to perfrom these analysis for M/EEG data

- [Lecture Series by Mike Cohen on Time Series Analysis](https://www.youtube.com/playlist?list=PLn0OLiymPak2BYu--bR0ADNBJsC4kuRWs)
- Time Frequency Analysis in M/EEG: [A Fieldtrip Tutorial](https://www.fieldtriptoolbox.org/tutorial/timefrequencyanalysis/)
- Cluster-based permutation tests on time-frequency data: [A Fieltrip Tutorial](https://www.fieldtriptoolbox.org/tutorial/cluster_permutation_freq/)


### Source-Level Analysis 

{: .note }
> The anatomical MRI is _preferred_ if you want to do source modelling of the MEG signal. Source modelling (also known as "inverse modelling", "source reconstruction", "beamforming" or "dipolefitting") requires that you have a volume conduction model. This volume conduction model (also known as "head model") describes the relation between sources in the head and the measured activity on the outside of the head (either EEG or MEG), and it models the geometry and conductive properties of the head.

> Ask [Paul Gaalman](https://www.ru.nl/personen/gaalman-p) for the standard MRI procedure and sequence.

The following links will direct you towards lectures and tutorials on how to perform these analysis for M/EEG data

- [Headmodel for MEG analysis](https://www.fieldtriptoolbox.org/tutorial/headmodel_meg/) :This tutorial describes how to construct a volume conduction model of the head (head model) based on an individual subject’s MRI.
- Headmodel for EEG analysis: [BEM Volume Conduction Model](https://www.fieldtriptoolbox.org/tutorial/headmodel_eeg_bem/) and [FEM Volume Conduction Model](https://www.fieldtriptoolbox.org/tutorial/headmodel_eeg_fem/)
- [Source Model for MEG or EEG analysis](https://www.fieldtriptoolbox.org/tutorial/sourcemodel/) - This tutorial will tell you how to construct a source model that can be used for source reconstruction of EEG or MEG data.
  - [Lecture from Donders Toolkit on Source Modelling for M/EEG](https://www.youtube.com/watch?v=86f5_x9SVQQ)
  - [Recording Headshape with Polhemus Digitizer at the DCCN](./Polhemus_Final.pdf): Head Shape Digitizer for Co-registration of the Data Recorded in the MEG system with a participant’s individual anatomical MRI scan

- Beamforming: localizing oscillatory sources in MEG data - [A Fieldtrip Tutorial](https://www.fieldtriptoolbox.org/workshop/natmeg2014/beamforming/)
  - [Lecture Recording from Donders Toolkit on Beamforming](https://www.youtube.com/watch?v=Ez72OFjSABs)
- Coherence: localizing activity coherent with a stimulus - [A FielTrip Tutorial](https://www.fieldtriptoolbox.org/tutorial/beamformingextended/)
- Source reconstruction of ERFs with Minimum-Norm Estimation - [A Fieldtrip Tutorial](https://www.fieldtriptoolbox.org/tutorial/minimumnormestimate/)
- Dipole Fitting - [A Fieldtrip Tutorial](https://www.fieldtriptoolbox.org/workshop/natmeg2014/dipolefitting/)
- Virtual channels - [A Fieldtrip Tutorial](https://www.fieldtriptoolbox.org/tutorial/virtual_sensors/)

#### Additional Analysis 
##### MVPA

- A Tutorial on Multivariate Pattern Analysis Applied to Time Series Neuroimaging Data - [An Overview](https://direct.mit.edu/jocn/article/29/4/677/28605/Decoding-Dynamic-Brain-Patterns-from-Evoked)
- [Video Lecture on Implementation and Concepts behind MVPA](https://www.youtube.com/watch?v=f3yrVfVtCUE)
- MVPA Tutorial - [A Fieldtrip Tutorial](https://www.fieldtriptoolbox.org/tutorial/mvpa_light/)
- From ERPs to MVPA Using the Amsterdam Decoding and Modeling Toolbox (ADAM) - [Beginner Friendly Toolbox](https://www.frontiersin.org/journals/neuroscience/articles/10.3389/fnins.2018.00368/full)

  
