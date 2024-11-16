---
tags:
  - methodology
  - HR
  - IBI
  - physiology
  - ECG
  - iSAT
---

search for outlier detection algorithm citation

```
%% Remove Outliers

threshold = 5;

% For ECG_guide

meanECG_guide = mean(ECG_guide, 'omitnan');

stdECG_guide = std(ECG_guide, 'omitnan');

outliers1 = abs(ECG_guide - meanECG_guide) > threshold * stdECG_guide;

ECG_guide(outliers1) = NaN;

% For ECG_controller

meanECG_controller = mean(ECG_controller, 'omitnan');

stdECG_controller = std(ECG_controller, 'omitnan');

outliers2 = abs(ECG_controller - meanECG_controller) > threshold * stdECG_controller;

ECG_controller(outliers2) = NaN;
```