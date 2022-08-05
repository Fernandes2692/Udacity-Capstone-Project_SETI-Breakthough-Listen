# Udacity-Capstone-Project_SETI-Breakthough-Listen

### SETI Breakthrough Listen - E.T. Signal Search : Find extraterrestrial signals in data from deep space

#### “Are we alone in the Universe?”

### Table of Contents
1. [Introduction](#introduction)
2. [Project Motivation](#project-motivation)
3. [Data Description](#data-description)
4. [Files](#files)
5. [Instructions](#instructions)
6. [Licensing and Acknowledgements](#licensing-and-acknowledgements)

## **Installations**

· Pandas · NumPy · Matplotlib · plotly · Seaborn · Sklearn · tensorflow · keras 

## **Introduction**
"*It’s one of the most profound—and perennial—human questions. As technology improves, we’re finding new and more powerful ways to seek answers. The Breakthrough Listen (BL) team at the University of California, Berkeley, employs the world’s most powerful telescopes to scan millions of stars for signs of technology (technosignatures). This project was initally made public as a competition on Kaggle, for those who are interested to help interpret the signals they pick up.*

*The Listen team is part of the Search for ExtraTerrestrial Intelligence (SETI) and uses the largest steerable dish on the planet, the 100-meter diameter Green Bank Telescope (GBT). Like any SETI search, the motivation to communicate is also the major challenge. Humans have built enormous numbers of radio devices. It’s hard to search for a faint needle of alien transmission in the huge haystack of detections from modern technology.*

*Current methods use two filters to search through the haystack. First, the Listen team intersperses scans of the target stars with scans of other regions of sky. Any signal that appears in both sets of scans probably isn’t coming from the direction of the target star. Second, the pipeline discards signals that don’t change their frequency, because this means that they are probably nearby the telescope. A source in motion should have a signal that suggests movement, similar to the change in pitch of a passing fire truck siren (Doppler Effect). These two filters are quite effective, but we know they can be improved. The pipeline undoubtedly misses interesting signals, particularly those with complex time or frequency structure, and those in regions of the spectrum with lots of interference.*" https://www.kaggle.com/c/seti-breakthrough-listen  
</br>

<p align="center" width="100%">
   <img src="radio-telescope-2.jpg" width="600">
</p>


## **Project Motivation**

Breakthrough Listen (BL) is a ten-year initiative to search for signatures of technologically capable life beyond Earth via radio and optical observations of the local Universe.

In this project, I use the data science skills I have learnt throughout the Udacity nanodegree so far, to help identify anomalous signals in scans of Breakthrough Listen targets. </br> 

**NB:** Because there are no confirmed examples of alien signals to use to train machine learning algorithms, the team included some simulated signals (that they refer to as “needles”) in the haystack of data from the telescope. They have identified some of the hidden needles so that you can train your model to find more. The data consist of two-dimensional arrays, so there may be approaches from computer vision that are promising, as well as digital signal processing, anomaly detection, and more. 

The task was to predict whether the spectrograms contained signals from E.T or not. The evaluation metric was AUC. There were 60,000 training samples and 39,995 test samples, 10% of which were positive. Each sample is a set of 6 spectrograms, or a “cadence”. They are continuous in time, but the first, third, and fifth are referred to as “on target” signals that come from the target star, while the rest are “off target” signals from the nearby stars. If there is a pattern in “on target” and no pattern in “off target”, then the signal is a candidate signature of extraterrestrial technology (a positive sample)! If the pattern is also seen in “off target”, it should be a human-generated artifact (a negative sample). 

## **Data Description**

:alien: FilterBank Format : 
2D Arrays of intensity as a function of frequency and time, accompanied by headers containing metadata such as the direction the telescope was pointed in, the frequency scale.  </br>
:alien: Snippets : 
Numpy arrays consisting of small regions of the spectrograms .  </br>
:alien: Technosignatures : 
Technosignature or technomarker is any measurable property or effect that provides scientific evidence of past or present technology. Technosignatures are analogous to the biosignatures that signal the presence of life, whether or not intelligent.  </br>
:alien: Cadence Snippets : 
Consider three nearby stars A , B and C to our primary target. Isolation of candidate technosignatures from RFI happens by alternating observations of primary target star with observations of three nearby stars . 5 minutes on star “A”, then 5 minutes on star “B”, then back to star “A” for 5 minutes, then “C”, then back to “A”, then finishing with 5 minutes on star “D”. One set of six observations (ABACAD) is referred to as a “cadence”.  </br>
:alien: Haystack : 
Thousands of cadence snippets put together is referred to as haystack  </br>
:alien: Needle Signal /Target : 
The goal of this problem is to identify the hidden needle signals in this haystack .

## **Files**

**train/** - a training set of cadence snippet files stored in numpy float16 format (v1.20.1), one file per cadence snippet id, with corresponding labels found in the train_labels.csv file. Each file has dimension (6, 273, 256), with the 1st dimension representing the 6 positions of the cadence, and the 2nd and 3rd dimensions representing the 2D spectrogram. </br>
**test/** - the test set cadence snippet files; you must predict whether or not the cadence contains a "needle", which is the target for this competition </br>
**sample_submission.csv** - a sample submission file in the correct format </br>
**train_labels** - targets corresponding (by id) to the cadence snippet files found in the train/ folder

## **Instructions**

You will need to use a Kaggle kernal to run the code. 

- Download the notebook.
- Sign in to Kaggle (create an account if you don't have one) 
- In Kaggle, go to the homepage, and select the <> code from the panel of options on the left hand side.  
- Click + New Notebook and then click file --> import new notebook and upload this notebook. 
- On the right hand side, click + Add data --> then select Competition Data and search for SETI Breakthrough Listen - E.T Signal Search. Click add. 
- Next, run all to execute the python script


## **Licensing and Acknowledgements**

The Breakthrough Listen science and engineering effort is headquartered at the University of California, Berkeley SETI Research Center. The Breakthrough Prize Foundation funds the Breakthrough Initiatives which manages Breakthrough Listen. The Green Bank Observatory is supported by the National Science Foundation, and is operated by Associated Universities, Inc. under a cooperative agreement. For an extensive overview of the Breakthrough Listen work, check out UCBerkeley's github repository: https://github.com/UCBerkeleySETI/breakthrough/tree/master/GBT
