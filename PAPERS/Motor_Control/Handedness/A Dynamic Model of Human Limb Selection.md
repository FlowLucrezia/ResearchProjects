---
tags:
  - dynamics
  - handedness
  - decision_making
  - report
  - experiment
  - hysteresis
  - grasping
  - motion
  - emergence
  - adaptation
  - coordination
---
10.3390/dynamics3030027

[Cox, R. F. (2023). A Dynamic Model of Human Limb Selection. _Dynamics_, _3_(3), 530-549.](https://www.mdpi.com/2673-8716/3/3/27)


### Hypotheses

*   Experiment 1 aimed to demonstrate **perseverative limb selection** resulting from a short-term bias built up during training. It was expected that after training trials at the nonpreferred hand, there would be an increase in nonpreferred-hand uses at midline. Only a small increase in preferred-hand uses was expected after training series for the preferred hand because of a ceiling effect.
*   Left-handers were hypothesized to demonstrate a stronger effect of perseveration than right-handers because they already switch more easily to their nonpreferred hand.
*   Experiment 2 aimed to find a **spatial delay** in the location of the switch from grasping a cube with the left hand to grasping it with the right hand when presenting cubes in a clockwise sequence. The same hysteresis effect was expected for right-hand grasping switching into left-hand grasping in a counter-clockwise sequence.

### Methodology

*  **Participants**: Experiment 1 included 20 strongly left-handed and 24 strongly right-handed adults. Experiment 2 included 15 strongly right-handed adult volunteers.
*  **Procedure**: In both experiments, participants were seated at a table and had to pick up a small cube and displace it to a box in front of them.
*  **Experiment 1**: Participants received training trials where cubes were placed at lateral positions, either four times on the extreme left side or four times on the extreme right side. This was followed by two trials in which the object was presented on the participant’s midline. The training was offered to both the preferred and nonpreferred hand in separate conditions.
* **Experiment 2**: Participants received a clockwise and counter-clockwise sequence of cube presentations. The main objective was to detect differences in the pattern of hand use across hemispace as a function of the type of sequence that has been performed.
* **General procedure for both experiments**: The original experiment by Gabbard et al. was replicated as a third condition in between the two training conditions in Experiment 1 and the two sequential conditions in Experiment 2. In this condition, the cube was randomly placed in each of the nine locations.

### Model Components
*   The core of the model consists of **two ‘limb-selection sites’**, each representing the selection process for using one of the two available hands.
*   The sites are assigned **time-varying activation functions**, *uL(t)* and *uR(t)*, for the left hand and right hand, respectively.
*   The limb-selection process obeys a continuous dynamic described by a set of two coupled, first-order nonlinear differential equations:

    τ · . *uL(t)* = −*uL(t)* + *h*− *cL* · *σ(uR)* + *IL(t)* + *n* · *ξ(t)*;

    τ · . *uR(t)* = −*uR(t)* + *h*− *cR* · *σ(uL)* + *IR(t)* + *n* · *ξ(t)*.
    
*  The limb-selection sites are mutually connected by **nonlinear cross-lateral inhibitory couplings**.
*  The total input consists of **perceptual input** about the spatial layout of objects and **memory input**, representing the accumulated motor memory of previous limb selections.
*  The final part of the dynamics is a **noise term** *ξ(t)*, which is equal for each site and assumed to be Gaussian white noise.
*  The model integrates external (task and environment) and internal (organismic) constraints, working on at least three different timescales: on-line, short-term and long-term.

### Results, etc.

*   The model reproduces the effects of **perseveration and hysteresis** in limb selection.
*   The model demonstrates how discrete behavioral choices emerge from a dynamic interplay of various external and internal factors.
*   The model replicates the findings of the original experiment by Gabbard et al., and can reproduce the differences in the patterns of hand use between left-handers and right-handers.
*   The difference in the **cross-lateral inhibition strengths** of the two sites is primarily responsible for the qualitative difference between the two laterality groups at the behavioral level.
*   The model suggests a positive relation between the extent of the cross-lateral inhibition asymmetry and the degree of handedness.
*   Age-related changes in hand preference can be implemented by an increasing asymmetry in cross-lateral inhibition.
