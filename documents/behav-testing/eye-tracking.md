---
layout: default
title: Eye Tracking
parent: Behavioral Testing 
nav_order: 4
---

# Eye Tracking at the DCCN

## How do I calibrate / use the eyetracker in the behavioural lab?

The Eyelink and eye-tracker is a useful tool for recording eye movements in your experiments. There are 3 critical components that enable the eyes to be tracked. These are:
1. An infrared light source that illuminates the eye and provides corneal reflection
2. A high speed video camera (taking up to 1000 samples of eye per second)
3. The EyeLink PC which receives the data from the camera.

In order to achieve data quality as high as possible procedures can be optimized. This includes: 
1. Participant setup
2. Camera setup
3. Calibration and validation.

### 1. Participant Set-Up

It is important to get the distances between participants’ eyes, camera and screen right. But also first of all ensure participants are seated comfortably. You can adjust the seat and / or table to achieve that. Participants’ eyes should be level with the top quarter of the screen. Check the Eyelink recommendations for the minimum / maximum distance between the eyes and camera / screen. Optimal camera-eye distance is between **40-70 cm on the setup used in Behavioural lab 1**. The ideal tracking distance is **50-55 cm**.

### 2. Camera Set-Up

The camera screw should be roughly aligned to the center of the monitor. You should also raise the Desktop Mount so that the top of the illuminator is as close as possible to the lower edge of the visible part of the monitor for maximum eye tracking range. The camera should be placed to the lower part of the screen. There are some recommendations of keeping it **20 cm away** from the screen. 

### 3. Calibration and Validation

There are several possible calibration types available. By default, Eyelink uses a nine-point calibration type (“HV9”), which is good for most of the eye tracking applications. **However, if a large calibration region is used, the “HV13” calibration type should be used for best calibration accuracy.**
After you run the calibration, check whether the crosses on the Eyelink computer look symmetrical. Often there might be a slight asymmetry in one of the upper corners. If that is the case, you may want to redo the calibration. Altogether it is best if (after validation) your accuracy of calibration is ‘good’ – try to strive towards that. It is worth having moments in your experiment where you can redo the calibration as the accuracy may decrease over time (e.g. with participant slightly changing their seating position etc).

## Other Tips and Tricks

-	Ask participant to look at the four corners of the screen when you have localized the pupil to make sure that the pupil is tracked in all locations. If not, adjust the contrast. 
-	Ask participant to cover the eye you have set to be tracking (if monocular) to make sure you are actually tracking the eye you set out to track.
-	It is recommended to do eye dominance tests and track the dominant eye. These are fast and simple. For example here is one:
    -	Extend one arm out, holding a finger of that hand in an upright position. 
    -	Keeping both eyes open and focused on a distant object, superimpose a finger on that object.
    -	Alternately close one eye at a time.
    -	The eye that keeps the finger directly in front of the object while the other eye is closed is the dominant eye.
-	Make sure that the background of your calibration screen matches the background of your main experiment. Having any difference in colour / contrast etc. could introduce inaccuracies or shifts in recorded eye position in the main experiment.
-	Start with illumination at the eyetracker set to 75%. If the pupil estimation does not work without decreasing the threshold below X, then change the illuminator power to 100%. 
-	If your stimuli are always presented in specific locations of the screen, then it may be wise to customize your calibration so as to include exactly those positions. 
-	Doing calibration (or at least validation) manually as opposed to automatically may increase the accuracy of the calibration.
-	Make sure participants are not wearing makeup.
-	It is best if participants wear no eye correction (contact lenses or glasses), so try to recruit participants with perfect sight. 

### Useful Links

Eyelink has useful documentation, both for programming and for setting up the eyetracker. That can be found [here](https://www.sr-research.com/support-options/learning-resources/)

### Code

See linked potentially useful code for programming with Eyelink. Here this is implemented via PsychoToolBox (MATLAB) interaction with Eyelink.
Functions:
-	[`EyelinkEnterSetup.m(el)`](https://drive.google.com/file/d/1sbnx45YlJ44-N3IBHkq7GMrTl7bscGxG/view?usp=drive_link)
    -	Determines whether the Eyelink is connected
-	[`et_transfer_edf.m(G)`](https://drive.google.com/file/d/1ie2M7jpfKH7XD8G1C6Demm3cGnyybRpo/view?usp=drive_link)
    -	edf is the file Eyelink produces with the eye data. This function moves this file to your folder. 
    -	Note that G.eyeFile in the function is the name of edf file you have given initially, and G.eyeDir is the directory you want to move it to (i.e. from the Eyelink computer to where you want the data saved)
-	[`et_eyelink_config.m(G)`](https://drive.google.com/file/d/1i-odIYP3snYjXN7p_F_llP1klAvnR0G1/view?usp=drive_link)
    -	This contains examples of how you can customize the options from Eyelink (e.g. different background colour, size of targets, type of calibration etc., etc.
-	To see exactly how the eyetracker and these functions are used in the context of a full experiment, see site on experimental code (PTB).

