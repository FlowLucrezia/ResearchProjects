---
tags:
  - Fundamentals_of_CAS
  - ABM
  - complexity
  - team
  - teams
  - problem_solving
  - collaboration
  - synchronization
  - emotion
  - affect
  - contagion
---
## Theoretical Background

Interactive team cognition perspectives [@cookeInteractiveTeamCognition2013](Cooke et al., 2013) and team dynamics research [@gormanMeasuringRealTimeTeam2020] have increasingly emphasized the importance of coordination, adaptability, and knowledge reorganization through ongoing collaboration at the team level, rather than simply aggregating individual teammates' knowledge. These perspectives posit that productive teamwork is driven by the interplay between direct verbal communication about relational and task-relevant aspects of collaboration and indirect emotional sharing (e.g., shared physiological arousal). Importantly, emotional factors are considered to play a critical role in collaborative problem-solving and learning activities. Shared emotional experiences have been shown to enhance engagement and improve learning outcomes ==(Järvelä et al., 2016, @@@ *find citation*)==, and shared physiological responses (e.g., inter-agent synchrony of electrodermal and cardiac activity) have been linked to variations in subjective appraisals and objective measures of team performance [@chanelAssessmentComputerSupportedCollaborative2013] [@chikersalDeepStructuresCollaboration2017] [@gordonGrouplevelPhysiologicalSynchrony2021]. ==*insert here linking to dialogue*==. It is hypothesized that the emotional character of interactions between collaborators is influenced by established team roles and the emotional nature of individual contributions [@molinariEmotionFeedbackComputerMediated2013] ==(@@@)==, with team dynamics continuously reshaping as individuals engage in emotionally varied dialogue with other teammates. 

Individual emotional responses to relational and task-related events during collaborative problem solving can be regulated, and thus evolve dynamically, through various means. While self-regulation of emotions in response to external perturbations has been a primary focus of psychology research agendas ==(e.g., @@@)==, there has been less emphasis on how interactions between team members shape the shared emotional states of collaborating agents. ==*insert here self, co-, socially-shared regulation differentiation*==. As the emotionally-laden nature of interactions in a collaborative setting is expected to vary dynamically depending on relational (e.g., social distance between participants) and task-related constraints (e.g., success of problem-solving attempt) ==(@@@)==, there is a need to clarify how role flexibility and ongoing task performance may influence how teams share, spread, and regulate emotions.

Previous agent-based models that have looked at emotion contagion have primarily focused on how emotions spread in multi-agent systems in evacuation scenarios or in response to rare events (e.g., disasters) ==(@@@) some research on dyads/triads??==. Constructing the following agent-based model will address how individual and group-level emotions emerge and evolve over the course of a triadic collaborative problem-solving (CPS) task, in response to both task-related and socioemotional influences.

## What does the model DO? 

This model sets out to explore how individual and group-level emotion dynamics evolve over the course of a triadic collaborative problem-solving (CPS) task in response to both changes in task performance and emotion contagion between agents. In particular, it sets out to answer:

- How these dynamics vary in response to acute perturbations (e.g., surprise or frustration arising from an incorrect submission)
and
- How these dynamics vary when behavioral roles are fixed or mutable during a collaborative problem-solving task  

The emotional state of an agent at a given time point, measured along two dimensions (valence & arousal), is affected by the emotional stimulus received as a result of ongoing task performance, as well as that resulting from emotion contagion. This is represented by a modification of an individuals’ emotional state at each time step, such that:

![[Pasted image 20241124132627.png]]

Values for emotion arousal and valence range from -1 to 1, representing low to high activating, and negative to positively valenced emotional states, respectively. Valenced emotional responses to emotion contagion and task performance are multiplied with a positive or negative bias, which reflects how personality traits are considered to influence the tendency for individuals to experience certain emotions (Marengo et al 2021; Steele et al 2008). The net emotion state of the receiver ER is updated by adding the valence and arousal of each (positively or negatively biased) incoming emotion to the current emotion state of the agent. 

In the absence of any emotional input (contagion or task performance), the overall emotional state of the receiving agent refers to a single point in valence-arousal space that will eventually approach a neutral state (i.e., origin of valence-arousal space [0,0]). ==Based on the framework outlined by @@@, emotions are considered to decay in the form of a hyperbolic tangential function - resulting in the persistence of emotion for some time, followed by a decay toward the neutral state with an inverted s-curve (@@@). Emotion regulatory strategies that contribute to the persistence of emotions are found to correlate with personality traits (@@@), in addition to the degree to which internal emotional states are expressed by individual agents (@@@). At each time step, the overall emotional intensity of each agent - given as the Euclidean distance in valence-arousal space with respect to a neutral origin [0,0] - is updated via the processes of regulation and expression (@@@).==

