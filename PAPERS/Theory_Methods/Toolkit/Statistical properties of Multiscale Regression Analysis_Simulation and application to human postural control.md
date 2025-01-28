---
tags:
  - methodology
  - iSAT
  - theory
  - postural_control
  - DFA
  - fractal_scaling
  - scaling
  - simulation
  - MRA
  - dynamics
  - interaction
  - coordination
  - complexity
  - kinematics
  - coordination_dynamics
  - stability
  - variability
  - report
  - FYP
---

[Likens, A. D., Amazeen, P. G., West, S. G., & Gibbons, C. T. (2019). Statistical properties of Multiscale Regression Analysis: Simulation and application to human postural control. _Physica A: Statistical Mechanics and Its Applications_, _532_, 121580.](https://pdf.sciencedirectassets.com/271529/1-s2.0-S0378437119X0014X/1-s2.0-S0378437119309331/am.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEGYaCXVzLWVhc3QtMSJGMEQCICjqgMzYdcmrjJY233txBd8t%2FyZVMK1NGakSFUBPrjouAiBRrNi35%2F%2BT7kxDCfUlCVRPQNntOW%2FNbmYliBnQIEUu9iqyBQgfEAUaDDA1OTAwMzU0Njg2NSIMjaa13Chj5hGbsCtoKo8FlxRKo7%2Bwe9Gw2N8X1iLy0h%2FC4C2DMKGrj4L1YfjwCPziR0Z4WSIqcaLrbMb7xYrJdihT9rljJ7YxPssBc%2FGgtGY5O%2BssPwWLT%2FipcC7AN2HPdBA1q8lAi0PLpM2F4OGGQ4HhU7HSFPuzpHwDOAGXeY6KGI4e5tJOO3a5LyN1qSoWSChFySCio4cnZXy%2FBz43UDXb6QUb1h8AwzLh%2F1YfUi2Hmdtkd5jnr0wxUp3yTSGZj92kU89sVGtTL3mOY3uyFXrcGxvjdONc4QB%2F%2BlTGmOnh0gmzZepudxVtLLJDWr0kYCJRlt7xP0O1WNHLPQzALV%2By0j6MUgycJqjf1Zoe3Bav%2FsqWvjk%2Fa7aoMV4G7AHz%2BZoDEy3e%2BiEGZQTfUtqSdVGq4VAQO25fw70KMgP2J3L1MZSHYVfSHXCiG7FTOdrsHPYzDN9BDS9miP2zkiqjF%2FuqzJCW38nf3euB895A1Rw2OVqPg5lSoGm6f3wmlsSbklXVyq8ivSNZYnxlSQp4wnjR6EJRI4i0EdEKNrvIA%2F6OvcOrklvvP573TRVfHMkBtmCU1ePRguV5i2OTZqus9ck7MSA7F0lGutqxveRxAi%2FuHp0%2Fdplexed3JoD1xFHcJYUXQ8PjrvzmI%2FtmU5H24GGgc%2F%2F6T9z%2FmRxg3m6eJjCZHQ1Zi1Q9sMVTdfqD2oFMiXmUcs9nBAhAYCrcfpj%2FwrAjnBg7vxYfwJAhJDE6pfeJBvtzc9RK9Xo8hjl%2Fr3nejKBdEWGeA7ipBpqjfsFo4jJWjHD8Njciy0HSmepo%2FiMVFHJGqBL%2Bq9CdGmO05KVbzd7ownkK2%2Bwn%2Fj0oHuUEf2g5%2FLAlzHXE%2B3ZQ6T3Dn0UUngkQtdfDrf5OLH7hETDXwsi6BjqyARcbgOW%2B8AxQFUo83Er%2FdUSaCo5jsrC1UdW%2FIiAbiLlFKjLaRaxA%2BH2qBBzwWxlLHPELbYnQns4DDNDrPNdq4xQMx4dd1tl9CPYV8xk3g%2BajZ8MEi0Q055DQgUGaMDfaFWAaEevgop%2BnQDKvDqavefRUhp5rULSnkRHetjheAid4m8GWAtCVm7%2BYcocN5EYk1al28WEaQwjfzooZxdE%2FU5tYaAxsUcwwVMGfnE27AZEaNxc%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20241205T223203Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTY3GIN7BSI%2F20241205%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=610a43d670f623f269f5ffadbafc705c9ce6f965c0b22cacae43949ac592afad&hash=f4fd19109fb46374e547b987cfb84a1a706a37aac8fe92aa3be6ac2a614d3dd6&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S0378437119309331&tid=pdf-78b66fe8-a4cb-4adb-b9e4-066f01354dfd&sid=3d9342a44d71b5414d3a381-85138e4b42c5gxrqa&type=client)

DFA -> DCCA 

### Detrended Cross-Correlation Analysis

> Detrended Cross-Correlation Analysis (DCCA) extends the DFA technique to two time series [5,9–11]. With DCCA, the DFA algorithm is applied twice, once on each signal in a bivariate time series, resulting in scale-wise fluctuation estimates (i.e., standard deviations) for both Xt (i.e., Equation 1) and Yt (i.e., Equation 3):

![[Pasted image 20241205153416.png]]

### DFA-Based Multiscale Regression Analysis

> Only a small modification is necessary to transition from estimating correlation or regression at many scales to estimating scale-wise regression coefficients [1]. The goals of DCCA and MRA, however, are distinct. As MRA’s simpler counterpart, DCCA is a symmetric estimate of the strength and direction of a relationship between two variables. In contrast, MRA provides estimates of the asymmetric multiscale relationship between two variables while preserving their original units, making MRA appropriate for addressing questions in which system components are better conceived as independent and dependent variables. In addition, regression is strongly preferred over correlation techniques when the goal is to compare different treatment conditions or different sub-groups [12,13]. In brief, comparison of correlation coefficients makes the strong assumption of equal variances on the variables in the different groups and leads to biased results when there is restriction or expansion of the range of the variables. In contrast, regression coefficients are not biased by differences between group variances; only the standard errors can potentially be affected.

![[Pasted image 20241205153518.png]]

![[Pasted image 20241205153530.png]]