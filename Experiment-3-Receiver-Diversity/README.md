## 3. Develop a MATLAB simulation for receiver diversity systems.  

## AIM
To develop a MATLAB simulation for receiver diversity systems and analyze the improvement in signal reception using diversity techniques.

## APPARATUS REQUIRED
- MATLAB Software / GNU Octave
- Computer System

## THEORY
Receiver diversity is used in wireless communication to combat fading effects by combining signals received from multiple antennas or branches. Selection diversity chooses the strongest signal among multiple received signals to improve communication reliability.

## ALGORITHM
1. Start the program.
2. Generate random transmitted data.
3. Generate multiple Rayleigh fading channels.
4. Pass the signal through different diversity branches.
5. Apply receiver diversity combining.
6. Compare received signals.
7. Plot the output responses.
8. Stop the program.

## MATLAB CODE

```matlab
clc;
clear;
close all;

N=1000;

s=ones(1,N);

x1=randn(1,N);
y1=randn(1,N);

r1=sqrt(x1.^2+y1.^2);

x2=randn(1,N);
y2=randn(1,N);

r2=sqrt(x2.^2+y2.^2);

r=max(r1,r2);

subplot(3,1,1);
plot(r1);
title('Branch 1 Signal');
grid on;

subplot(3,1,2);
plot(r2);
title('Branch 2 Signal');
grid on;

subplot(3,1,3);
plot(r);
title('Selection Diversity Output');
grid on;
```

## OUTPUT
- Plot of Branch 1 signal.
- Plot of Branch 2 signal.
- Plot of Selection Diversity output.

<img width="539" height="409" alt="image" src="https://github.com/user-attachments/assets/2b63dbcb-0b92-4846-9949-dd76bc035cd7" />

## RESULT
Thus, the MATLAB simulation for receiver diversity systems was successfully developed and executed. The diversity technique improved received signal quality under fading conditions.
