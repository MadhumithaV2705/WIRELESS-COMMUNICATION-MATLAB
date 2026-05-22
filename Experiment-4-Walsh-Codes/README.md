## 4. Write a MATLAB code to generate Walsh codes for CDMA communication.  

## AIM
To write a MATLAB program to generate Walsh codes used in CDMA communication systems.

## APPARATUS REQUIRED
- MATLAB Software / GNU Octave
- Computer System

## THEORY
Walsh codes are orthogonal codes used in CDMA systems to separate users sharing the same frequency spectrum. Orthogonality minimizes interference between users.

## ALGORITHM
1. Start the program.
2. Define the order of Walsh matrix.
3. Initialize the basic Walsh matrix.
4. Generate Walsh codes recursively.
5. Display the generated Walsh matrix.
6. Stop the program.

## MATLAB CODE

```matlab
clc;
clear;
close all;

n=8;

W=hadamard(n);

disp('Walsh Codes:');
disp(W);

imagesc(W);

colormap(gray);

title('Walsh Code Matrix');

xlabel('Chip Number');

ylabel('Code Number');
```

## OUTPUT
- Display of Walsh code matrix.
- Gray-scale visualization of orthogonal Walsh codes.

<img width="551" height="423" alt="image" src="https://github.com/user-attachments/assets/d91b039e-e680-416d-a96c-813f6d629eca" />
<img width="565" height="333" alt="image" src="https://github.com/user-attachments/assets/c82db731-8f5f-4556-9fc8-716bf8577878" />

## RESULT
Thus, the MATLAB program to generate Walsh codes for CDMA communication was successfully developed and executed. The generated Walsh codes are orthogonal and suitable for multi-user CDMA systems.

