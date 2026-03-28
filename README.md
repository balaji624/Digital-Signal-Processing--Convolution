# Digital-Signal-Processing--Convolution
## Aim:
                  To perform linear convolution using MAT LAB.
## Software Required:
MAT LAB R2012
## Algorithm:
Step 1: Open mat lab. Write the program.

Step 2: Read the first input sequence.

Step 3: Read the second impulse sequence.

Step 4: Plot the input sequences with x-label and y-label with suitable title. 

Step 5: Perform convolution for both the sequences using conv2() function.
  
Step 6: Plot the sequence with x-label and y-label with suitable title

Step 7: Terminate the program.

## PROGRAM: 
```
%Balaji v 212223050008

clc;
clear all; 
close all; 

% input sequence
a=-3;
x=[2,-1,2.7,2.6,3,6,3,5,-2];
n=a:1:length(x)+a-1;
figure(1);
stem(n,x);
xlabel('time');
ylabel('amplitude');
title('input sequence');

%𝑥[𝑛]={2,−1,2.7,2.6,3 ,6,3,5,−2} and ℎ[𝑛]={3,2.5,−4,2.7,−3.5,2,4,1}
% -3 [2,-1,2.7,2.6,3 ,6,3,5,-2] -3 [3,2.5,-4,2.7,-3.5,2,4,1]

% impulse sequence
b=-3;
y=[3,2.5,-4,2.7,-3.5,2,4,1];
m=b:1:length(y)+b-1;
figure(2);
stem(m,y);
xlabel('time');
ylabel('amplitude');
title('impulse response')

% LINEAR CONVOLUTION
z=conv2(x,y);
n1=a+b:1:length (z)+a+b-1;
figure(3);
stem(n1,z);
xlabel('time');
ylabel('amplitude');
title('linear convolution');
```

## OUTPUT:
<img width="1919" height="1017" alt="Screenshot 2026-02-06 145515" src="https://github.com/user-attachments/assets/a453ef96-6ca9-416d-9bec-682f727e2c36" />
<img width="1919" height="1012" alt="Screenshot 2026-02-06 145640" src="https://github.com/user-attachments/assets/6940c40b-1c88-4756-9e0c-b4d637f2c29a" />
<img width="1919" height="1019" alt="Screenshot 2026-02-06 145218" src="https://github.com/user-attachments/assets/1421d167-49f0-4f6a-adc2-7bb52ba04f28" />





## RESULT:
The linear Convolution of Signal is y[n]={6,2,-2.4,23.95,-5,29.89,15.57,0.9,15.2,-18.8,37.6,10.1,35,19,-3,-2}

