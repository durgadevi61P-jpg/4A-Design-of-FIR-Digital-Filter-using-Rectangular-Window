# FIR-FILTER-DESIGN
# EXP 4 A: Design-of-FIR-Digital-Filter-using-Rectangular-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Rectangular-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ;
close ;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
alpha= (M -1)/2 // Center Value
for n = 1:M
if (n ==alpha+1)
hd(n) = Wc/ %pi ;
else
hd(n) = sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi);
end
end

for n = 1:M
W(n) = 1;
end
h = hd.*W;
disp(h,'Filter Coefficients are')
[hzm,fr]= frmag (h,256) ;
subplot(2 ,1 ,1)
plot(2*fr, hzm)
xlabel( ' Normalized Digital Frequency w');
ylabel( 'Magnitude ');
title( ' Frequency Response of FIR LPF using Rectangular Window ')
hzm_dB = 20* log10 (hzm);
subplot (2 ,1 ,2);
plot(2*fr , hzm_dB);
xlabel( ' Normalized Digital Frequency W' );
ylabel( 'Magnitude in dB');
title('Frequency Response of FIR LPF using Rectangular Window');
```

# OUTPUT: 
<img width="1637" height="1011" alt="image" src="https://github.com/user-attachments/assets/b12fc574-d8dc-4e90-b620-5e1442e17d72" />


# RESULT: 

Thus design of low pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ;
close ;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
alpha= (M -1)/2 // Center Value
for n = 1:M
if (n ==alpha+1)
hd(n)=1-Wc/ %pi ;
else
hd(n) =-sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi);
end
end
for n = 1:M
W(n) =1;
end
h = hd.*W;
disp(h,'Filter Coefficients are')
[hzm,fr]= frmag (h,256) ;
subplot(2 ,1 ,1)
plot(2*fr, hzm)
xlabel( ' Normalized Digital Frequency w');
ylabel( 'Magnitude ');
title( ' Frequency Response of FIR LPF using Rectangular Window ')
hzm_dB = 20* log10 (hzm);
subplot (2 ,1 ,2);
plot(2*fr , hzm_dB);
xlabel( ' Normalized Digital Frequency W' );
ylabel( 'Magnitude in dB');
title('Frequency Response of FIR HPF using Rectangular Window');
```

# OUTPUT: 
<img width="1820" height="1092" alt="Screenshot 2026-03-10 212932" src="https://github.com/user-attachments/assets/50c0d899-9292-40c1-be21-2f64334e0ca6" />



# RESULT: 
Thus design of HIGH pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ;
close ;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
Wc2=Wc(2);
Wc1=Wc(1);
alpha= (M -1)/2 // Center Value
for n = 1:M
if (n ==alpha+1)
hd(n) =(Wc2-Wc1)/%pi ;
else
hd(n) =((sin(Wc2 *((n -1)-alpha)))-(sin(Wc1 *((n -1)-alpha))))/(((n -1)-alpha)*%pi);
end
end
for n = 1:M
W(n) =1;
end
h = hd.*W;
disp(h,'Filter Coefficients are')
[hzm,fr]= frmag (h,256) ;
subplot(2 ,1 ,1)
plot(2*fr, hzm)
xlabel( ' Normalized Digital Frequency w');
ylabel( 'Magnitude ');
title( ' Frequency Response of FIR BPF using Rectangular Window ')
```

# OUTPUT: 
<img width="1766" height="946" alt="Screenshot 2026-03-10 215230" src="https://github.com/user-attachments/assets/b71c267e-1be5-4de4-bfca-71bda4f60c5d" />


# RESULT: 
Thus design of BAND pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ;
close ;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
Wc2=Wc(2);
Wc1=Wc(1);
alpha= (M -1)/2 // Center Value
for n = 1:M
if (n ==alpha+1)
hd(n) =1-((Wc2-Wc1)/%pi) ;
else
hd(n) =((sin(Wc1 *((n -1)-alpha)))-(sin(Wc2 *((n -1)-alpha))))/(((n -1)-alpha)*%pi);
end
end
for n = 1:M
W(n) =1;
end
h = hd.*W;
disp(h,'Filter Coefficients are')
[hzm,fr]= frmag (h,256) ;
subplot(2 ,1 ,1)
plot(2*fr, hzm)
xlabel( ' Normalized Digital Frequency w');
ylabel( 'Magnitude ');
title( ' Frequency Response of FIR BSF using Rectangular Window ')
hzm_dB = 20* log10 (hzm);
subplot (2 ,1 ,2);
plot(2*fr , hzm_dB);
xlabel( ' Normalized Digital Frequency W' );
ylabel( 'Magnitude in dB');
title('Frequency Response of FIR BSF using Rectangular Window');
```
# OUTPUT: 
<img width="1767" height="976" alt="Screenshot 2026-03-10 221004" src="https://github.com/user-attachments/assets/af67bbb5-f2f0-4005-b606-2684b42da1ce" />


# RESULT: 
Thus design of BAND STOP FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.
