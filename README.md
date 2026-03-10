# Communication Systems Laboratory: FM Modulation, Sampling, and PCM (Experiments 9–14)
### Objective
To study and analyze key principles of analog and digital communication systems through experiments on frequency modulation (FM) and demodulation, signal sampling and reconstruction, pulse code modulation (PCM) encoding and decoding, and techniques for bandwidth limiting and restoring digital signals.

---
### Materials / Components Used
- Emona Telecoms-Trainer 101 (ETT-101)
- Dual Channel 20MHz Oscilloscope
- ETT-101 Oscilloscope Leads
- ETT-101 Patch Leads

---
## Laboratory Experiment 9: Frequency Modulation
This laboratory experiment covers the basic principles and generation of frequency-modulated signals.

### FM Characteristics
- The frequency of the carrier varies according to the amplitude of the message signal.
- The amplitude of the FM signal remains constant, unlike amplitude modulation.
- Increasing the message amplitude results in a larger frequency deviation.
- FM signals provide better noise immunity compared to AM signals.

### Circuit Setup/Diagrams
<details>
  <summary>Experiment 9 Diagram</summary>
  
**Part A: Frequency modulating a squarewave** 
**Figure 9.4: FM Signal**

![Experiment 9 Setup](Simulation_images/Exp9-Diagrams/Exp9_Fig9.4.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 9 Results</summary>
  
**Part A: Frequency modulating a squarewave** 

![Experiment 9 Setup](Simulation_images/Exp9-Waveforms/Exp9_FM_signal.jpg)

**Part B: Genarating an FM signal using speech** 

![Experiment 9 Setup](Simulation_images/Exp9-Waveforms/Exp9_FM_signalwSpeech.jpg)

</details>

### Observation
The experiment demonstrated how the frequency of the carrier signal varies with the amplitude of the message signal. As the input signal amplitude increased, the frequency deviation of the carrier also increased while maintaining constant amplitude. This illustrates the fundamental behavior of frequency modulation in communication systems.

---
## Laboratory Experiment 10: FM Demodulation
This laboratory experiment covers the techniques used to recover the original message signal from an FM-modulated waveform.

### FM Demodulation Principle
- FM demodulation converts frequency variations back into voltage variations.
- The recovered signal represents the original message signal.

### Circuit Diagram
<details>
  <summary>Experiment 10 Diagram</summary>

**Figure 10.9: FM Modulator-Demodulator**

![Experiment 10 Setup](Diagrams/Exp10-Diagrams/Exp10_Fig10.9.jpg)

</details>

### Observation
In the Emona Telecoms Trainer 101, FM demodulation starts with a variable DC voltage (VDC) as the input signal, which is applied to the VCO (FM modulator). The VCO converts the input voltage into a frequency-modulated signal, which is routed through the trainer’s utilities to the Zero-Crossing Detector (ZCD). The ZCD converts the frequency variations into a pulse train, which is then passed through a baseband low-pass filter (LPF) to reconstruct the original signal. This process demonstrates how the FM signal is demodulated back into the original input voltage.

---
## Laboratory Experiment 11: Sampling and Reconstruction
This laboratory experiment covers the principles of signal sampling and the reconstruction of analog signals using the sampling theorem.

### Sampling Concept
- Sampling converts a continuous-time signal into discrete-time samples.
- Natural sampling multiplies the message signal by a periodic pulse train to obtain instantaneous samples.
- Sample-and-hold circuits capture and maintain the sampled amplitude until the next sample.
- According to the Nyquist Sampling Theorem, the sampling frequency must be at least twice the highest frequency of the signal.
- Aliasing occurs when the sampling rate is insufficient, causing higher-frequency components to appear as lower frequencies.
- Proper reconstruction of the signal requires a low-pass filter to recover the original analog waveform.

### Circuit Diagram
<details>
  <summary>Experiment 11 Diagram</summary>

**Figure 10.9: FM Modulator-Demodulator**

![Experiment 11 Setup](Diagrams/Exp11-Diagrams/Exp11_Fig10.9.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 11 Diagram</summary>

**Natural Sampling**

![Experiment 11 Setup](Diagrams/Exp11-Waveforms/Exp11_NaturalSampling1.jpg)
![Experiment 11 Setup](Diagrams/Exp11-Waveforms/Exp11_NaturalSampling2.jpg)

**Sample and Hold**

![Experiment 11 Setup](Diagrams/Exp11-Waveforms/Exp11_SH1.jpg)
![Experiment 11 Setup](Diagrams/Exp11-Waveforms/Exp11_SH2.jpg)

**Reconstruction**

![Experiment 11 Setup](Diagrams/Exp11-Waveforms/Exp11_Reconstruction1.jpg)
![Experiment 11 Setup](Diagrams/Exp11-Waveforms/Exp11_Reconstruction2.jpg)

</details>

---
## Learnings Summary

Through these experiments, I gained a deeper understanding of both analog and digital communication techniques. I learned how frequency modulation works and how the original message signal can be recovered through demodulation. Additionally, the experiments demonstrated how analog signals can be converted into digital form through sampling and PCM encoding, and how these signals can later be decoded and reconstructed. Finally, the effects of bandwidth limitations on digital signals highlighted the importance of signal restoration techniques in maintaining reliable communication systems.
