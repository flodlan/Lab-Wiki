---
layout: default
title: 7T Essen fMRI
parent: fMRI
nav_order: 4
---

# 7T Essen fMRI

{: .important }
> There is no available information on the intranet regarding the 7T scanner in Essen. The information presented here is the one compiled in the old lab wiki. Hence, it might be **outdated**.

### Completely New?
- Contact between Essen & Donders is not very formalized. It is best to contact someone who scans there and join for one session to get to know the important players.
- In addition, contact [Oliver Kraff](https://www.hahn-institut.de/de/ueber/team/kraff-oliver)(Researcher in Essen) and [Peter Koopmans](https://www.diagnijmegen.nl/people/peter-koopmans/) with short introduction of yourself and your project.

## Organization
### Security 
- Familiarize yourself with 3T security
- Get security training (_see below_)

### Getting Access to the Scanner
#### Security Training / Certified User
 * Contact [Oliver Kraff](https://www.hahn-institut.de/de/ueber/team/kraff-oliver) for a 1h onsite security training.
 * If you speak German, you can join one of the hospital trainings.
 * If you speak English, you will get a "private" training
 * If you have used the MRI for more than 3 years, you can do an online course, see this [link](https://hahn-institut.de/projects/safetytraining)

{: .note }
> If you will be scanning together with RA's, make sure to bring them with you so they get the security training as well

#### Getting a key

* Bring 50€ (you will get them back) to the secretary. You will need to leave your email address
* The key will work for scanner + doors

### People and Responsibility 

#### Oliver Kraff
* _Security Responsibility Person in Essen_
* Will provide the security training
* Will guide you around the scanner.

#### Stefan Maderwald
* _Lab Manager_

#### [David Norris](https://www.ru.nl/en/people/norris-d)
* _Responsible Donders PI. Will be responsible for your projects proposals_
* Talk to him at least once so he knows what you want to do 

#### [Peter Koopmans](https://www.diagnijmegen.nl/people/peter-koopmans/)
* _PI Contact Person in Nijmegen_
* Can help you setup the sequences you need
* Very knowledgeable in laminar analysis 
* Adapted the offline Streamer for CAIPI data

#### Marcel Gratz
* _Admin_
* Will provie you with SSH access to the ETH computers

##### Other people
* Thomas Ernst & Viktor Pfaffenrot are using the fMRI rack & streamer

### Applying for Scanning Time
To apply to use the scanner in Essen, it has to be done through their [website](https://hahn-institut.de/projects/). 
There are two booking options:
1. Pilot (6h)
2. Full Scanning (it requires to do an Essen PPM, see [link](https://hahn-institut.de/projects/help))

{: .note }
> We recommend reading the [help section](https://hahn-institut.de/projects/help) when applying for a project. It contains all the updated information.

#### Pilot
The online website will generate a prefilled form that you have to print and bring to David Norris. Use the online form!
_Comments to specific fields from previous lab member experiences:_

#### Funding
- If you do not have scanning overhead in your grant (ask Floris): After talking to Finance Donders I put "not applicable"
- If you have scanning overhead: Add this information here

#### Ethical
- If you have a normal study, you just have to tick the "fmri" rack option.
- You have to click Covered by "general approval no. 16 7214 BO" and the blue questionairy (for healthy subjects).
- Ask David Norris before you hand it in if this is OK (just to be sure).
- No Donders Ethical Approval necessary
- ELH-PI is David Norris

##### PPM
This [page](https://hahn-institut.de/projects/help) contains information about how to do a PPM there.

### Getting to Essen
You can arrange the transport to and from Essen, Germany with the [Donders Administration](admin@donders.ru.nl). Send them an email stating:

> _Could you please arrange a rental car for me for the following date and time?_
> 
> _[Day of the Week and Month]_
> _[Time to] pick up car from [Rental Car Agency]_
> _[Time to] return car to [Rental Car Agency]_
> 
> _any car they have will do. Thank you in advance!_

You can then go to the rental car agency and get your car. 
{: .important }
> The car agency used in the past has closed since then. Hence, check with admin whether there are any alternatives.

### Measuring Subjects

* Find a subject in Sona
* Book scanning time (On Wednesdays, if booked ahead, we have priority) 2 weeks ahead
* Subjects have to fill the Donders form 24h before
* If they have any metal in their body (tattoos, dental wire, etc.) write to Oliver Kraff . The 7T machine has different regulations than the regular 3T.
* Subjects have to fill a form from the Essen institute (these are usually at the scanner)
* Write down your consecutive subject-id + project ID + number of volumes you acquired into the logbook


## Analysis of 7T Data
Data are analysed similarly to 3T data. These steps were I inherited from Sam Lawrence and he from Peter Kok in order.

### Essen Recording
Essen has quite a few additional manual steps that are quite complex to explain without sitting in front of the scanner. You will usually get an introduction. 

#### CAIPI reconstruction
The CAIPI 3D-EPI sequence (allowing 3D*Acceleration) in Essen is extremely slow to reconstruct on the scanner (~15min for 3 volumes), therefore we record the raw-raw 3D k-space data and reconstruct it offline at the donders. The "CAIPI Sequence" allows to record ~60 slices of 0.8mm isotropic with a TR of 2.3s. Alterantive sequence with ~48slices and TR of 3.5s. Dataquality gets a hit with CAIPI, but its hard to compare.

#### Recording/streaming CAIPI
- Start the streamer by ssh'ing to the streamer computer and starting the streaming script
- On the fMRI scanner console open the start menü, there are three scripts:
  - START BLOCK
  - START
  - STOP
- You most often want START BLOCK, which starts streaming and blocks the scanner from reconstructing the image
- It is recommended to record 1 Volume (for the header) that you also reconstruct by the scanner. Therefore you would run START before starting the 1 volume acquisition.
- Use STOP to stop it.

- Sometimes the scanner reconstruction is messed up.

#### Streaming to Donders

- Get an openvpn tunnelkey from Marcel Gratz (see above) & SSHkey for the streamer
- Open VPN connection to ELH
- putty/ssh to streamer using SSHkey
- putty/ssh back to Donders

`screen ssh *L 1234:mentat004:22 *p 22 benehi@ssh.dccn.nl`

- Copy your files

`rsync *ahv **progress *e 'ssh *p 1234' meas_MID21_benehi_caipi_localizer.dat benehi@localhost:/project/3018028.04/benehi/test.dat`

#### Offline Reconstruction
- In case you want to reconstruction offline (one 10min run ~50GB) you need the reconscripts from Peter Koopmans. Write him to get the newest edition.
- Recon is quite slow (1st Volume much slower than the others)
- You need to put one reconstructed volume in the same folder so that the script can copy the DICOM header.
- You have to specify the CAIPI acceleration factors. For me it was 4times in plane and 2 in z*plane so:

`ELH_3DEPI_reconstruction_function(datadir,[4 2])`

### Pipeline
Mostly consistent with Sam J. D. Lawrence Pipeline ([Attention & Working Memory Papers](https://scholar.google.nl/citations?user=IkEbg-0AAAAJ&hl=en))

1. Reconstruct CAIPI / bidscoiner

#### Anatomical
1. Modify MP2RAGE: This makes the very noise background of the uni-image black ([TVM openfmritoolbox](https://github.com/TimVanMourik/OpenFmriAnalysis/tree/master)).
- Recommended upgrade: Skullstripping (and segmentation) with Nighres
1. Freesurfer recon-all
`recon-all -i $T1Path -subjid 'ses-01' -cw256 -all -parallel -hires`

1. Crop to Occipital Cortex (done manually, for better realignment)
2. Create Retinotopy from Atlas

#### Functional 
1. Realignment (we right now use SPM realign)
2. Bias Correct

#### Surface+Functional
We need to align functional surface + anatomical in same space. We also want to coregister the boundaries of WhightMatter(WM) and Gray Matters(GM) to later generate the layers

1. Align Surface & Functional ([TVM toolbox](https://github.com/TimVanMourik/OpenFmriAnalysis/tree/master))
2. Boundary Based Registration
3. Recursive Boundary Registration ([TVM toolbox](https://github.com/TimVanMourik/OpenFmriAnalysis/tree/master)) - minor changes only for me, at least visually. Would be interesting to inspect the laminar profiles with and without.


### Layer Analysis
There are multiple different ways to do layer analyses. Renzo Huber has a [list of software](https://layerfmri.com/2018/01/04/layer-fmri-software-in-the-field/) on his blog.
Here is how we right now do it:

1. (Optional): Weight your functional activations with some localizer t-values
2. Move the anatomical ROIs to functional space & select topN voxels as a 0/1 binary mask
3. LayerPipeline, use TVMs toolbox to extract layers. See his thesis / https://github.com/TimVanMourik/OpenFmriAnalysis/blob/master/Interface/LaminarAnalysis/tvm_layerPipeline.m - this extracts the layers. It is right now recommended to only use 5 layers to reduce ringing artefacts in the spatialGLM step (see TVMs plos one paper)
4. Create Designmatrices for different Conditions
5. Generate Timecourses & analyze them similarly to ERP (EEG) analyses