![[netlogo model.png]]

If there is no input due to task performance at a given timestep, then the current emotion will simply be updated by adding the new emotional stimulus due to contagion. That is, if there is no emotional input of task performance (E_T = 0), then the change in emotion of the “receiver” over one time step is found by adding E_C to the current emotion value (for valence and arousal separately). The emotion contagion process implies multiple “sending” agents, and one “receiving” agent, although in practice this process is generalized to all agents. Thus, In the absence of task performance input, for each timestep, the emotional state of any agent at t(i-1) is modified by the emotional contagion input of the other two agents.

Finally, the emotional state of the team as a whole is simply evaluated as the average emotion intensity of all team members, and will be updated at each timestep along with individual emotion states. 

![[netlogo model (1).png]]
Figure 2. Basic flowchart of model components, indicating how emotional inputs due to task performance and emotion contagion are integrated into the emotional state of a receiving agent.

## Model Initialization

The intensity of the emotional state for each agent (coarsely representing their baseline mood) in this model is initialized by randomly setting the starting values for each agents’ emotional dimension parameter to a number from -1 to 1. Specifically, emotional state intensity is measured as the distance in valence-arousal space with respect to a neutral origin [0, 0]. ==Variability is represented by drawing initial values from a normal distribution, centered around this neutral origin (@@@). ==

![[Pasted image 20241124134513.png]]

In the collaborative problem solving tasks that this model aims to describe (see Sun et al., 2020 for a description of their collaborative coding task), the timescale of interest for detecting changes in emotions reflects the approximate timescale of discourse taking place between agents (Bietti & Sutton, 2015; Lougheed & Hollenstein, 2018; Zhang et al., 2021, 2024). That is, emotional states are expected to change or be updated at frequent intervals (in the range of every 1-30 seconds) during the task. As each task is expected to last approximately 15-20 minutes (e.g, Sun et al., 2020, see Minecraft Hour of Code task), this model will be run over approximately 800-1000 timesteps to capture an ecologically relevant evolution of emotional states.

Whether behavioral roles are fixed (i.e., one agent holds more behavioral responsibilities than the other two) or mutable (i.e., all agents are capable of assuming equal behavioral responsibilities) may influence the symmetry of the social connection or distance between interacting partners (e.g., Magee & Smith, 2013; Agnès et al., 2023), which could in turn influence the extent to which emotional contagion takes place between agents (Elfenbein, 2014; Tee, 2015; Harris & Hancock, 2019; Kane et al., 2023). Moreover, task performance, and by consequence its emotional influence on individual agents, is considered to depend on task difficulty and understanding (e.g., Malmberg et al., 2022). Behavioral roles are set to be either fixed or mutable ([0 1]) during a triadic collaborative task with varying degrees of difficulty (“easy”, “medium”, “hard”). 

### MODEL SETUP (NetLogo)

