---
tags:
  - methodology
  - ECG
  - HR
  - IBI
  - physiology
  - iSAT
---
- consider location and amount of missing points
- look for citations here about linear interpolation for ECG

```
%% Interpolate NaN Values

Indices1 = 1:numel(ECG_guide);

Indices2 = 1:numel(ECG_controller);

nonNanIndices1 = ~isnan(ECG_guide);

nonNanIndices2 = ~isnan(ECG_controller);

%% Interpolation

int_ECG1 = ECG_guide; % Copy original data

int_ECG1(~nonNanIndices1) = interp1(Indices1(nonNanIndices1), ECG_guide(nonNanIndices1), Indices1(~nonNanIndices1), 'linear');

int_ECG2 = ECG_controller; % Copy original data

int_ECG2(~nonNanIndices2) = interp1(Indices2(nonNanIndices2), ECG_controller(nonNanIndices2), Indices2(~nonNanIndices2), 'linear');

% Plot Interpolated Data with Highlights

figure(2);

title("Interpolated ECG Data");

plot(Indices1, int_ECG1, 'r', 'DisplayName', 'ECG Guide (Cleaned)');

hold on;

plot(Indices2, int_ECG2, 'b', 'DisplayName', 'ECG Controller (Cleaned)');

% Highlight interpolated points

interpPoints1 = Indices1(~nonNanIndices1);

interpPoints2 = Indices2(~nonNanIndices2);

plot(interpPoints1, int_ECG1(~nonNanIndices1), 'go', 'MarkerSize', 3, 'DisplayName', 'Interpolated (Guide)');

plot(interpPoints2, int_ECG2(~nonNanIndices2), 'go', 'MarkerSize', 3, 'DisplayName', 'Interpolated (Controller)');

legend();

hold off;
```