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

### Useful Findings

> CI was neither significantly correlated with synchrony in pEDA nor with synchrony in heart rate
> Group satisfaction was positively associated with high levels of pEDA synchrony (r = .33, p = .04). In other words, when both members of a dyad exhibited similar levels of electrodermal activity, they later reported a higher level of satisfaction with the interaction with their partner. However, group satisfaction had no significant relationship with synchrony in facial expressions and heart rate. Finally, pEDA and heart rate were positively related to one another (r = .34, p = .02). Dyads that had higher synchrony in their heart rate also had higher synchrony in electrodermal activity. Only synchrony in electrodermal activity was significantly associated with group satisfaction.

>Group satisfaction was also indirectly affected by the group composition variables we examined. Similar to collective intelligence, sex and ethnic diversity had positive indirect effects on group satisfaction, but via synchrony in EDA, a signal of shared arousal in the group. However, age diversity, measured by distance, also had a positive indirect effect on group satisfaction via synchrony in EDA. That is, groups composed of members with a greater age gap demonstrated a high level of synchrony in EDA, which was positively associated with group satisfaction. It is possible that a greater age gap between members created a noncompetitive, caring environment for group members; however, without the greater attentiveness engendered via facial expression synchrony, this did not translate into the group’s collective intelligence. Finally, social perceptiveness indirectly increased group satisfaction via synchrony in EDA, albeit to a very small degree.

> heart rate synchrony turned out to be a less sensitive measure of synchrony of arousal for the present study

 - limitations of wristbands with an averaged out measure of HR vs ECG signals... sensitivity 


## Methods

### Procedure

> Each session lasted approximately 30 minutes. Members of each dyad were seated in different rooms. None of the participant pairs knew each other before the experiment. After completing a pretest survey, they were instructed to wear the E4 2 wristbands on their non-dominant hand and relax for two minutes to obtain a baseline in EDA and heart rate. After that, participants initiated the video conference call with their partner. Participants then logged onto the Platform for Online Group Studies (POGS), a web  rowser based platform that supports synchronous multiplayer interaction, to complete the Test of Collective Intelligence (TCI) with the other research participant [27, 28, 95]. The TCI contained six tasks ranging from 2 to 6 minutes each, and instructions were displayed before each task for 15 seconds to 1.5 minutes. At the end of the test, they were instructed to sign off the videoconference and proceed to the post-test survey, which was completed independently. Participants were then compensated and debriefed.

### Electrodermal Activity

>We recorded EDA using the E4 wristband with a sample rate of 4 samples per second (4Hz). The resulting signals have two components - tonic (skin conductance level) and phasic (skin conductance response). The tonic component changes gradually over time, approximates a person’s baseline and is not the result of stimuli. The phasic component contains quickly changing peaks that typically occur in response to shortterm events or environmental stimuli. We separate phasic EDA from tonic EDA using Continuous Decomposition Analysis [8], and use only phasic EDA (pEDA) henceforth, since we’re only interested in participant task responses and not their baselines.

> We normalized pEDA signals using z-score of each sample to enable inter-participant comparison. The signals obtained were very noisy and so we applied a Simple Moving Average filter (window size = 5 seconds = 5 x 4 samples, empirically determined) to smooth the signals, and name these physiological response signals.

### Heart Rate

> We measured HR to assess each participant’s level of cardiovascular arousal during the session. Since different people have different resting heart rates, to enable interparticipant comparison, we normalized the HR data by dividing it by its mean (assuming mean to be an estimate of the baseline) and multiplying it by 100. No smoothing was required for HR signals, since HR is the number of heartbeats averaged for 1 minute. We obtained six task HR signals that are physiological response signals representing a participant’s percentage change in HR over time, from his/her mean HR.
### Physiological Synchrony

> We assessed physiological synchrony by recording facial expressions, electrodermal activity (EDA), and heart rate (HR) of each individual in the dyad throughout their interaction during the TCI. Synchrony in facial expressions can capture shared experience or mimicry [79] over time. Synchrony in HR and EDA captures shared arousal during periods of stress, excitement, or high levels of engagement [2, 73, 76]. We processed the individual responses into physiological  response signals, sequences of response scores over time in the study, and then calculated distances between the series of scores (or signals) of each individual in a dyad using Dynamic Time Warping. 

> We used Dynamic Time Warping (DTW) [11] to calculate synchrony between facial expressions, heart rate, and EDA of partners in a dyad. DTW is an algorithm for measuring similarity between two temporal sequences that vary in time and speed. Physiological response signals of each participant are also temporal sequences that are computed using the method described above. DTW provides the distance between the partners’ physiological response signals for each task, which are then summed across tasks to give the total distance. We operationalize synchrony as similarity of a physiological measure between the partners’ response signals of that measure. This similarity is calculated by subtracting the total distance from the total distance of the most different (largest total distance) dyad. Figure 2 shows an example of two signals - Signal A and Signal B that are different in length, time, and speed. DTW warps the time axis of these signals to find corresponding points between the two signals that optimally match. Figure 3 shows some of the matched corresponding points in signals A and B. A locality constraint in DTW is the maximum distance allowed between the matched corresponding points in the two sequences. The algorithm used to match the signals illustrated in figure D does not specify a locality constraint, which may or may not be always favorable.