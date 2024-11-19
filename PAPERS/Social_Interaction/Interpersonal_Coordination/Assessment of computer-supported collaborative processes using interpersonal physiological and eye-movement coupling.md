---
tags:
  - eye_movement
  - CSCL
  - iSAT
  - collaboration
  - process
  - dynamics
  - interpersonal_synchrony
  - interpersonal_coordination
  - physiology
  - gaze_steps
  - coupling
  - learning
  - information
  - groups
  - task_performance
  - methodology
  - theory
  - experiment
  - report
  - emotion
  - attention
  - arousal
  - ECG
  - HR
  - IBI
  - SCR
  - GSR
  - CRQA
  - multimodal
  - HF_HRV
  - conflict
  - coordination
  - synchronization
  - empathy
  - joint_action
  - skin_conductance
---
DOI 10.1109/ACII.2013.26

[Chanel, G., Bétrancourt, M., Pun, T., Cereghetti, D., & Molinari, G. (2013, September). Assessment of computer-supported collaborative processes using interpersonal physiological and eye-movement coupling. In _2013 Humaine Association Conference on Affective Computing and Intelligent Interaction_ (pp. 116-122). IEEE.](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6681417&casa_token=9UIq6AohMaYAAAAA:HVMKaewKXLacad-iBXFscedQHa5nJnc7r61BwSYDkPWyOyfJ7hfglSJrVur1QweLl2i_OnLa&tag=1)

### Physiological Activity

> The physiological activity of the collaborators was recorded using two daisy-chained Biosemi Active II systems (P1 and P2, Fig. 1). Peripheral physiological signals were chosen based on their relationship with emotional and cognitive processes. Skin temperature and skin conductance (an index of physiological arousal) were obtained by placing sensors on the proximal phalanges of the hand. Blood volume pulse, a relative measure of blood pressure, was obtained by finger plethysmography. The Biosemi CMS/DRL reference electrodes were positioned on the hand hypothenar surface. All these sensors were attached to the non-dominant hand of the participants to reduce noise contamination due to keyboard typing and mouse movement. A belt was attached around the abdomen of the participants to measure respiration amplitude. Finally, a electro-cardiogram (ECG) was recorded. All physiological signals were recorded at a sampling frequency of 512 Hz.

### ECG Processing

![[Pasted image 20241119113258.png]]

> The transformation proposed by [22] was applied to have a coupling index that follows a normal distribution. Weighted coherence has the advantage of separating the shared variance of two time series among the chosen frequency bands of interest. This is particularly useful for heart rate variability analysis since it is known to be composed of three main periodic components [23]: a high frequency (HF) component [0.15Hz - 0.4 Hz], a low frequency (LF) component [0.05 Hz - 0.15 Hz], and a very low frequency (VLF)  component [0.003 Hz - 0.05 Hz]. The Welch’s method was employed to compute the power spectral density of the signals with a time window of 5 min and half overlap. The ECG was first resampled at 256 Hz and a band-pass filter between 0.05 Hz and 40 Hz was applied to remove noise in the signal. The ECG peaks were identified using the PanTompkins algorithm [24] and IBI (Inter-Beat Intervals) were computed by measuring the time elapsed between all pairs of consecutive peaks. From these unevenly spaced time series the final IBI time series were obtained by interpolation at 4 Hz using the algorithm detailed in [25]. This interpolation resulted in two synchronous IBI time series for each dyad (i.e. one foreach dyad member) from which the  coupling indices RIBI,CIBI(HF), CIBI(LF) and CIBI(VLF) were computed. 

### Skin Conductance Processing
> The skin conductance and temperature signals were filtered using a moving average window of 0.5 sec. RSCR and RTemp were than computed to measure skin conductance and temperature coupling


![[Pasted image 20241119113555.png]]

![[Pasted image 20241119113620.png]]