```
extensions [math stats]  
  
globals [  
  ;task-difficulty  ;; "easy", "medium", "hard"  
  ;data             ;; Personality data loaded from CSV  
  task-outcome  
  correct-interval correct-end incorrect-interval incorrect-end ;; Event timing settings  
]  
  
breed [teammates teammate]  
  
teammates-own [  
  valence          ;; Emotional valence (-1 to 1)  
  valence_out1  
  valence_out2  
  influence-valence  
  EC-valence  
  arousal          ;; Emotional arousal (-1 to 1)  
  arousal_out1  
  arousal_out2  
  influence-arousal  
  EC-arousal  
  intensity        ;; Emotional Intensity (0 to sqrt(2), euclidean distance from origin in valence-arousal space)  
  beta  
  dist  
  RSR  
  channel-strength  
  total-channel-strength  
  personality      ;; List of Big Five personality traits (OCEAN)  
  role             ;; "controller" or "guide"  
  susceptibility   ;; Emotional susceptibility (δR)  
  expressiveness   ;; Emotional expressiveness (εS)  
  regulation-effectiveness ;; Emotion regulation effectiveness (τR)  
  positive-bias    ;; Personality bias towards positive emotions  
  negative-bias    ;; Personality bias towards negative emotions  
  timestep  
  tmax  
]  
  
;; --- Setup Procedures ---  
to setup  
  clear-all  
  ;set timestep 0  
  ;set task-difficulty ;; Set initial difficulty level as needed  
  initialize-task-settings  
  ;load-personality-data  
  setup-task-plot  
  setup-emotion-plots  
  create-teammates 3 [  
    initialize-agent  
    assign-roles  
  ]  
  reset-ticks  
end  
  
;to load-personality-data  
; let file-path "personality_traits.csv"  
; set data csv:from-file file-path  
;end  
  
to initialize-task-settings  
  if task-difficulty = "easy" [  
    set correct-interval 20  
    set correct-end 1000  
    set incorrect-interval 50  
    set incorrect-end 900  
  ]  
  if task-difficulty = "medium" [  
    set correct-interval 40  
    set correct-end 1000  
    set incorrect-interval 30  
    set incorrect-end 900  
  ]  
  if task-difficulty = "hard" [  
    set correct-interval 50  
    set correct-end 1000  
    set incorrect-interval 20  
    set incorrect-end 900  
  ]  
  print (word "Task settings: "  
          "Correct interval: " correct-interval ", "  
          "Correct end: " correct-end ", "  
          "Incorrect interval: " incorrect-interval ", "  
          "Incorrect end: " incorrect-end)  
end  
  
to setup-task-plot  
  set-current-plot "Task-Performance"  
  set-plot-x-range 0 1000  
  set-plot-y-range 0 1  
end  
  
to setup-emotion-plots  
;  set-current-plot "Emotion-Intensity"  
;  clear-plot  
;  create-temporary-plot-pen "teammate-1"  
;  create-temporary-plot-pen "teammate-2"  
;  create-temporary-plot-pen "teammate-3"  
;  create-temporary-plot-pen "team"  
;  set-plot-x-range 0 10000  
;  set-plot-y-range 0 0.1  
;  
;  set-current-plot "Emotion-Dimensions"  
;  clear-plot  
;  create-temporary-plot-pen "tm1-val"  
;  create-temporary-plot-pen "tm2-val"  
;  create-temporary-plot-pen "tm3-val"  
;  set-plot-x-range 0 10000  
;  set-plot-y-range -1 1  
end  
  
to initialize-agent  
  set size 2  
  let radius (min list world-width world-height) / 3  
  layout-circle teammates radius  
  ;setxy random-xcor random-ycor ;; distribute agents randomly in world  
  set shape "controller"  
  ;set random personality traits (1-5, for items 0-4 [OCEAN])  
  set personality (list ((random 4 + 1) / 5) ((random 4 + 1) / 5) ((random 4 + 1) / 5)  
                  ((random 4 + 1) / 5) ((random 4 + 1) / 5))  
  ;set starting emotion valyes  
  set valence random-normal 0 0.2  
  set arousal random-normal 0 0.2  
  set intensity sqrt (valence ^ 2 + arousal ^ 2)  
  ;setup timestep  
  set timestep 0  
  ;  let random-index random length data  
  ;  set personality item random-index data  
  ;  let traits sublist personality 0 4  
  calculate-personality-parameters  
 end  
  
;; Calculation procedures for personality-based parameters  
to calculate-personality-parameters  
  ;; Susceptibility (δR)  
  set susceptibility 0.35 * (item 0 personality) - 0.18 * (item 1 personality) +  
  0.14 * (item 2 personality) + 0.31 * (item 3 personality) + 0.02 * (item 4 personality)  
  ;; Expressiveness (εS)  
  set expressiveness 0.14 * (item 0 personality) - 0.02 * (item 1 personality) +  
  0.32 * (item 2 personality) + 0.11 * (item 3 personality) + 0.29 * (item 4 personality)  
  ;; Regulation Effectiveness (τR)  
  set regulation-effectiveness 0.17 * (item 0 personality) -  
  0.22 * (item 1 personality) + 0.19 * (item 2 personality) + 0.45 * (item 3 personality) + 0.23 * (item 4 personality)  
  ;; Positive/Negative Bias  
  set positive-bias 1 + (0.2 * (item 0 personality) -  
    0.26 * (item 1 personality) + 0.44 * (item 2 personality) + 0.12 * (item 3 personality) + 0.29 * (item 4 personality)) / 2  
  set negative-bias 1 - (0.03 * (item 0 personality) -  
    0.21 * (item 1 personality) + 0.18 * (item 2 personality) + 0.19 * (item 3 personality) + 0.54 * (item 4 personality)) / 2  
end  
  
to assign-roles  
  ;; Determine roles based on the structure setting  
  ifelse role-structure = true [  
    ;; Fixed roles: Assign "controller" to the first teammate, and "guide" to the others  
    ask teammate 0 [ set role "controller"  
      set color blue  
    ]       ;; First teammate is always a controller  
    ask teammates with [who != 0] [ set role "guide"  
    set color green  
    ] ;; Other teammates are guides  
  ] [  
    ;; Mutable roles: All agents are "controller"  
    ask teammates [ set role "controller"  
    set color blue  
    ]        ;; Assign all teammates as controllers  
  ]  
end  
  

```
## Emotional Influence of Task Performance

