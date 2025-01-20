
[Wallot, S., Irmer, J. P., Tschense, M., Kuznetsov, N., Højlund, A., & Dietz, M. (2023). A Multivariate Method for Dynamic System Analysis: Multivariate Detrended Fluctuation Analysis Using Generalized Variance. Topics in Cognitive Science.](https://onlinelibrary.wiley.com/doi/full/10.1111/tops.12688)


### Generalization to shared HR dynamics

1. **Input Data**:  
   - Collect simultaneous heart rate (HR) time series from two individuals.  
   - Preprocess the data to remove artifacts and ensure the signals are stationary.
2. **Compute Cumulative Profiles**:  
   - Transform each HR time series into cumulative profiles by summing the deviations of the data from its mean.
3. **Segment Time Series**:  
   - Divide the cumulative profiles into non-overlapping segments of a specified size.
4. **Calculate Covariance Matrix**:  
   - For each segment, compute the variance-covariance matrix to capture individual variances and the covariance between the two signals.
5. **Fluctuation Functions**:  
   - **Total Variance**: Compute the sum of variances from the covariance matrix to get the total variability.  
   - **Generalized Variance**: Use the determinant of the covariance matrix to emphasize joint variability and correlations.
6. **Scaling Behavior**:  
   - Plot the logarithm of fluctuation sizes against the logarithm of segment sizes.  
   - Determine scaling properties by calculating slopes, which reflect the dynamics of individual and joint variability.

  The generalized variance method captures shared variability between the two signals, making it ideal for assessing synchrony.  
  This method can identify how synchrony changes across different timescales, such as rapid or slower heart rate fluctuations.  
### Interpretation
  - A higher generalized variance scaling value (compared to total variance) suggests stronger coupling or synchronization between the individuals.  
  - Persistent scaling indicates stable, coordinated dynamics between the two signals.

