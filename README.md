# IDEAL SAMPLING
# AIM
To perform construction and reconstruction of ideal sampling using python code.

# TOOLS REQUIRED
IDE python with scipy and numpy

# PROGRAM
```
#Impulse Sampling
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
```
# OUTPUT
![WhatsApp Image 2025-03-18 at 11 50 46_d49a22e7](https://github.com/user-attachments/assets/95751fad-0b2c-4977-ace1-dd34df2a7cdc)
![WhatsApp Image 2025-03-18 at 11 51 08_584bf7c9](https://github.com/user-attachments/assets/aaf304d2-0270-4709-95b5-eaeccd1e6517)
![WhatsApp Image 2025-03-18 at 11 51 23_f9475922](https://github.com/user-attachments/assets/a076ca76-83a5-49c8-bc38-3ce62e7f999a)

# RESULT
Thus the given construction and reconstruction of ideal sampling has been verified successfully.