In this model, a task-related event modifies the emotion states of the agents depending on whether the outcomes are considered correct or incorrect. For instance, in the context of collaborative problem-solving for a coding task, this may look like the selection of the correct coding block as well as the successful completion of a sub-task or task. The alternative would look like the incorrect selection of a coding block or the unsuccessful completion of a task, at smaller and larger scales, respectively. With respect to the current model, these outcomes at multiple scales will be considered equivalent, such that the same classification of the event will trigger similar changes in emotion state for each individual agent. To represent variability in the process of appraising an event emotionally, the valence and arousal values are drawn from normal distributions ==(@@@)==.

![[Pasted image 20241124134625.png]]

Here, the task difficulty setting will vary the frequency at which these events occur over the course of the task, with smaller scale correct (and possibly incorrect) outcomes occurring more frequently in shorter, simpler tasks, and less frequently in more complex or difficult tasks. Thus, the degree of complexity of the task will determine how often the event “stimulus” modulates the agents’ emotional states.

If task difficulty = “easy”:
Event = “correct” will occur at timesteps = [10 : 10 : 800]
Event = “incorrect” will occur at timesteps = [15 : 40 : 700]

If task difficulty = “medium”:
Event = “correct” will occur at timesteps = [10 : 30 : 900]
Event = “incorrect” will occur at timesteps = [15 : 30 : 800]

If task difficulty = “hard”:
Event = “correct” will occur at timesteps = [10 : 50 : 1000]
Event = “incorrect” will occur at timesteps = [15 : 20 : 900]

## Emotion Contagion

Following initialization of emotion states of all agents, each agent, or ‘teammate’, is able to influence the emotional state of all other agents at each consecutive time step. Calculated at each timestep for the dimensions of valence and arousal, separately, the emotional stimulus resulting from emotion contagion consists of two components: the combined channel strength between the receiver and senders αSR and the net emotional influence of the senders ES.

The change in valence and arousal of an agent as a result of emotion contagion EC is the result of the total connection strength between the receiver and its neighbors multiplied by the emotional influence (for the given emotional dimension). 

![[Pasted image 20241124140306.png]]

The total channel strength αSR  is calculated as the sum of the individual channels between each sender and the receiver. For any sender and the receiver, the channel strength 𝞴SR is the product of the connection between the agents βSR , the susceptibility of the receiver δR, and the weighted attention of the receiver for the sender ӨS.

![[Pasted image 20241124140232.png]] 

The setting of behavioral roles as either fixed or mutable addresses the symmetry of the parameter βSR -  the connection between the communicating agents - calculated as the inverse of the distance DSR and the strength of the social relationship RSR between receiver and sender. Based on previously empirically validated model settings (Van Haeringen et al., 2023)  that looked at emotional contagion via video conferencing (like the context of the collaborative task in this model), the distance to each sender DSR is assumed to be equal for all groupings of receivers and senders.

![[Pasted image 20241124140211.png]]

In the case of fixed roles (0), two agents are prescribed “Guide” or indirect contributor roles, and one agent is prescribed a “Controller”, or direct contributor role. The indirect contributors are able to communicate about the task and their emotions, but they are not able to directly control task performance via the interface. That is, agents in the Guide (Gx) role are unable to influence performance themselves, but must interact with the Controller (C) in order to execute their intended behaviors. The Controller is able to directly affect task performance by engaging with the task interface, in addition to communicating their ideas and emotions to the other agents. That is, their emotional state results in behavioral intentions (which may influence task performance) that can be executed without necessarily needing to be preceded by a communicative interaction with teammates. 

An asymmetrical connection βSR between agent C and agents G1 & G2 results from a difference in the strength of the social relationship RSR between receiver and sender. Specifically, there is expected to be a stronger “link” between Guide agents and the Controller agent, which may reflect higher reciprocal communication needs in order to explore ideas, share emotions, and enact problem-solving strategies (Grand et al., 2016; Driskell et al., 2017). As the need to communicate ideas and intentions is expected to be higher for C-G pairs compared to G-G pairs, the parameter value for RSR when C is a communicating agent will be greater than when G-G pairs are communicating (e.g., 1 for C-Gx combinations, 0.8 for Gx-Gx combinations). In terms of agents-own variables, the “Controller” will have an RSR = 1 whereas both “Guides” will have RSR = 0.8.

In the case of mutable roles (1), all agents are capable of interacting with the task interface in the same manner as the Controller. In certain situations and group compositions (e.g., low mood or rapport, low task complexity, greater differences in perceived and actual competence of other agents) this may result in more independent problem-solving approaches and limited emotional sharing or communication, whereas the possibility for flexible role assignments may promote enhanced collaboration and shared emotional regulation in response to task-related or socio-emotional stressors. With respect to parameter setting for channel strength, the connection between interacting agents βSR is equivalent for all combinations of interacting agents in this condition.

