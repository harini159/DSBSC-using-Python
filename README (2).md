
# DSBSC using Python

EX NO: 6 DSBSC Modulation using NumPy and Matplotlib

AIM:

To implement and analyze phase modulation (PM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required:
1. Software: Python with NumPy and Matplotlib libraries 
2. Hardware: Personal Computer Theory

Note: Keep all the switch faults in off position


Algorithm:

1. Set Up the Python Environment: Ensure that Python is installed on your system. You can use 
Anaconda for managing Python packages and environments, or any other Python IDE of your choice. 
2. Import Necessary Libraries: Import the math library in Python. 
3. Initialize Parameters: 
o Set values for carrier amplitude (AcA_cAc), carrier frequency (fcf_cfc), message frequency 
(fmf_mfm), sampling frequency, and phase deviation sensitivity (kpk_pkp). 
4. Generate Time Axis: 
o Create a time vector for the signal duration based on the sampling frequency. 
5. Generate Message Signal: 
o Define the message signal as a cosine wave. 
6. Generate DSBSC Signal: 
o Apply the DSBSC modulation formula to obtain the modulated signal. 
7. Plot the Signals: 
o Use Matplotlib to plot the message signal, carrier signal, and DSBSC modulated signal. 

Program:
```
import numpy as np
import matplotlib.pyplot as plt
Am=2.20
fm=294
fs=29400
Ac=3.20
fc=2940
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1=(Ac+m)*np.cos(2*3.14*fc*t)
s2=(Ac-m)*np.cos(2*3.14*fc*t)
s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)
plt.tight_layout()
plt.show()
```

Model Waveform:

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

Output Graph:

<img width="786" height="581" alt="image" src="https://github.com/user-attachments/assets/63c7ee49-4891-4b5e-80e6-5123e18900c5" />

Tablular Column:

![WhatsApp Image 2025-10-21 at 8 54 13 PM](https://github.com/user-attachments/assets/eefd0bf9-0b49-4394-bfe3-3993d8c0b96a)

Result:
 
The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal. 



