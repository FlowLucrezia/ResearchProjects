---
tags:
  - groups
  - positive_emotions
  - decision_making
  - anxiety
  - physiology
  - synchronization
  - interpersonal_synchrony
  - affect
  - emotion
  - dyadic
  - GSR
  - skin_conductance
  - HR
  - MdRQA
  - methodology
  - iSAT
  - theory
  - experiment
  - report
  - ECG
  - IBI
  - HRV
  - joint_action
  - coupling
---
DOI: 10.1111/psyp.13857

[Gordon, I., Wallot, S., & Berson, Y. (2021). Group‐level physiological synchrony and individual‐level anxiety predict positive affective behaviors during a group decision‐making task. _Psychophysiology_, _58_(9), e13857.](https://onlinelibrary.wiley.com/doi/pdfdirect/10.1111/psyp.13857)

## Key Notes
- Effects of physiological synchrony on positive affective behavior were particularly strong at the group level but nonsignificant at the individual and dyadic levels
- Heart rate and electrodermal synchronization showed opposite effects on group members' display of affective behavior
- group-level EDA synchrony was a negative predictor of affective synchrony, whereas group-level BPM synchrony was a positive predictor of affective behavior
- Trait anxiety moderated the relationship between physiological synchrony and affective behavior, perhaps due to social uncertainty, while social phobia did not have a moderating effect
## Methods
### Physiological Measures

> An electrocardiogram (ECG) was obtained for every participant using a modified lead II configuration. The impedance cardiogram, which provides respiratory data for the analysis of IBI, was obtained using the standard tetrapolar electrode system (Sherwood et al., 1990). Electrodermal activity (measured in microsiemens [μS]) was collected via two disposable Ag-AgCl electrodes, both placed on the palm of the participant's nondominant hand. EDA values were outputted from the MindWare EDA analysis software as the mean skin conductance level recorded at 2 Hz. All recorders for the physiological signals are transmitted synchronously and wirelessly to a laptop computer in the control room adjacent to the lab room, with a sampling rate of 500 Hz.

### ECG Processing

> Each participant's ECG signal was visually examined and analyzed in the MindWare Technologies HRV application software (v3.1.4). Visual inspection and manual editing of the data were completed by trained graduate students to ensure the proper removal of artifacts and ectopic beats (Nabil & Reguig, 2015; Peltola, 2012). The signal was amplified by a gain of 1,000 and filtered with a Hamming windowing function. IBIs were extracted from the ECG recording. As IBI data usually differ in terms of number of data points between participants due to differences in the frequency of heart beats, they were transformed to BPM signals to obtain time series of equal rate for each participant. BPM series were oversampled to retain the full variability of the dynamics of the IBIs to increase the sensitivity of recurrence analysis (Wallot et al., 2013). The resulting physiological time series used for the following analyses are for epochs of 500 milliseconds.

### EDA processing

>Each participant's EDA signal was again examined visually and analyzed in the MindWare Technologies EDA application software (v3.1.4). When unusual peaks or sudden, unreasonable drops in the data were found, linear spline interpolation was used to replace the corrupted portions of the signal, limited to a maximum of 5% of each individual's data. We used a rolling filter set for a block size of 500 milliseconds. In the cases in which the editor identified an unusual peak or a drop for more than 5% of the data or in the case of a complete loss or flat line of the data, the participant's EDA signal was not used in the final analysis. The outputted physiological time series for following analyses were for epochs of 500 milliseconds

### Physiological Synchrony
> We used MdRQA (Wallot, Roepstorff, et al., 2016) to calculate the different synchrony measures for the EDA and BPM data. MdRQA was particularly suited for the analysis of the coupling of physiological time series in the present study for two reasons. First, recurrence-based analyses are extremely robust to outliers, heterogeneous variance over time, and nonstationarity (Marwan et al., 2007), which are common features of extended physiological recordings. Second, MdRQA provides a coherent analysis framework analyzing multivariate signals of different dimensionality, particularly the simultaneous coupling of more than two time series (Wallot, Roepstorff, et al., 2016).

*come back to revisit MdRQA protocol*