![[Pasted image 20241124140144.png]]  

Personality traits of the agents can also be modified in the model, which by altering the emotional susceptibility parameter of the emotion receiver δR will in turn also affect the channel strength between interacting agents. This parameter is tuned based on a previous empirically validated model (Van Haeringen, 2023) that calculated δR by taking the sum of the agent’s personality traits, multiplied by the slopes of the correlations between empathy and each trait of the OCEAN personality model (Jolliffe and Farrington, 2006).

![[Pasted image 20241124140120.png]]

The third component that modulates channel strength is the receiver’s attention bias for the sender ӨS. In this model, one or two senders compete for the receiver’s attention, although all agents will receive at least a base degree of attention. The potential attention for a sender Өs is weighted against the combined potential attention of the group of senders ӨC. The relative importance of the potential attention ӨS is determined by the constant k1 - representing the ratio of the part of the attention that is distributed based on expression strength against the part that is allocated equally. Half the attention will be distributed equally, while the other half is distributed based on the expressions of the senders. This will be reflected in a value of 1 for the k1 constant. 

![[Pasted image 20241124140106.png]]

Without a bias in attention towards emotional stimuli, the potential attention ӨS a sender claims is equal to their expressiveness εS (see the subsection Emotional Expression), derived from the personality of the agent based on reported correlations between the Big Five traits and emotional expressivity (Gross & John, 1995). In line with Van Haeringen at al (2023), no attention preference for a specific type of emotion is set, so the potential attention for a sender ӨS is equal to the Euclidean distance of its expression in valence-arousal space to the origin [0, 0].

![[Pasted image 20241124140031.png]]

The final aspect of emotional contagion corresponds to the net emotional influence 𝜁SR of the senders on the receiver. First, the emotional expressions of the senders are weighted with respect to the relative channel strength to the receiver:

![[Pasted image 20241124135946.png]]

Then, the weighted emotion of the senders is either amplified (🇾R > 0.5), absorbed (🇾R = 0.5) or dampened (🇾R < 0.5) depending on the weighted valence of the senders. In this model, negative emotions are dampened and positive emotions are amplified (see Van Haeringen et al., 2021).

![[Pasted image 20241124135932.png]]

==Finally, net emotional influence of the senders on the receiver is calculated using three different conditions that account for amplification of negative and positively valenced emotions in the range of -1 to 1. When both the emotion of the receiver and the weighted average of the senders is on the positive side of the scale, the influence is calculated in the same manner as the amplification process was in ASCRIBE (@@@). If both are on the negative end of the scale, influence is calculated in the same way and then inverted. When they have opposite polarity, the emotion is the difference between the weighted emotion of the senders modulated by 🇾R and the emotion of the receiver modulated by 1 – 🇾R. ==

  
![[Pasted image 20241124140009.png]]
  
The change in emotional state of a receiver resulting from the described contagion process is then found by multiplying total channel strength αSR by net emotional influence 𝜁SR  (calculated above).

## Emotion Generation

Personality traits may bias individuals’ tendency to experience certain emotions (e.g., Steel et al., 2008), for instance, neuroticism has been linked to negative affect (Marengo et al., 2021). In the present model, if the valence of incoming emotions (either ET and EC) is above zero, agents multiply the incoming emotional stimuli with a personality bias toward positive emotions, or else with the personality bias towards negative emotions (see Van Haeringen, 2023). These personality biases are defined by slopes found by Steel et al (2008) in a meta-analysis reporting correlations between the Big Five personality traits and the propensity for positive and negative emotions. Specifically, the personality profile of each agent is multiplied by these slopes, such that the influence of emotions fitting the personality of the agent is inflated, whereas those that are not are relatively deflated.

![[Pasted image 20241124135827.png]]


## Emotion Regulation

==Based on work by xxx (@@@), emotions are considered to decay over time. Previous work has suggested modeling this process of decay as allowing emotions to persist for an amount of time, after which they decay exponentially (Ojha et al @@@)==. In this model, the process of emotion decay is modeled according to a hyperbolic tan function proposed by Van Haeringen et al (2024), where an emotion is maintained for a certain amount of time prior to decaying exponentially toward zero, where it functions as an asymptote as it approaches the origin of valence-arousal space. Following from the work of Van Haeringen et al (2024), a regulation threshold set to a distance of 0.2 from the origin decides if emotion is regulated by incrementing or resetting ti. This regulation threshold is set to match the limits of the neutral category reported by Van Haeringen et al (2024).

![[Pasted image 20241124135727.png]]

The time it takes for an emotion to decay T depends on its maximum lifespan tmax, the regulation effectiveness of the agent τR, as well as other unknown individual differences that could be represented by generating a normal distribution. 

