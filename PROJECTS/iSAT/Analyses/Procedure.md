
## Collection

1. Placement
	1. EDA/GSR
		1. Non-dominant hand
		2. Thenar and hypothenar eminences on their palms (see Dawson 2016/2017 paper cited in @dindarWhatDoesPhysiological2020)
		3. Last two fingers, e.g., @tanRolePhysiologicalCues2014
	2. ECG
		1. 3-lead
			1. below collarbones and below lower left ribs
		2. Multi-lead?
2. Baseline
	1. 3-5 minutes as the norm
	2. relaxing, looking at nature background
3. Synchronization
4. ***
## Processing
#### Skin Conductance

1. Sampling and Downsampling
	1. Often sampled at 128Hz, e.g., @tormanenAffectiveStatesRegulation2023
	2. Downsampling usually to 32 or 16Hz
2. Check for outliers and abnormalities
	1. Linear spline interpolation, <5% of data; e.g.,  @gordonGrouplevelPhysiologicalSynchrony2021
3. Low-pass butterworth filter
	1. frequency 1, order 5
4. *PEAK DETECTION* - SCL vs SCR
	1. Continuous decomposition analysis
		1. Ledalab commonly used for analyses, e.g., @jarvenojaCollaborativeLearningDesign2020
		2. Threshold of 0.05 μS
	2. Trough-to-Peak method
		1. Minimum amplitude of .05 μS


##### EDA Resources:
- [[A collaborative learning design for promoting and analyzing adaptive motivation and emotion regulation in the science classroom]]
- [[Affective states and regulation of learning during socio‐emotional interactions in secondary school collaborative groups]]
- [[Assessment of computer-supported collaborative processes using interpersonal physiological and eye-movement coupling]]
- [[Breathe Easy EDA_A MATLAB toolbox for psychophysiology data management, cleaning, and analysis]]
- [[Deep structures of collaboration_Physiological correlates of collective intelligence and group satisfaction]]
- [[Group‐level physiological synchrony and individual‐level anxiety predict positive affective behaviors during a group decision‐making task]]
- [[Learners’ Linguistic Alignment and Physiological Synchrony_Identifying Trigger Events that Invite Socially Shared Regulation of Learning]]
- [[Physiological Synchrony in Interpersonal Agency_A Case Study on Collaborative Problem Solving of a Group of Year 7 Students]]
- [[Physiological evidence of interpersonal dynamics in a cooperative production task]]
- [[Sympathetic arousal commonalities and arousal contagion during collaborative learning_How attuned are triad members]]
- [[The role of physiological cues during remote collaboration]]
- [[What does physiological synchrony reveal about metacognitive experiences and group performance]]
- [[What multimodal data can tell us about the students’ regulation of their learning process]]

#### Cardiac Activity

1. Sampling and Downsampling
	1. Often sampled at 128Hz
	2. Downsampling usually to 32 or 16Hz
2. Check for outliers and abnormalities
3. Band-pass filter to remove noise, e.g., @edwardsEngagedFrustratedDisambiguating2017
	1. High-band: 0.05 Hz 
	2. Low-band: 35 or 40 Hz
	3. Gain: 1000 Hz
5. *PEAK DETECTION*
	1. PanTompkins algorithm
6. IBI calculation and alignment

##### HR Resources:
- [[Assessment of computer-supported collaborative processes using interpersonal physiological and eye-movement coupling]]
- [[Autonomic nervous system activity in emotion_A review]]
- [[Bridging the gap between emotion and joint action]]
- [[Deep structures of collaboration_Physiological correlates of collective intelligence and group satisfaction]]
- [[Engaged or Frustrated_Disambiguating Emotional State in Search]]
- [[Group‐level physiological synchrony and individual‐level anxiety predict positive affective behaviors during a group decision‐making task]]
- [[Heart rate variability (HRV) as a way to understand associations between the autonomic nervous system (ANS) and affective states_A critical review of the literature]]
- [[Interpersonal physiological synchrony predicts group cohesion]]
- [[Insight and non-insight problem solving_A heart rate variability study]]
- [[Multifractal Analysis of Heart Rate Dynamics as a Predictor of Teammate Trust in Human-Machine Teams]]

## Synchronization

#### Signal Alignment
- ***

#### Time Series Analysis
- CRQA
- MdRQA
	- REC% = ratio of time points with recurrence to all time points
	- DET = ratio of adjacent recurrence time points to all recurrence time points
	- DL = average length of adjacent recurrence time points
	- MDL =length of longest adjacent time points with recurrence

##### Analysis Resources:
- [[Group‐level physiological synchrony and individual‐level anxiety predict positive affective behaviors during a group decision‐making task]]
- [[Interpersonal physiological synchrony predicts group cohesion]]
- [[What does physiological synchrony reveal about metacognitive experiences and group performance]]