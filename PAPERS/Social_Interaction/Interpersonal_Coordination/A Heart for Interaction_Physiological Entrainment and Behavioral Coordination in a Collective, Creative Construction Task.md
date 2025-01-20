---
tags:
  - HR
  - physiology
  - coordination
  - coordination_dynamics
  - dynamics
  - experiment
  - iSAT
  - CRQA
  - methodology
  - FYP
  - cardiac_activity
  - interaction
  - collaboration
  - communication
  - interpersonal_coordination
  - interpersonal_synchrony
  - synchronization
  - rapport
  - experience
  - cooperation
  - speech
  - joint_action
  - affordances
  - groups
  - dyadic
  - task_performance
  - structure
  - engagement
  - regulation
  - arousal
  - entrainment
---

[Fusaroli, R., Bjørndahl, J. S., Roepstoff, A., & Tylén, K. (2015). A Heart for Interaction: Physiological Entrainment and Behavioral Coordination in a Collective, Creative Construction Task. arXiv preprint arXiv:1504.05750.](https://pure.au.dk/ws/portalfiles/portal/96219349/pdf)

## Key Notes
- Uses CRQA on HR time series
	- extent and stability of coordination
		- RR and meanLine
- surrogate analysis performed, also compared individual vs group building
- speech and behavioral coordination related to experience/subjective outcomes, but not HR coordination
	- negative correlation between coordination and experience ... look at leader-follower and turn-taking dynamics rather than just the extent of coordination
		- To what extent is the coordination symmetrical?
		- refer to algorithm discussed with Ye and Jayci (number of peaks and area under DCRP curves)


## Findings
> Overall level of shared HR dynamics is lower in collective trials, the stability is the same across collective and individual trials, for real pairs, but lower for virtual pairs. This suggests that actual online collaboration has an impact on shared HR dynamics above and beyond simple task constraints: collaborative tasks involve not just similar individual levels of engagement (being equally physiologically aroused), but repeated, prolonged sequences of behavioral coordination which might entrain physiological dynamics (see also Study 2).
> 
> This hypothesis is further supported by the general increase in level and stability of shared HR dynamics over the course of collective but not individual trials; possibly as a function of coordinative routines being established. While the level of shared HR dynamics in collective constructions reaches individual constructions levels over the progression of trials, the stability even becomes significantly higher.

> The level of heart rate coordination (HR RR) was significantly related to the level of building and the stability of speech coordination (Build RR and Speech L): the higher the level of building coordination and the more stable the speech coordination, the higher the level of shared HR dynamics, with particularly substantial evidence in favor of the role of stable coordination (cf. Table 5 and Figure 5). The stability of heart rate coordination (HR L) was significantly and with substantial evidence related to speech coordination: the more frequent (RR) and stable (L) the speech coordination, the more stable the heart rate entrainment (cf. Table 5 and Figure 5).

> Self reported relatedness was significantly predicted by the stability of building and speech coordination: the more stable building and the less stable speech coordination, the higher the ratings. Self reported group competence was significantly predicted by the level of building coordination: the less building coordination, the higher the ratings (cf. Tables 6 and 7 and Figure 6). None of the HR predictors were significantly correlated with experience.

> The results suggest that behavioral coordination (building and speech) is a better predictor of the phenomenological experience of group relatedness and competence than shared HR dynamics. This supports the idea that emotions might be environmentally extended, and more specifically dependent on specific sustained patterns of social interactions (Colombetti & Krueger, 2014; Krueger, 2014). Curiously, HR does not correlate with experience at all. This suggests that in collaborative tasks – in which behavioral coordination is crucial – behavioral coordination mediates both physiological entrainment and experience. However, it should be noted that the connection between behavioral coordination and experience is not a trivial one: some of the indexes of interpersonal behavioral coordination are negatively related to experience. This negative correlation between coordination and experience has been previously observed in (Strang, et al., 2014; Wallot, et al., submitted) and might point to the complexity of coordination dynamics and their timescales. Good cooperation cannot always be reduced to doing the same things or even continuously coordinating, and division of labor might play an important role (Bjørndahl, et al., 2015; Fusaroli, Raczaszek-Leonardi, et al., 2014).

> Shared HR dynamics can be shown to vary according to the demands of the task: generally, individual trials induce higher level of shared HR dynamics than collective trials. We speculate that this is because in individual tasks, participants engage in very similar actions (quietly build each their model). However, only collective trials show the marks of actual interactions: within-group pairs display a significantly higher stability of shared HR dynamics than virtual pairs in collective, but not in individual trials. Similarly, shared HR dynamics grows during collective, but not during individual trials. Further supporting this line of arguments, shared HR dynamics during collective trials were predicted by level and stability of speech and building coordination: the more behavioral coordination, the more shared HR dynamics. Consistently, we observed behavioral coordination (but not shared HR dynamics) to predict perceived group relatedness and competence.
## Methods
### Cardiac Activity

> To align heart beat activity across participants we generated equally sampled time-series by estimating beats per minute every second based on sliding 5- second windows (Wallot, et al., 2013). We isolated 5-minute HR sequences corresponding to the 12 construction tasks.

### Synchronization
> HR time series present non-stationary dynamics. In other words, their means and standard deviations may vary over time as a function of e.g. activity, respiration and emotional arousal (Malik et al., 1996; Sayers, 1973). For this reason, linear methods assuming data stationarity, such as for instance correlation, are not appropriate to assess interpersonal shared HR dynamics. Additionally, interpersonal HR dynamics have been shown to display continuously varying lags of synchronization (Strang, et al., 2014), which require a method that does not assume constant lags as, for instance, a cross-correlation would do. We therefore chose to employ Cross Recurrence Quantification Analysis (CRQA), a method initially developed by Webber and Zbilut to quantify the shared dynamics of complex non-linear systems (Marwan, Thiel, & Nowaczyk, 2002; Shockley, Butwill, Zbilut, & Webber, 2002; Webber & Zbilut, 1994). Relying on two time-series, CRQA reconstructs the phase space of possible states and quantifies the structure of recurrence, that is, of the instances in which the two time-series display similar dynamics, controlling for individual baselines of HR (for more details on the methods, cf. Fusaroli, Konvalinka, & Wallot, 2014; Marwan, Carmen Romano, Thiel, & Kurths, 2007).

> With CRQA we were able to produce several metrics with which to estimate the similarity between dynamical patterns and capture many properties of the heart rate dynamics that would otherwise be lost due to averaging with more traditional correlation analysis. In particular, we calculated: 
> 
> Level of coordination, defined as the percentage of shared states in the phase space, that is the basic dynamic patterns that are repeated between the two time series (recurrence rate, RR). The higher the recurrence rate, the more similar the range of basic dynamic patterns displayed by the participants’ HRs. 
> 
> Stability of coordination, defined as average length of sequences repeated across time-series (L). The higher the L, the more the participants tend to display prolonged and stable sequences of shared HR dynamics. CRQA was calculated using the CRP Toolbox for Matlab 2014a. The phase space parameters were calculated according to Abarbanel (1996): the delay was set to minimize mutual information, and the embedding dimensions to minimize false nearest neighbors across all time-series. The threshold of recurrence was set to ensure recurrence rates comprised between 0.04 and 0.10 (Marwan et al 2007). This led to the following parameters: an embedding dimensions of 4, a delay of 6 and a threshold of 1.

## Important Discussion Points

- Link between conversation/communication and heart rate

>Interlocutors involved in conversation have also been shown to spontaneously adapt to each other’s linguistic forms, conversational moves, syntax and prosody (Fusaroli, Abney, Bahrami, Kello, & Tylén, 2013; Hopkins, Yuill, & Keller, 2015; Pickering & Garrod, 2004; Wilson & Wilson, 2005), which may lead to the development of interactional routines and procedural conventions (Fusaroli & Tylén, in press; Mills, 2014). By using more similar linguistic forms and coordinating the timing of their speech behavior, interlocutors might come to tightly interweave their breathing patterns (McFarland, 2001; Warner, Waggener, & Kronauer, 1983), which in turn have been shown to affect HR (Beda, Jandre, Phillips, Giannella‐Neto, & Simpson, 2007; Berntson, Cacioppo, & Quigley, 1993).