![[Pasted image 20241124135706.png]]

In the original model by Van Haeringen et al (2023), the maximum lifespan of emotions was simplified to a single value of 250, which was found by manually tuning the values to approximate the average decay in their empirical data. This parameter will also be altered in the present model to align with research that has reported on the half-life of learning centered emotions such as confusion, frustration, and surprise ==(@@@)==. The exponential decay functions developed by @dmelloHalflifeCognitiveaffectiveStates2011 supported the following classification of learning-centered emotions: persistent emotions (boredom, flow/engagement, and confusion), an emotion of intermediate duration (frustration), and transitory emotions (delight and surprise). In this model, the maximum lifespan of highly negative emotions (e.g., anger, frustration) is set to an intermediate duration of 100. For strong, transitory emotions such as surprise or delight, the maximum lifespan was set to a short duration of 50. Finally, persistent emotions that are characterized as having intermediate positions in valence-arousal space (e.g., flow, confusion) were set to have a maximum lifespan of 250. Thus, the net value of the incoming emotion (angle and distance from the origin in valence-arousal space) also determines tmax.

![[Pasted image 20241124135644.png]]

The current emotion state ER is modified by ΔER if the regulation threshold (above described) is surpassed:

![[Pasted image 20241124135554.png]]
## Emotion Expression

Following regulation of emotional state, an agents’ emotional expressiveness εS is derived from the personality traits of the agent, based on correlations between the Big Five personality traits and emotional expressivity [@grossFacetsEmotionalExpressivity1995]. The regulated emotion of the receiver ER is modified by multiplying it by the emotional expressiveness value obtained εS. This step was unchanged from the emotion contagion model described by Van Haeringen et al (2023). Following this step, the agent that expresses their emotional state is now considered the ‘sender’, and their their emotion intensity is represented by the variable ES.

![[Pasted image 20241124135403.png]]

### MODEL RUN (NetLogo)

