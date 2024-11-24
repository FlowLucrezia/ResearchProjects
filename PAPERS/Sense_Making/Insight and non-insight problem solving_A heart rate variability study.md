---
tags:
  - insight
  - problem_solving
  - HRV
  - HR
  - cardiac_activity
  - physiology
  - methodology
  - iSAT
  - experiment
  - consciousness
  - memory
  - agency
  - theory
  - emotion
  - attention
  - affect
  - autonomic
  - polyvagal
  - executive_function
  - vmHRV
  - task_complexity
  - ECG
  - creativity
  - metacognition
  - speed_accuracy
  - process
  - task_performance
---

[Stuyck, H., Demeyer, F., Bratanov, C., Cleeremans, A., & Van den Bussche, E. (2024). Insight and non-insight problem solving: A heart rate variability study. _Quarterly Journal of Experimental Psychology_, _77_(7), 1462-1484.](https://journals.sagepub.com/doi/abs/10.1177/17470218231202519)

### Physiological Data Processing

> The Kubios HRV software was used to preprocess the ECG data (Tarvainen et al., 2020). We used the automatic artefact correction algorithm of Kubios to correct for potential artefacts in the IBI time series (e.g., ectopic beats, and missed and extra beats). All detected artefacts were subsequently replaced with IBIs based on cubic spline interpolation. In addition, we applied a visual inspection of the ECG signal to identify unstable recording epochs, missed r-peaks, and missed artefacts by an automatic correction algorithm. In case an artefact was detected, a manual correction was applied. We only retained data that were minimally 95% noise-free and had a maximum of 5% corrected IBIs.

> To synchronize the course of the experiment programmed in PsychoPy with the ECG signal, we used the Nexus trigger interface to send triggers from PsychoPy to the ECG recording software (i.e., BioTrace+), marking the intervals of interest (i.e., baseline, solution search, and recovery).

 > To detect the r-peaks in the ECG signal, the Kubios HRV software uses a QRS-detection algorithm based on the Pan-Tompkins algorithm (see Tarvainen et al., 2020, for an in-depth explanation). After that, the IBIs were calculated by determining the time interval between two r-peaks for the ECG signal (see Fig. 2 for an example). To correct potential artifacts in the IBI time series, we used the automatic artifact correction algorithm of Kubios. This algorithm uses the distribution of the differences between consecutive IBIs to estimate a time-varying threshold (i.e., threshold changes depending on location in the IBI time series) to identify ectopic beats. To detect missed and extra beats, the time-varying threshold is determined based on the distribution of the differences between the IBIs and a local, median IBI (see Lipponen & Tarvainen, 2019, for the algorithm and decision rule). All detected artifacts are subsequently replaced with IBIs based on cubic spline interpolation. Lastly, Kubios deploys a detrending procedure to accommodate the non-stationarity of the IBI time series by defining an a priori smoothing parameter (cut-off frequency 0.035 Hz; see Tarvainen et al., 2002).

> Additionally, all ECG signals were visually inspected for abnormal ECG signals, unstable recording epochs, missed r-peaks, and missed artifacts by the algorithms that might influence the vmHRV data (e.g., supraventricular extrasystole; see Kumral et al., 2019 for a similar procedure). In case of abnormalities, we applied a manual correction to the ECG signal (e.g., marking noisy ECG epochs as to-be-excluded noise epochs and/or adding missing r-peaks). For all ECG recording intervals (i.e., baseline, solution search, and recovery), we only accepted ECG recordings consisting of at least 95% noise-free data (i.e., clear and distinct ECG wave morphology) and no more than 5% corrected IBIs in that noise-free data. For example, a baseline ECG recording of 300s could not include more than 15s of noise epochs (i.e., an epoch with an uninterpretable ECG wave morphology).

 >  As the 5min baseline ECG recording is vital for the statistical analysis of the trait vmHRV and the resource-dependent vmHRV, baseline ECG recordings that violated these above percentages (i.e., min. 95% noise-free data and max. 5% corrected IBIs) led to the exclusion of one participant (see participant section). To create the solution search and recovery intervals over which RMSSD was calculated, we merged the time intervals of the individually correctly solved CRA word puzzle trials for each solution type. This led to four RMSSD observations per participant (i.e., solution search insight, solution search non-insight, recovery insight, and recovery non-insight). The merged _solution-search_ interval consisted of a series of time intervals with differing lengths. This is because CRA word puzzles took between 1s and 30s to be solved. The merged _recovery_ interval always consisted of a series of time intervals of 10s, as the recovery time interval after each trial had a fixed length of 10s. The minimum _solution search_ and _recovery_ interval length deemed acceptable for assessing RMSSD was 10s. Previous research (e.g., Munoz et al., 2015) has shown that RMSSD calculated with a 10s ECG recording gives a reliable approximation of the RMSSD obtained with a 5min ECG recording. Based on this minimum required interval length, we refrained from calculating RMSSD for the insightful _solution search_ of one participant. 
 >  
 >  Next, similar to the baseline ECG recording, we determined the percentage of noise-free data and the percentage of corrected IBIs in the noise-free data. If these percentages were below 95% and above 5%, respectively, we refrained from calculating the RMSSD value but retained the participant. This led to an additional omission of five RMSSD values of five different participants. We note that for the _solution search_ and _recovery_ intervals below 30s all ECG data were 100% noise-free without corrected IBIs. This is important, as for such short intervals with a low number of IBIs which can be used to calculate RMSSD, additional missing/erroneous ECG data would be detrimental to the valid estimation of RMSSD. Finally, we used Tukey's (1977) method (see participant section for explanation) to identify severely outlying RMSSD observations in the four different interval types (i.e., solution search insight, solution search non-insight, recovery insight, and recovery non-insight; see Kumral et al., 2019 for a similar procedure). No RMSSD observations were considered as outlying based on this method. Table 1 depicts the percentage of noise-free data, the percentage of corrected IBIs, and the number of excluded RMSSD observations for each interval type.