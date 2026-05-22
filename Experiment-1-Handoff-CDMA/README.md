## 1. Develop a MATLAB program to demonstrate soft handoff in CDMA systems. 

## AIM
To develop a MATLAB program to demonstrate soft handoff in a CDMA communication system by analyzing the received signal strength from two base stations and observing the handoff region.

## APPARATUS REQUIRED
- MATLAB Software / GNU Octave
- Computer System

## THEORY
In CDMA systems, soft handoff allows a mobile user to communicate simultaneously with more than one base station while moving between cells. This reduces call drops and improves communication quality. The handoff occurs when the received signal strengths from two base stations become nearly equal.

## ALGORITHM
1. Initialize the distance between two base stations.
2. Define the mobile station movement path.
3. Set transmitted power and path loss exponent.
4. Calculate distances from the mobile user to both base stations.
5. Compute received powers from both base stations.
6. Convert powers into dB scale.
7. Define the soft handoff threshold.
8. Identify the region where both received powers are nearly equal.
9. Plot received signal strengths versus distance.
10. Display the soft handoff region.

## MATLAB CODE

```matlab
clc;
clear;
close all;

d_total = 2000;
x = 0:10:d_total;

Pt = 1;
n = 4;
threshold = 3;

d1 = x;
d2 = d_total - x;

d1(1) = 1;
d2(end) = 1;

Pr1 = Pt ./ (d1.^n);
Pr2 = Pt ./ (d2.^n);

Pr1_dB = 10 * log10(Pr1);
Pr2_dB = 10 * log10(Pr2);

handoff_region = abs(Pr1_dB - Pr2_dB) <= threshold;

figure;
plot(x, Pr1_dB, 'b', 'LineWidth', 2);
hold on;

plot(x, Pr2_dB, 'r', 'LineWidth', 2);

plot(x(handoff_region), Pr1_dB(handoff_region), ...
'ko', 'MarkerFaceColor', 'g');

grid on;

xlabel('Mobile User Position (m)');
ylabel('Received Power (dB)');
title('Soft Handoff in CDMA System');

legend('Base Station 1', ...
'Base Station 2', ...
'Soft Handoff Region');
```

## OUTPUT
- Graph showing received signal strengths from two base stations.
- Soft handoff region highlighted near overlap area.

<img width="539" height="405" alt="image" src="https://github.com/user-attachments/assets/e86b66b7-c928-432d-b135-fa4a19c421f0" />

## RESULT
Thus, the MATLAB program to demonstrate soft handoff in a CDMA system was successfully implemented. The soft handoff region was observed where the mobile station maintained communication with both base stations simultaneously.

