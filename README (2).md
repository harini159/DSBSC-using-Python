
# DSBSC using Python

EX NO: 6	DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using COLAB and study its spectral characteristics

EQUIPMENTS REQUIRED:

•	Computer with i3 Processor
•	Google COLAB

Note: Keep all the switch faults in off position


Algorithm:

1. Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.

PROCEDURE:

•	Refer Algorithms and write code for the experiment.
•	Open Google COLAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform


Model Waveform:

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />


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

Output Graph:

<img width="786" height="581" alt="image" src="https://github.com/user-attachments/assets/63c7ee49-4891-4b5e-80e6-5123e18900c5" />



Tablular Column:


Result:

Thus the DSB-SC-AM Modulation and Demodulation is generated.