```
to go  
  
  ask teammates [  
  output-emotions  
  if emotion-contagion = true [  
    contagion  
    ]  
  if task-event = true [  
     update-task-emotion  
   ]  
  
    regulate-emotion  
    express-emotion  
  ]  
  
  
  update-task-performance-plot  
  ;plot-emotion-intensity  
  ;plot-emotion-dimensions  
  
  if ticks >= 1000 [  
    stop  
  ]  
  
  tick  
end  
  
to output-emotions  
    let senders n-of 2 other teammates  
    let senderlist [who] of senders  
  ;let templist1 [valence] of senders  
    set valence_out1 first [valence] of senders with [who = first senderlist]  
    set valence_out2 first [valence] of senders with [who = last senderlist]  
    set arousal_out1 first [arousal] of senders with [who = first senderlist]  
    set arousal_out2 first [arousal] of senders with [who = last senderlist]  
    ;set intensity_out1 first [intensity] of senders with [who = first senderlist]  
    ;set intensity_out2 first [intensity] of senders with [who = last senderlist]  
end  
  
  
;; contagion procedure -------------------------------  
  
to contagion  
 set EC-valence calculate-contagion-valence  
 set EC-arousal calculate-contagion-arousal  
 set valence valence + EC-valence  
 set arousal arousal + EC-arousal  
 set intensity sqrt (valence ^ 2 + arousal ^ 2)  
  ;print (word "EC-valence of " [who] of teammates [EC-valence] of teammates)  
  ;print (word "EC-arousal of " [who] of teammates [EC-arousal] of teammates)  
end  
  
to-report calculate-contagion-valence  
 ;let total-channel-strength 0  
 ask teammates [  
   set channel-strength calculate-channel-strength  
   set influence-valence calculate-influence-valence  
   set total-channel-strength sum [channel-strength] of teammates  
   let net-influence-v sum [influence-valence] of other teammates  
   set EC-valence net-influence-v / total-channel-strength  
  ]  
  report EC-valence  
  ;print (word "EC-valence " [EC-valence] of teammates)  
end  
  
to-report calculate-contagion-arousal  
  ;let total-channel-strength 0  
  ask teammates [  
   set channel-strength calculate-channel-strength  
   set influence-arousal calculate-influence-arousal  
   set total-channel-strength sum [channel-strength] of teammates  
   let net-influence-a sum [influence-arousal] of other teammates  
   set EC-arousal net-influence-a / total-channel-strength  
  ]  
  report EC-arousal  
end  
  
;; channel strength calculations -------------------------------  
  
to-report calculate-channel-strength  
 ask-concurrent teammates [  
 set beta calculate-beta  
 let delta susceptibility  
 let theta_w calculate-attention-bias  
 set channel-strength beta * delta * theta_w  
  ]  
 report channel-strength  
end  
  
;beta  
to-report calculate-beta  
 ask-concurrent teammates [  
    set RSR ifelse-value (role-structure = true and  
   (role = "controller")) [1] [0.8] ;; I don't think this part is right, how to fix?  
    set dist 1  
    set beta (1 / dist * RSR)  
  ]  
  report beta  
end  
  
;attention bias  
to-report calculate-attention-bias  
  let theta_w [expressiveness] of teammates  
  ask teammates [  
    let theta expressiveness  
    let k 1  
    let N 3  
    let theta_c sum [expressiveness] of teammates ;need to sum up expressiveness of all senders  
    set theta_w (((1 / N)+ k * theta) / 1 + (k * theta_c))  
  ]  
  report theta_w  
end  
  
;; ----------------------------------  
  
;net emotional influence of senders on receiver  
to-report calculate-influence-valence  
 ;let total-channel-strength 0  
 ;let channel-strength 0  
  let ESw 0  
  if channel-strength > 0 [  
  ask teammates [  
    ;let senders n-of 2 other teammates  
    ;let senderlist [who] of senders  
    ;set channel-strength calculate-channel-strength  
    set total-channel-strength sum [channel-strength] of teammates  
    let ES valence_out1 + valence_out2  
    let ER valence  
    ;foreach senderlist [  
    set ESw (total-channel-strength * ES / channel-strength)  
    ;]  
    let inf (ESw + 1) / 2  
  
   if (ESw >= 0 and ER >= 0) [  
       set influence-valence inf * (1 - (1 - (abs(ESw)))*(1 - ER)) + ((1 - inf) * ESw * ER) - ER  
    ]  
    if (ESw <= 0 and ER <= 0) [  
       set influence-valence -1 * inf * (1 - ((1 - abs(ESw)))*(1 - ER)) + ((1 - inf) * ESw * ER) - ER  
    ]  
   if (ESw >= 0 and ER <= 0) [  
       set influence-valence inf * (ESw - ((1 - inf)) * ER)  
    ]  
    if (ESw <= 0 and ER >= 0) [  
      set influence-valence inf * (ESw - ((1 - inf)) * ER)  
    ]  
  ]  
  ]  
  report influence-valence  
end  
  
to-report calculate-influence-arousal  
 ;let total-channel-strength 0  
 ;let channel-strength 0  
let ESw 0  
  if channel-strength > 0 [  
  ask teammates [  
    ;let senders n-of 2 other teammates  
    ;let senderlist [who] of senders  
    ;set channel-strength calculate-channel-strength  
    set total-channel-strength sum [channel-strength] of teammates  
    let ES arousal_out1 + arousal_out2  
    let ER arousal  
    ;foreach senderlist [  
    set ESw (total-channel-strength * ES / channel-strength)  
    ;]  
    let inf (ESw + 1) / 2  
  
   if (ESw >= 0 and ER >= 0) [  
       set influence-arousal inf * ((1 - (abs(ESw)))*(1 - ER)) + ((1 - inf) * ESw * ER) - ER  
    ]  
    if (ESw <= 0 and ER <= 0) [  
       set influence-arousal inf * (((1 - abs(ESw)))*(1 - ER)) + ((1 - inf) * ESw * ER) - ER  
    ]  
   if (ESw >= 0 and ER <= 0) [  
       set influence-arousal inf * (ESw - ((1 - inf)) * ER)  
    ]  
    if (ESw <= 0 and ER >= 0) [  
      set influence-arousal inf * (ESw - ((1 - inf)) * ER)  
    ]  
  ]  
  ]  
  report influence-arousal  
end  
  
;; influence of task performance on emotions ---------------------------------  
  
to-report task-event  
  ifelse ticks >= 10 and ticks <= correct-end and ticks mod correct-interval = 0 [  
    print (word "Correct event at tick " ticks)  
    set task-outcome "correct"  
    report true  
  ] [  
    ifelse ticks >= 15 and ticks <= incorrect-end and ticks mod incorrect-interval = 0 [  
      print (word "Incorrect event at tick " ticks)  
      set task-outcome "incorrect"  
      report true  
    ] [  
      report false  
    ]  
  ]  
end  
  
  
to update-task-emotion  
 let ET-valence 0  
 let ET-arousal random-normal 0.3 0.2  
  
 if task-outcome = "correct" [  
   set ET-valence random-normal 0.3 0.2  
 ]  
 if task-outcome = "incorrect" [  
   set ET-valence random-normal 0 0.2  
 ]  
  
 if ET-valence > 0 [  
   set ET-valence ET-valence * positive-bias  
 ]  
 if ET-valence <= 0 [  
   set ET-valence ET-valence * negative-bias  
 ]  
  
 set valence valence + ET-valence  
 set arousal arousal + ET-arousal  
 set intensity  sqrt (valence ^ 2 + arousal ^ 2)  
;  set valence max [-1]  
;  set valence min [1]  
;  set arousal max[-1]  
;  set arousal min [1]  
end  
  
;; regulate emotion -----------------------------  
  
to regulate-emotion  
 let delta-ER-valence 0  
 let delta-ER-arousal 0  
  ask-concurrent teammates [  
    if intensity > 0.2 [  
      set timestep timestep + 1  
    ]                             ;; set regulation threshold to limits of neutral  
    if intensity <= 0.2 [  
      set timestep 0  
    ]  
    ;; set maximum lifespan depending on intensity of emotion  
    set tmax (ifelse-value  
      intensity > 0.4 [100]  
      intensity > 0.8 [50]  
      [250]  
      )  
    let T random-normal (tmax - tmax * regulation-effectiveness) 20  
    let tanh (exp (timestep - T) - exp (-1 * timestep - T)) / (exp (timestep - T) + exp (-1 * timestep - T))  
    set delta-ER-valence (-1 * valence) * ((1 + tanh) / 2)  
    set delta-ER-arousal (-1 * arousal) * ((1 + tanh) / 2)  
  
 ;; Adjust current emotional state  
    set valence valence + delta-ER-valence ;; are these right, or necessary?  
    set arousal arousal + delta-ER-arousal  
  ]  
end  
  
;; emotion expression ----------------------------------  
  
to express-emotion  
;  let valence-min -1  
;  let valence-max 1  
;  let arousal-min -1  
;  let arousal-max 1  
  
  set valence valence * expressiveness  
  set arousal arousal * expressiveness  
  
;    ; Normalize valence  
;  set valence ((valence - valence-min) / (valence-max - valence-min)) * (1 - -1) + -1  
;  ; Normalize arousal  
;  set arousal ((arousal - arousal-min) / (arousal-max - arousal-min)) * (1 - -1) + -1  
;  
  set intensity sqrt (valence ^ 2 + arousal ^ 2)  
  ;print (word "Teammate " who ": valence = " valence ", arousal = " arousal ", intensity = " intensity)  
  
end  
  
;; ---------------------- update plots and report values ----------------------------------  
  
to update-task-performance-plot  
  let value-as-number ifelse-value (task-outcome = "correct") [1] [0]  
  set-current-plot "Task-Performance"  
  set-current-plot-pen "performance"  
  plot value-as-number  
end  
  
;to plot-emotion-intensity  
;;  set-current-plot "Emotion-Intensity"  
;;  let intensity1 [intensity] of teammate 0  
;;  let intensity2 [intensity] of teammate 1  
;;  let intensity3 [intensity] of teammate 2  
;;  let intensitym mean [intensity] of teammates  
;;  
;;  set-current-plot-pen "teammate-1"  
;;  plot intensity1  
;;  set-current-plot-pen "teammate-2"  
;;  ;plot [intensity] of teammate 1  
;;  plot intensity2  
;;  set-current-plot-pen "teammate-3"  
;;  ;plot [intensity] of teammate 2  
;;  plot intensity3  
;;  set-current-plot-pen "team"  
;;  ;plot mean [intensity] of teammates  
;;  plot intensitym  
;end  
  
;to plot-emotion-dimensions  
;;  set-current-plot "Emotion-Dimensions"  
;;  set-current-plot-pen "tm1-val"  
;;  plot [valence] of teammate 0  
;;  set-current-plot-pen "tm2-val"  
;;  plot [valence] of teammate 1  
;;  set-current-plot-pen "tm3-val"  
;;  plot [valence] of teammate 2  
;end
```
  

## Model Inputs

- Task difficulty (3)
	- Chooser button
		- Easy
		- Medium
		- Hard
	- Determine:
		- When task input occurs
		- Whether task performance is correct or incorrect
		- compute ET_valence
- Role structure [0 1]
	- Switch button → 
		- Fixed (on)
		- Mutable (off)
	- Determine:
		- Relationship strength between sender and receiver
- Personality traits (5) of each agent (3)
	- Select random rows from csv file (personality_traits.csv)
	- First five columns = OCEAN traits
- Starting emotional state
	- Randomly generated
## Model Outputs

- Task performance - 1 graph
- Binary coded (win vs loss, 0 1)
- Emotion state of each agent 
	- 1 graph → Individual emotional state of each agent (continuous update)
		- Emotion intensity = distance in Euclidean space
			- 3 lines => intensity (1 per agent)
			- Separate lines
	- 1 graph → Averaged emotional state of the group (continuous update)
		- Valence and arousal, separate dimensions
		- Combined as a distance in Euclidean space
		- Separate lines