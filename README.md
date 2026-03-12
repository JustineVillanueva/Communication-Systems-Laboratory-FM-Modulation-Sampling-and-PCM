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
![Experiment 9 Setup](Diagrams/Exp9-Diagrams/Exp9_Fig9.4.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 9 Results</summary>
  
**Part A: Frequency modulating a squarewave** 
![Experiment 9 FM Signal](Simulation/Exp9-Waveforms/Exp9_FM_signal.jpg)


**Part B: Genarating an FM signal using speech** 
![Experiment 9 FM Signal w/ Speech](Simulation/Exp9-Waveforms/Exp9_FM_signalwSpeech.jpg)

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

**Figure 11.3: Natural Sampling**
![Experiment 11 Setup](Diagrams/Exp11-Diagrams/Exp11_Fig11.3.jpg)


**Figure 11.5: Sample-and-Hold**
![Experiment 11 Setup](Diagrams/Exp11-Diagrams/Exp11_Fig11.5.jpg)


**Figure 11.8: Reconstruction**
![Experiment 11 Setup](Diagrams/Exp11-Diagrams/Exp11_Fig11.8.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 11 Result</summary>

**Natural Sampling**
![Experiment 11 Natural Sampling 1](Simulation/Exp11-Waveforms/Exp11_NaturalSampling1.jpg)
![Experiment 11 Natural Sampling 2](Simulation/Exp11-Waveforms/Exp11_NaturalSampling2.jpg)


**Sample and Hold**
![Experiment 11 Sample-and-Hold 1](Simulation/Exp11-Waveforms/Exp11_SH1.jpg)
![Experiment 11 Sample-and-Hold 2](Simulation/Exp11-Waveforms/Exp11_SH2.jpg)


**Reconstruction**
![Experiment 11 Reconstruction 1](Simulation/Exp11-Waveforms/Exp11_Reconstruction1.jpg)
![Experiment 11 Reconstruction 2](Simulation/Exp11-Waveforms/Exp11_Reconstruction2.jpg)

</details>

### Observation
In this experiment, different sampling methods such as natural sampling and sample-and-hold were explored. It was observed that natural sampling produced pulses that followed the shape of the original signal, while the sample-and-hold method maintained the sampled value for a short period, resulting in a step-like waveform. The sampled signal was then passed through a reconstruction filter, which smoothed the waveform and produced an output that closely resembled the original analog signal.

---
## Laboratory Experiment 12: PCM Encoding
This laboratory experiment covers the process of converting analog signals into digital signals through pulse code modulation (PCM).

### PCM Encoding Process
PCM encoding consists of three main steps:
- Sampling - Converting the continuous signal into discrete samples.
- Quantization – Approximating each sample to the nearest amplitude level.
- Encoding – Representing the quantized values as binary numbers.

### Circuit Diagram
<details>
  <summary>Experiment 12 Diagram</summary>

**Figure 12.3**
![Experiment 12 Setup](Diagrams/Exp12-Diagrams/Exp12_Fig12.3.jpg)


**Figure 12.6**
![Experiment 12 Setup](Diagrams/Exp12-Diagrams/Exp12_Fig12.6.jpg)


**Figure 12.8**
![Experiment 12 Setup](Diagrams/Exp12-Diagrams/Exp12_Fig12.8.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 12 Result</summary>

**Part A Results**

Step 6: Slope control at the "-" position
![Experiment 12 Part A-6](Simulation/Exp12-Waveforms/Exp12_A6.jpg)


Step 8: Timebase control changed to 0.1ms/div
![Experiment 12 Part A-8](Simulation/Exp12-Waveforms/Exp12_A8.jpg)


Step 12: PCM Encoder output connected to Channel 2
![Experiment 12 Part A-12](Simulation/Exp12-Waveforms/Exp12_A12.jpg)


End of Part A
![Experiment 12 Part A-End](Simulation/Exp12-Waveforms/Exp12_A_end.jpg)



**Part B Results**

Variable DC control in counter clockwise position
![Experiment 12 Part B-VDC C.CW](Simulation/Exp12-Waveforms/Exp12_B_CCW.jpg)


Variable DC control in clockwise position
![Experiment 12 Part B-VDC CW](Simulation/Exp12-Waveforms/Exp12_B_CW.jpg)



**Part D Result**

End of Part D
![Experiment 12 Part D-End](Simulation/Exp12-Waveforms/Exp12_D_end.jpg)

</details>

### Observation
The PCM encoder converted the analog input signal into a digital bitstream by sampling and quantizing the signal. Each sample was represented by a binary value, showing how analog information can be digitally transmitted. Minor differences between the original signal and the encoded output were observed due to quantization.

---
## Laboratory Experiment 13: PCM Decoding
This laboratory experiment covers the process of decoding PCM signals and reconstructing the original analog waveform.

### PCM Decoding Process
- The digital PCM signal is decoded back into quantized amplitude levels.
- A reconstruction filter smooths the stepped waveform.
- The resulting signal approximates the original analog message signal.

### Circuit Diagram
<details>
  <summary>Experiment 13 Diagram</summary>

**Part A: Setting up the PCM Encoder**

**Figure 13.2: PCM Data w/ variable DCV**
![Experiment 13 Setup](Diagrams/Exp13-Diagrams/Exp13_Fig13.2.jpg)


**Figure 13.4: PCM Data w/ VCO**
![Experiment 13 Setup](Diagrams/Exp13-Diagrams/Exp13_Fig13.4.jpg)



**Part B: Decoding the PCM data**

**Figure 13.6: PCM Encoding-Decoding**
![Experiment 13 Setup](Diagrams/Exp13-Diagrams/Exp13_Fig13.6.jpg)



**Part D: Recovering the message**

**Figure 13.11: PCM Encoding-Decoding-Reconstruction**
![Experiment 13 Setup](Diagrams/Exp13-Diagrams/Exp13_Fig13.11.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 13 Result</summary>

**Part A Result**

PCM Data
![Experiment 13 PCM Encoding](Simulation/Exp13-Waveforms/Exp13_A.png)



**Part B Result**

PCM Decoder
![Experiment 13 PCM Decoding](Simulation/Exp13-Waveforms/Exp13_B.png)



**Part D Result**

Modified set-up with reconstructed signal
![Experiment 13 Reconstruction](Simulation/Exp13-Waveforms/Exp13_D.png)

</details>

### Observation
In this experiment, a reconstructed message signal was obtained by first generating PCM data using a PCM encoder. The resulting bit stream was then passed through a PCM decoder, which converted the digital data back into its corresponding quantized levels. Finally, a low-pass filter was added to the circuit to reconstruct the signal, producing an output waveform that closely resembled the original signal.

---
## Laboratory Experiment 14: Bandwidth limiting and restoring digital signals
This laboratory experiment covers the effects of bandwidth limitations on digital signals and techniques used to restore degraded digital waveforms.

### Digital Signal Bandwidth Effects
- Limited bandwidth can cause signal distortion and intersymbol interference (ISI).
- Digital signals may lose sharp transitions due to filtering.
- Signal restoration techniques can reshape distorted waveforms.

### Circuit Diagram
<details>
  <summary>Experiment 14 Diagram</summary>

**Part A: The effects of bandwidth limiting on PCM decoding**

**Figure 14.4: PCM Encoding-Decoding**
![Experiment 14 Setup](Diagrams/Exp14-Diagrams/Exp14_Fig14.4.jpg)

**Figure 14.6: Tuneable Low-pass Filter module models the bandwidth limiting of the channel**
![Experiment 14 Setup](Diagrams/Exp14-Diagrams/Exp14_Fig14.4.jpg)



**Part B: The effects of bandwidth limiting on a digital signal's shape**

**Figure 14.8: Digital signal modeling - BW limited channel**
![Experiment 14 Setup](Diagrams/Exp14-Diagrams/Exp14_Fig14.8.jpg)

**Figure 14.10: Digital signal modeling - BW limited channel (Master Signal changed to VCO)**
![Experiment 14 Setup](Diagrams/Exp14-Diagrams/Exp14_Fig14.10.jpg)



**Part C: Restoring digital signals**

**Figure 14.12: The comparator is used to restore the bandwidth limited digital signal**
![Experiment 14 Setup](Diagrams/Exp14-Diagrams/Exp14_Fig14.12.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 14 Result</summary>

**Part A Result**

Step 12: Tuneable Low-Pass Filter module models bandwidth limiting of the channel
![Experiment 14 Part A](Simulation/Exp14-Waveforms/Exp14_A.png)

Step 13: VDC control is varied and Cut-off Frequency control is adjusted anti-clockwise
![Experiment 14 Part A](Simulation/Exp14-Waveforms/Exp14_A13.png)



**Part B Result**

Step 21: Sequence Generator is used to model a digital signal.
![Experiment 14 Part B](Simulation/Exp14-Waveforms/Exp14_B.png)

Step 25: Tuneable Low-pass Filter cut-off frequency control is adjusted anti-clockwise
![Experiment 14 Part B](Simulation/Exp14-Waveforms/Exp14_B25.png)

Step 29: The sequence generators's clk is provided by the VCO module's digital output
![Experiment 14 Part B](Simulation/Exp14-Waveforms/Exp14_B29.png)

Step 31: The VCO Frequency control is adjusted clockwise
![Experiment 14 Part B](Simulation/Exp14-Waveforms/Exp14_B31.png)



**Part C Result**

Step 36: The variable DC module's DC voltage control is varied and observed
![Experiment 14 Part C](Simulation/Exp14-Waveforms/Exp14_C36.png)

Step 40: Comparison of the restored digital signal with the bandwidth limited signal
![Experiment 14 Part C](Simulation/Exp14-Waveforms/Exp14_C40.png)


</details>

### Observation
In this experiment, the effects of bandwidth limiting on digital signals and PCM decoding were observed. I gained an understanding that when the signal passes through a bandwidth-limited channel, the shape of the digital waveform becomes distorted, with rounded edges and reduced sharp transitions between logic levels. This distortion made the signal less ideal for decoding. However, by using signal restoration techniques such as filtering or reshaping circuits, the digital waveform was improved and became closer to its original square form.

---
## Learnings Summary

These lab experiments highlighted how both analog and digital signals are transmitted, processed, and recovered in communication systems. In the FM modulation lab, I learned how information can be transmitted by varying the frequency of a carrier signal and how the original signal can be recovered through FM demodulation. The sampling experiments demonstrated how continuous analog signals can be converted into discrete samples and later reconstructed using low-pass filters. The PCM encoding and decoding labs further showed how analog signals can be digitized into binary data, transmitted, and then accurately reconstructed back into an analog waveform. Finally, the bandwidth limiting experiment illustrated how channel limitations can distort digital signals and affect decoding, and how restoration techniques can help recover the original waveform. Together, these labs emphasized the complete process of signal transmission, processing, and recovery in communication systems.
