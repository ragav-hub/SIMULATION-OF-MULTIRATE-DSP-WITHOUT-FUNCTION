# EXP 6 : SPEECH RECOGNITION USING SCILAB

## AIM: 

To perform and verify multirate DSP without function using SCILAB.

## APPARATUS REQUIRED: 
PC installed with SCILAB. 

## PROGRAM : 

//  SPEECH RECOGNITION USING SCILAB
```
clear; 
clc; 
close; 
n = 0:%pi/50:2*%pi; 
 
x = sin(%pi*n); //original signal 
M=input('Enter the downsampling factor'); 
L=input('Enter the upsampling factor'); 
 
 
//Down Sampling 
 
downsampling_x = x(1:M:length(x)); 
disp(x,'Input signal x(n)='); 
disp(downsampling_x,'Downsampled Signal'); 
figure(1); 
subplot(2,1,1) 
plot2d3(1:length(x),x); 
xtitle('original singal') 
subplot(2,1,2) 

plot2d3(1:length(downsampling_x),downsampling_x); 
xtitle('Downsampled Signal by a factor of M'); 
 
 
//Upsampling 
upsampling_x=[]; 
for i=1:length(x) 
upsampling_x(1,L*i)=x(i); 
end 
disp(x,'Input signal x(n)='); 
disp(upsampling_x,'Upsampled Signal'); 
 
 
figure(2); 
subplot(2,1,1); 
plot2d3(x); 
title('original signal'); 
subplot(2,1,2); 
plot2d3(upsampling_x); 
title('Upsampled Signal by a factor of L');

```
## OUTPUT: 

<img width="1915" height="572" alt="image" src="https://github.com/user-attachments/assets/7e75715b-66f3-4bb5-89f9-fbf2d1cd63a2" />

<img width="1917" height="670" alt="image" src="https://github.com/user-attachments/assets/8475d622-e037-4fc6-bdda-5deba40aa049" />

<img width="1918" height="1135" alt="image" src="https://github.com/user-attachments/assets/510e46e8-4125-4b80-b15b-d3ebeb672d7e" />

<img width="1915" height="1143" alt="image" src="https://github.com/user-attachments/assets/203000d0-c817-42cd-8f36-71613ba9609c" />




## RESULT: 
Thus the decimation process by a factor M and interpolation process by a factor L using 
SCILAB was implemented. 
