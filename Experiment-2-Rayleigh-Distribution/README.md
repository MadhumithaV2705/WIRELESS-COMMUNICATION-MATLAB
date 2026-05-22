## 2. Develop a MATLAB program to generate Rayleigh distributed random variables.  

## AIM
To develop a MATLAB program to generate Rayleigh distributed random variables and plot their probability density function (PDF).

## APPARATUS REQUIRED
- MATLAB Software / GNU Octave
- Computer System

## THEORY
Rayleigh distribution is widely used in wireless communication to model multipath fading channels where there is no direct line-of-sight component. The distribution represents the statistical variation of signal amplitude.

## ALGORITHM
1. Start the program.
2. Define the number of random samples.
3. Define the Rayleigh distribution parameter σ.
4. Generate uniformly distributed random numbers.
5. Convert them into Rayleigh distributed random variables.
6. Plot histogram and theoretical PDF.
7. Display the generated distribution.
8. Stop the program.

## MATLAB CODE

```
clc;
clear;
close all;

N = 10000;
sigma = 2;

U = rand(1, N);

R = sigma * sqrt(-2 * log(1 - U));

nbins = 50;

[counts, centers] = hist(R, nbins);

binWidth = centers(2) - centers(1);

pdf_hist = counts / (N * binWidth);

bar(centers, pdf_hist, 'facecolor', [0.2 0.6 1], 'edgecolor', 'none');

hold on;

x = 0:0.01:15;

pdf_rayleigh = (x ./ sigma.^2) .* exp(-(x.^2) ./ (2 * sigma.^2));

plot(x, pdf_rayleigh, 'r', 'LineWidth', 2.5);

xlabel('Random Variable');
ylabel('Probability Density');

title('Rayleigh Distribution');

legend('Histogram', 'PDF Curve');

grid on;

axis([0 15 0 0.35]);
```

## OUTPUT
- Histogram of generated random variables.
- Theoretical Rayleigh PDF curve plotted together.

<img width="560" height="429" alt="image" src="https://github.com/user-attachments/assets/c8bf20af-5b55-4650-9133-4065f082a88e" />

## RESULT
Thus, the MATLAB program to generate Rayleigh distributed random variables was successfully developed and executed. The generated distribution matches the theoretical Rayleigh PDF.
