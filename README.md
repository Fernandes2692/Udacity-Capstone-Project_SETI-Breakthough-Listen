# Udacity-Capstone-Project_SETI-Breakthough-Listen

### SETI Breakthrough Listen - E.T. Signal Search : Find extraterrestrial signals in data from deep space

#### “Are we alone in the Universe?”


It’s one of the most profound—and perennial—human questions. As technology improves, we’re finding new and more powerful ways to seek answers. The Breakthrough Listen team at the University of California, Berkeley, employs the world’s most powerful telescopes to scan millions of stars for signs of technology (technosignatures). This project was initally made public as a competition on Kaggle, for those who are interested to help interpret the signals they pick up.

The Listen team is part of the Search for ExtraTerrestrial Intelligence (SETI) and uses the largest steerable dish on the planet, the 100-meter diameter Green Bank Telescope (GBT). Like any SETI search, the motivation to communicate is also the major challenge. Humans have built enormous numbers of radio devices. It’s hard to search for a faint needle of alien transmission in the huge haystack of detections from modern technology.

Current methods use two filters to search through the haystack. First, the Listen team intersperses scans of the target stars with scans of other regions of sky. Any signal that appears in both sets of scans probably isn’t coming from the direction of the target star. Second, the pipeline discards signals that don’t change their frequency, because this means that they are probably nearby the telescope. A source in motion should have a signal that suggests movement, similar to the change in pitch of a passing fire truck siren. These two filters are quite effective, but we know they can be improved. The pipeline undoubtedly misses interesting signals, particularly those with complex time or frequency structure, and those in regions of the spectrum with lots of interference. </br>

In this project, I use the data science skills I have learnt throughout the Udacity nanodegree so far, to help identify anomalous signals in scans of Breakthrough Listen targets. </br> 

**NB:** Because there are no confirmed examples of alien signals to use to train machine learning algorithms, the team included some simulated signals (that they refer to as “needles”) in the haystack of data from the telescope. They have identified some of the hidden needles so that you can train your model to find more. The data consist of two-dimensional arrays, so there may be approaches from computer vision that are promising, as well as digital signal processing, anomaly detection, and more. 

![](radio-telescope-2.jpg)



**Data Description**

Task: to look for technosignature signals in cadence snippets taken from the Green Bank Telescope (GBT). 


Files

**train/** - a training set of cadence snippet files stored in numpy float16 format (v1.20.1), one file per cadence snippet id, with corresponding labels found in the train_labels.csv file. Each file has dimension (6, 273, 256), with the 1st dimension representing the 6 positions of the cadence, and the 2nd and 3rd dimensions representing the 2D spectrogram.
**test/** - the test set cadence snippet files; you must predict whether or not the cadence contains a "needle", which is the target for this competition
**sample_submission.csv** - a sample submission file in the correct format
**train_labels** - targets corresponding (by id) to the cadence snippet files found in the train/ folder


The project involved:
 - Loading and cleaning a smaller subset (~420MB) of a full dataset available (13.1GB): 
 
The Breakthrough Listen Search for Advanced Life:
1.1-1.9 GHz observations of 692 Nearby Stars 
 
[Data Downoload](http://seti.berkeley.edu/lband2017/downloads.html): 
 
1.1 million 3Hz hits from the 11 top ranking stars
(~420 MB)


Acknowledgments

The Breakthrough Listen science and engineering effort is headquartered at the University of California, Berkeley SETI Research Center. The Breakthrough Prize Foundation funds the Breakthrough Initiatives which manages Breakthrough Listen. The Green Bank Observatory is supported by the National Science Foundation, and is operated by Associated Universities, Inc. under a cooperative agreement. 
