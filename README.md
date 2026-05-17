# Laboratory 9 — Robotic Signal Smoothing
## 1 Hz Low-Pass Filter (RMS Envelope Detector)

---
## Group Information

#### Group 2 — Team Members

| Name | GitHub Profile |
|---|---|
| Mangali, Ma. Kristina Cassandra S. | [GitHub](#) |
| Nueva, Juliana Kyle L. | [GitHub](#) |
| Pomarejos, Sophia Moira Leigh M. | [GitHub](#) |
| Valencia, Pearl Marie N. | [GitHub](#) |

---
## Module Objectives

This laboratory activity aims to:

- To construct two 1 Hz Low Pass filters to produce two usable waveforms to control the EMG-powered robotic arm.
- Use the square wave generator built in Lab 1 as a test signal to determine the frequency response of the filters. 

---
##  BIOPAC Documentation & Data

### Circuit Function

[Explain the specific engineering purpose your circuit block plays in the overall robotic arm system. How does it process the bio-signal?]

>#### Engineering Purpose (eedit pa rin)

The RMS Envelope Detector: 
- Removes high-frequency noise and fluctuations
- Produces smoother control signals
- Improves robotic arm movement stability
- Converts raw EMG activity into usable motion control data

>#### Biomedical Relevance: (eedit pa rin)

In biomedical instrumentation, signal conditioning is critical for:

- Accurate muscle activity interpretation
- Noise reduction
- Safe actuator control
- Reliable human-machine interfacing

---
###  Schematics & Waveforms

>#### Circuit Schematics

```md
![Circuit Schematic](images/schematic.png)
```
_Short Description_

> #### BIOPAC Waveform Outputs

**EMG Channel 1 Low Pass:**

<p align="center">
  <img src="images/EMG%201.png" alt="EMG Channel 1 Low Pass" width="700">
</p>

_Short Description_

**EMG Channel 1 Waveform Selection from 10% to 90%:**

<p align="center">
  <img src="images/EMG%201_10-90.png" alt="EMG Channel 1 Waveform Selection from 10% to 90%" width="700">
</p>

_Short Description_

**EMG Channel 2 Low Pass:**

<p align="center">
  <img src="images/EMG%202.png" alt="EMG Channel 2 Low Pass" width="700">
</p>

_Short Description_

**EMG Channel 2 Waveform Selection from 10% to 90%:**

<p align="center">
  <img src="images/EMG%202_10-90.png" alt="EMG Channel 2 Waveform Selection from 10% to 90%" width="700">
</p>

_Short Description_
---

### Calculations & Frequency Response Analysis

>#### Low Pass Filter Measurements

<div align="center">

|  | P-P (mV) |
|---|---|
| **EMG Channel 1** |  |
| **EMG Channel 2** |  |

<b>Table 9.1 CH 1: 0.5Vpp Sq Wave</b>

</div>

<br>

<div align="center">

|  | P-P (mV) | Min (mV) | 10% of max. (mV)<br>(Calculate) | 90% of max. (mV)<br>(Calculate) |
|---|---|---|---|---|
| **EMG Channel 1** |  |  |  |  |
| **EMG Channel 2** |  |  |  |  |

<b>Table 9.2 CH 2: Low Pass Out</b>

</div>

---

>#### Calculations for 10% and 90% Values

<div align="center">

```text
10% Value = Min + (0.1 × P-P)

90% Value = Min + (0.9 × P-P)
```

</div>

**EMG Channel 1**

[Show calculations here]

**EMG Channel 2**

[Show calculations here]


---

>#### Low Pass Frequency Response

<div align="center">
	
 ### $f_h = \frac{0.35}{t_r}$

</div>

Where:

- $f_h = estimated low-pass frequency response  
- $t_r = rise time from 10% to 90%

<div align="center">
	
| Measurement | EMG Channel 1 | EMG Channel 2 |
|---|---|---|
| Delta T (s) |  |  |
| Low Pass Filter Frequency (Estimated) |  |  |

**Table 9.3**

</div>

_Guide Questions Answer this in  discussion format

- Does the calculated frequency response match the intended 1 Hz cutoff frequency?
- Explain why equivalent measurements may differ between the two low-pass filters.
_

---

>#### Gain and 3 dB Cutoff Frequency Calculations

**Gain**
<div align="center">

$$
Gain = \frac{V_{out}}{V_{in}}
$$

$$
Gain = 1
$$

</div>


_Explain pa konti: Since the circuit uses a unity-gain Sallen-Key low-pass filter configuration, the output voltage is approximately equal to the input voltage._

**Low-Pass 3 dB Cutoff Frequency Calculation**

Using:

<div align="center">

$$
f_c = \frac{1}{2\pi R\sqrt{C_1 C_2}}
$$

</div>

Given:

```text
R = 237 kΩ = 237000 Ω

C₁ = 0.47 µF = 0.47 × 10⁻⁶ F

C₂ = 1 µF = 1 × 10⁻⁶ F
```

Substitute:

<div align="center">

$$
f_c = \frac{1}{2\pi (237000)\sqrt{(0.47\times10^{-6})(1\times10^{-6})}}
$$

</div>

Calculate the Capacitor Term

<div align="center">

$$
\sqrt{(0.47 \times 10^{-6})(1 \times 10^{-6})}
$$

$$
= 6.855 \times 10^{-7}
$$

</div>

Substitute again:

<div align="center">

$$
f_c =
\frac{1}{2\pi (237000)(6.855 \times 10^{-7})}
$$

</div>

Final Answer:

<div align="center">

$$
f_c \approx 0.98 \text{ Hz}
$$

</div>


_Explain pa kontii Therefore, the theoretical 3 dB cutoff frequency of the low-pass filter is approximately 1 Hz.
_

---
## Video Presentation

### Demonstration Video

Insert your presentation/demo link below.

- 📺 YouTube: [Insert Link Here](#)
- 📁 Vimeo: [Insert Link Here](#)

---
## Group Conclusion

Provide a concise 1–2 paragraph summary discussing:

- Success of the RMS envelope detector implementation
- Performance of the 1 Hz low-pass filters
- Importance of signal conditioning in biomedical robotics
- Relevance to safe and accurate robotic arm control systems

---

## References

BIOPAC Systems, Inc. (2020). *BSL PRO Lesson H40: EMG-Powered Robotic Arm*. BIOPAC Systems, Inc.

---
## Repository Structure

```bash
LABORATORY-9/
│
├── README.md
├── schematics/
├── waveform-data/
├── fft-analysis/
├── calculations/
├── presentation/
└── documentation/
```

---
