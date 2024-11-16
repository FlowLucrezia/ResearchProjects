---
tags:
  - methodology
  - physiology
  - HR
  - ECG
  - IBI
  - iSAT
---

- look for citations here for validated peak detection algorithms!
- Matlab findpeaks
	- consider MinPeakDistance (e.g., 200 vs 100)
		- what does this mean for the mean IBI and realistic HR values...
		- how does FD change in response to varying parameter
	- other parameter settings to constrain findpeaks function?
- gradient vs diff for differences between subsequent points?

[USEFUL RESOURCE](https://terpconnect.umd.edu/~toh/spectrum/PeakFindingandMeasurement.htm)

```
%% find peaks

[pks1,locs1] = findpeaks(int_ECG1,'MinPeakDistance',200);

[pks2,locs2] = findpeaks(int_ECG2,'MinPeakDistance',200);

figure(3)

plot(pks1, "red")

hold on

plot(pks2, "blue")

hold off

IBI_guide=gradient(locs1);

IBI_controller=gradient(locs2);

figure(4)

plot(IBI_guide, "red")

hold on

plot(IBI_controller, "blue")
```