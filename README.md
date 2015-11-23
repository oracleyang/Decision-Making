# Decision-Making via Wearable Biosensors

## Concepts


- Decision-making and stress / cognitive resources are limited
  - Psychology research considers cognitive resources to be limited \cite{Hockey1997}. 
  
> A higher cognitive load can "reduce performance goals" or impose other "behavioral and physiological cost".

- Implicit bias and IAT 
  - implicit bias is bad
  - can use IAT to characterize the bias
  - need to justify: tying implicit bias and cognitive load together
- Physiological data and machine learning
  - Wearable sensors can stream physiological signals with rich information. Through calibration then classfication, physiological signals can be related to the level of cognitive workload. Heart rate and skin conductance are such signals that wearble sensors like Empatica E4 provide. 


_Main Idea:_ use physiological data to classify user workload, so as to mitigate the effects of implicit bias in decision-making processes.

## Hypotheses 

- __H0:__ Physiological signals are “different” under H/L workload induced by n-back.
- __H1:__ Decision-making quality is different under H/L workload (by looking at the MouseTracker data)
- __H2:__ to be continued



## Code

- [bucknell-hci/flyloop](https://gitlab.bucknell.edu/bucknell-hci/flyloop)
  - the physiological computing framework that collects, processes and classfifies data.
- [n-back](https://gitlab.bucknell.edu/xp002/n-back)
  - the working memory stressor that involves staring at picture stimuli.
- [empatica_connect](https://gitlab.bucknell.edu/xp002/empatica_connect)  
  - the Android application that
    - get data via bluetooth low energy from Empatica E4
    - send data to FlyLoop via mqtt messages.
- [mouse-tracker-matlab](https://gitlab.bucknell.edu/xp002/mouse-tracker-matlab)
  - MATLAB code from MouseTracker's example folder
  - this repo is not useful; compiling MATLAB into a JAR is not worth the trouble
  - MATLAB code has been manually translated into Java and included in `dm_task` repository.
- [dm_task](https://gitlab.bucknell.edu/xp002/mouse-tracker-matlab)
  - decision-making tasks
    - primary task is to click pictures / make decisions on MouseTracker (see below)
    - secondary task is digit-recall 
  
[__MouseTracker__](http://mousetracker.jbfreeman.net): non-opensource, free software developed by John Freeman.  

## Devices 

- Empatica E4
  - the wrist band
  - crater, USB cord, extra electrodes and the red box
  - for physiological data collection of course
- Professor Peck's Android phone
  - always turn on Wi-Fi and Bluetooth
- [Optional] get a Windows computer
  - MouseTracker needs to run on Windows



## Network dependency

- `mqtt.bucknell.edu` (134.82.56.50). Maintained by Professor Marchiori. 
- publish / subscribe at various points 


## Experiment

1. Set-up: wire up the subject, check network connections
1. Calibration: do n-back task while FlyLoop builds the model
2. Experimentation: do MouseTracker with digit recall task


## More resources

- Presentations
  - Susquehanna Valley Undergraduate Research Symposium
    - Oral presentation: ppt 
  - Bucknell Engineering Research Symposium
    - Poster presentation: pdf
- Write-ups
  - The original proposal @ google drive
  - Hypotheses @ google drive
  - Schemas @ google drive
- bibtex dump
  - physiological computing overview
  - similar HCI papers
  - stress and other psychology stuff
  - misc: mousetracker, etc.
- Annotated bibliography dump


_Xiaoying Pu 2015_
