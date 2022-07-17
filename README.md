# Udacity-Capstone-Project_SETI-Breakthough-Listen

## SETI Breakthrough Listen - E.T. Signal Search
## Find extraterrestrial signals in data from deep space

### “Are we alone in the Universe?”


It’s one of the most profound—and perennial—human questions. As technology improves, we’re finding new and more powerful ways to seek answers. The Breakthrough Listen team at the University of California, Berkeley, employs the world’s most powerful telescopes to scan millions of stars for signs of technology. Now it wants the Kaggle community to help interpret the signals they pick up.

The Listen team is part of the Search for ExtraTerrestrial Intelligence (SETI) and uses the largest steerable dish on the planet, the 100-meter diameter Green Bank Telescope. Like any SETI search, the motivation to communicate is also the major challenge. Humans have built enormous numbers of radio devices. It’s hard to search for a faint needle of alien transmission in the huge haystack of detections from modern technology.

Current methods use two filters to search through the haystack. First, the Listen team intersperses scans of the target stars with scans of other regions of sky. Any signal that appears in both sets of scans probably isn’t coming from the direction of the target star. Second, the pipeline discards signals that don’t change their frequency, because this means that they are probably nearby the telescope. A source in motion should have a signal that suggests movement, similar to the change in pitch of a passing fire truck siren. These two filters are quite effective, but we know they can be improved. The pipeline undoubtedly misses interesting signals, particularly those with complex time or frequency structure, and those in regions of the spectrum with lots of interference.

In this competition, use your data science skills to help identify anomalous signals in scans of Breakthrough Listen targets. Because there are no confirmed examples of alien signals to use to train machine learning algorithms, the team included some simulated signals (that they call “needles”) in the haystack of data from the telescope. They have identified some of the hidden needles so that you can train your model to find more. The data consist of two-dimensional arrays, so there may be approaches from computer vision that are promising, as well as digital signal processing, anomaly detection, and more. The algorithm that’s successful at identifying the most needles will win a cash prize, but also has the potential to help answer one of the biggest questions in science.

![](radio-telescope-2.jpg)


Acknowledgments

The Breakthrough Listen science and engineering effort is headquartered at the University of California, Berkeley SETI Research Center. The Breakthrough Prize Foundation funds the Breakthrough Initiatives which manages Breakthrough Listen. The Green Bank Observatory is supported by the National Science Foundation, and is operated by Associated Universities, Inc. under a cooperative agreement.

The project involved:
 - Loading and cleaning a smaller subset (~420MB) of a full dataset available (13.1GB): 
 
The Breakthrough Listen Search for Advanced Life:
1.1-1.9 GHz observations of 692 Nearby Stars 
 
[Data Downoload](http://seti.berkeley.edu/lband2017/downloads.html): 
 
1.1 million 3Hz hits from the 11 top ranking stars
(~420 MB)
