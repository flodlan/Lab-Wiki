---
layout: default
title: M/EEG Analysis
parent: M/EEG
nav_order: 2
---

# M/EEG Analysis

This section will provide you with information and resources to perform M/EEG analysis. We will mostly explain the different analysis commonly performed by lab members and the available software you can use for tme. 

## Software

The main software used by the members of the Predictive Brain Lab to do M/EEG analysis is the following:
* [FieldTrip](https://www.fieldtriptoolbox.org/) - **MATLAB** software toolbox for MEG, EEG and iEEG analysis. This is the **default** software being used given that it is developed at the Donders and they provide support for it.
* [MNE](https://mne.tools/stable/index.html#) - Open-source **Python** package for exploring, visualizing, and analyzing human neurophysiological data: MEG, EEG, sEEG, ECoG, NIRS, and more
* [EEGLAB](https://sccn.ucsd.edu/eeglab/index.php) - EEGLAB is an interactive **Matlab** toolbox for processing continuous and event-related EEG, MEG and other electrophysiological data

{: .note }
> You can ask other lab members if they have pro's and con's regarding their software selection before deciding what to use. It may be the case that specific software is better for some analysis compared to others. 

## Preprocessing
{: .note }
> Given that most members use MEG, we will focus on the analysis of this type of data. However, keep in mind that it will be fairly similar to EEG. If you want EEG specific information, go to the MEG resources [ADD PAGE] page where you will find links to relevant EEG tutorials.

Additionally, we will provide snippets of code for the different analysis steps related to FieldTrip. 


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



