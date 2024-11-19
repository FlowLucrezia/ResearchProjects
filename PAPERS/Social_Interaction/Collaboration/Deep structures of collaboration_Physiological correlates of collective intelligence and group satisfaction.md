---
tags:
  - team
  - teams
  - groups
  - satisfaction
  - collaboration
  - physiology
  - synchronization
  - dynamics
  - interaction
  - feedback
  - rapport
  - GSR
  - emotion
  - positive_emotions
  - facial_expressions
  - skin_conductance
  - HR
  - cardiac_activity
  - joint_action
  - arousal
  - reactivity
  - valence
  - affiliation
  - theory
  - methodology
  - iSAT
  - experiment
  - report
  - DTW
  - interpersonal_synchrony
  - empathy
---
DOI: http://dx.doi.org/10.1145/2998181.2998250

[Chikersal, P., Tomprou, M., Kim, Y. J., Woolley, A. W., & Dabbish, L. (2017, February). Deep structures of collaboration: Physiological correlates of collective intelligence and group satisfaction. In _Proceedings of the 2017 ACM conference on computer supported cooperative work and social computing_ (pp. 873-888).](https://dl.acm.org/doi/pdf/10.1145/2998181.2998250)

### Procedure

> Each session lasted approximately 30 minutes. Members of each dyad were seated in different rooms. None of the participant pairs knew each other before the experiment. After completing a pretest survey, they were instructed to wear the E4 2 wristbands on their non-dominant hand and relax for two minutes to obtain a baseline in EDA and heart rate. After that, participants initiated the video conference call with their partner. Participants then logged onto the Platform for Online Group Studies (POGS), a web  rowser based platform that supports synchronous multiplayer interaction, to complete the Test of Collective Intelligence (TCI) with the other research participant [27, 28, 95]. The TCI contained six tasks ranging from 2 to 6 minutes each, and instructions were displayed before each task for 15 seconds to 1.5 minutes. At the end of the test, they were instructed to sign off the videoconference and proceed to the post-test survey, which was completed independently. Participants were then compensated and debriefed.

### Electrodermal Activity

>We recorded EDA using the E4 wristband with a sample rate of 4 samples per second (4Hz). The resulting signals have two components - tonic (skin conductance level) and phasic (skin conductance response). The tonic component changes gradually over time, approximates a person’s baseline and is not the result of stimuli. The phasic component contains quickly changing peaks that typically occur in response to shortterm events or environmental stimuli. We separate phasic EDA from tonic EDA using Continuous Decomposition Analysis [8], and use only phasic EDA (pEDA) henceforth, since we’re only interested in participant task responses and not their baselines.

> We normalized pEDA signals using z-score of each sample to enable inter-participant comparison. The signals obtained were very noisy and so we applied a Simple Moving Average filter (window size = 5 seconds = 5 x 4 samples, empirically determined) to smooth the signals, and name these physiological response signals.

### Heart Rate

> We measured HR to assess each participant’s level of cardiovascular arousal during the session. Since different people have different resting heart rates, to enable interparticipant comparison, we normalized the HR data by dividing it by its mean (assuming mean to be an estimate of the baseline) and multiplying it by 100. No smoothing was required for HR signals, since HR is the number of heartbeats averaged for 1 minute. We obtained six task HR signals that are physiological response signals representing a participant’s percentage change in HR over time, from his/her mean HR.
### Physiological Synchrony

> We assessed physiological synchrony by recording facial expressions, electrodermal activity (EDA), and heart rate (HR) of each individual in the dyad throughout their interaction during the TCI. Synchrony in facial expressions can capture shared experience or mimicry [79] over time. Synchrony in HR and EDA captures shared arousal during periods of stress, excitement, or high levels of engagement [2, 73, 76]. We processed the individual responses into physiological  response signals, sequences of response scores over time in the study, and then calculated distances between the series of scores (or signals) of each individual in a dyad using Dynamic Time Warping. 

