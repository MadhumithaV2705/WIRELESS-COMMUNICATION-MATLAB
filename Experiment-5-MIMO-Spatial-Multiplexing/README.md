
# 📘 EXPERIMENT 5

# Spatial Multiplexing in MIMO Communication Using MATLAB

## AIM
To write a MATLAB program for spatial multiplexing in MIMO communication systems.

---

## APPARATUS REQUIRED
- MATLAB Software / GNU Octave
- Computer System

---

## THEORY
Spatial multiplexing is a MIMO technique that transmits multiple data streams simultaneously through multiple antennas. It increases channel capacity and data transmission speed without requiring additional bandwidth.

---

## ALGORITHM
1. Start the program.
2. Generate random binary input data.
3. Modulate the data using BPSK.
4. Create a MIMO channel matrix.
5. Transmit data through multiple antennas.
6. Add noise to the received signal.
7. Recover transmitted data using Zero Forcing detection.
8. Plot transmitted and received signals.
9. Stop the program.

---

## MATLAB CODE

```matlab
clc;
clear;
close all;

N=1000;

data1=randi([0 1],1,N);
data2=randi([0 1],1,N);

x1=2*data1-1;
x2=2*data2-1;

X=[x1;x2];

H=randn(2,2);

Y=H*X;

N0=0.5*randn(2,N);

Y=Y+N0;

X_hat=inv(H)*Y;

rx1=X_hat(1,:)>0;
rx2=X_hat(2,:)>0;

subplot(2,1,1);
plot(data1(1:100),'b');

title('Transmitted Data');

grid on;

subplot(2,1,2);
plot(rx1(1:100),'r');

title('Received Data after Spatial Multiplexing');

grid on;
```

---

## OUTPUT
- Plot of transmitted binary data.
- Plot of received data after MIMO spatial multiplexing.

---

## RESULT
Thus, the MATLAB program for spatial multiplexing in MIMO communication was successfully developed and executed. The simulation demonstrates parallel transmission and successful recovery of data using MIMO techniques.

---
