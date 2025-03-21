---
tags:
  - methodology
  - report
  - scaling
  - fractal_scaling
  - motor_control
  - adaptation
  - variability
  - dynamics
  - attention
  - driving
  - DFA
  - power_law
  - FYP
  - Hurst
---

[Likens, A. D., Fine, J. M., Amazeen, E. L., & Amazeen, P. G. (2015). Experimental control of scaling behavior: what is not fractal?. Experimental brain research, 233, 2813-2821.](https://d1wqtxts1xzle7.cloudfront.net/46927555/Experimental_control_of_scaling_behavior20160630-19247-zmo4o-libre.pdf?1467331029=&response-content-disposition=inline%3B+filename%3DExperimental_control_of_scaling_behavior.pdf&Expires=1733441917&Signature=VsWy~Be3L8irKS4XRAfDLxOHX-e-Qy4aPMuXR2ghT2Q8cW8l1ScfnwsT7Lcm97kreX1GC~~VJ3pfA2dZKyMzT3VwoQvXp0NTkYyqmvUAU6SQoJdfCRSCbQLa5K5WPJ5fD-B3W-WYgYTor3p9pfDw0VeQFm8A7pAxs~PxjzLiD-ytuBhkSL13CKfNAL5LHPi8zgRlJplKogIbx3d69IlbrxsVctafbeQzBGFY~6ohT7k50zVJLh2p0TwtMMkxoXo3PSkFz57K2--c6FV9dLiFaHK~rQf2msUhNmCwJdOztqS-wMPW5KtV3kf-K5QOjCEQhvqBxgahbRoADKMqEpYNIQ__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)
### Fractal Analysis

> The goal of any fractal analysis is to determine how variability changes as a function of scale (Eke et al. 2002). Execution of fractal analysis involves, at least, two steps— signal classification and estimation of fractal scaling exponents. Signal classification is important because the class of signal—discussed in the next paragraph—determines what methods may be used for estimates of scaling behavior. The class of signal also has theoretical importance, given that a particular signal class has figured prominently in the literature (cf. Van Orden et al. 2003; Wagenmakers et al. 2004). Scaling exponents are likewise important because those measures characterize the fractal properties of a time series and represent the focus of fractal analysis.
> 
> Our interest is to couch the current findings within the larger literature, a task that requires characterizing the current data as either fractional Gaussian noise or fractional Brownian motion. Fractional Gaussian noise (fGn) refers to a class of time series in which the first two central moments are stable (i.e., mean, variance; Eke et al. 2000). Within the psychological domain, fractal analysis has been applied most frequently to fractional Gaussian noise (e.g., Van Orden et al. 2003). In contrast, fractional Brownian motions are those signals that have non-constant variance over time. In experimental contexts, noises generally emerge from event series (e.g., response times, Van Orden et al. 2003; intertap asynchronies, Torre and Wagenmakers 2009). The angular position time series data that we collected may be considered as fractional Gaussian noise for two reasons. First, our study was designed such that participants could theoretically hold the steering wheel at a constant angle in order to accomplish the task. That is true regardless of the steering condition. Thus, any movement is, by definition, error. The second reason is that we used a signal classification routine similar to that proposed in Eke et al. (2000). 
> 
> Classification involves first performing a power spectral analysis. We used the improved variant outlined in Eke et al. (2000) and examined the index, −β, where β is regression slope of power on frequency on a double log scale. If −β < 1, then the signal was considered a case of fractional Gaussian noise; if −β > 1, the signal was considered a case of fractional Brownian motion. All −βs for the time series we analyzed met the criteria for fractional Gaussian noise; −βs and Hurst exponents derived from –βs are found in Table 1. 
> 
> Following classification, fractal properties of angular time series were estimated using detrended fluctuation analysis (DFA; Peng et al. 1994), an algorithm that estimates fractal properties in a time series by determining how a measure of variance depends on scale size. DFA is appropriate for both fractional Gaussian noise and fractional Brownian motion and provided converging evidence regarding the class of the signal. The ultimate use of DFA in estimating scaling behavior stems from the fact that DFA tends to outperform power spectral analysis in estimating Hurst exponents (e.g., Delignières et al. 2006).