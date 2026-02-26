
## Experiment – 1

# DESIGN OF COMMON SOURCE (CS) AMPLIFIER USING 180nm TECHNOLOGY


---

# 1. AIM

To design and analyze a Common Source (CS) Amplifier using 180nm CMOS technology and verify its performance using DC, AC and Transient analysis.

---

# 2. GIVEN SPECIFICATIONS

VDD = 1.5V  
VT = 0.36V  
ID = 200µA  
Technology = 180nm  
Channel Length (L) = 180nm  
Chosen VGS = 0.9V  

---

# 3. THEORY

## 3.1 Common Source Amplifier

A Common Source (CS) amplifier is a basic MOSFET amplifier configuration where:

- Input is applied at Gate
- Output is taken from Drain
- Source is grounded
- It provides voltage gain
- Output is 180° phase shifted (inverted)

---
## Circuit Analysis

## DC Analysis

<img width="957" height="783" alt="Screenshot 2026-02-26 201327" src="https://github.com/user-attachments/assets/73050e04-ed89-41e0-96e0-b1f449b5df9c" />
## Transient Analysis

vin

<img width="1920" height="1200" alt="Screenshot 2026-02-26 201449" src="https://github.com/user-attachments/assets/0fc633dc-645d-4355-82c1-820524a110bb" />
vout

<img width="1920" height="1200" alt="Screenshot 2026-02-26 201606" src="https://github.com/user-attachments/assets/a3711a70-cc1d-4ca1-bb26-a9da85b2a23b" />

## AC Analysis
<img width="1920" height="1200" alt="Screenshot 2026-02-26 201805" src="https://github.com/user-attachments/assets/b8d39e33-9aca-41d0-a5bc-d03a165a9d3d" />



## 3.2 MosFET in Saturation Region

For amplification, MOSFET must operate in saturation region.

Condition:

VDS ≥ (VGS − VT)

Drain current equation in saturation:

ID = (1/2) μnCox (W/L) (VGS − VT)^2

Where:

μn = Electron mobility  
Cox = Oxide capacitance  
W = Width  
L = Length  

---

## 3.3 Small Signal Gain

Transconductance:

gm = 2ID / (VGS − VT)

Voltage Gain:

Av = -gm RD

Gain in dB:

Gain(dB) = 20 log10 |Av|

---

## 3.4 Bandwidth

Bandwidth at -3dB point:

BW = f(-3dB)

Gain Bandwidth Product:

GBW = Av × BW

---

# 4. DESIGN CALCULATIONS

---

## 4.1 Choosing Operating Point

To allow maximum symmetrical swing:

VD = VDD / 2

VD = 1.5 / 2  
VD = 0.75V

---

## 4.2 Drain Resistor Calculation

RD = (VDD − VD) / ID

RD = (1.5 − 0.75) / 200µA  
RD = 0.75 / 200 × 10⁻⁶  
RD = 3.75kΩ

---

## 4.3 Width Calculation

Using saturation equation:

ID = (1/2) μnCox (W/L) (VGS − VT)^2

Rearranging:

W = (2 ID L) / (μnCox (VGS − VT)^2)

Given:

μnCox ≈ 230.5 µ  
L = 180nm  
VGS = 0.9V  
VT = 0.36V  

Substituting:

W ≈ 1.07µm

---

# 5. PARAMETER SUMMARY

| Parameter | Value |
|------------|--------|
| VDD | 1.5V |
| VT | 0.36V |
| ID | 200µA |
| RD | 3.75kΩ |
| L | 180nm |
| W | 1.07µm |
| VGS | 0.9V |

---

# 6. SMALL SIGNAL ANALYSIS

## 6.1 Transconductance

gm = 2ID / (VGS − VT)

gm = 2 × 200µA / (0.9 − 0.36)

gm ≈ 0.00074 S

---

## 6.2 Voltage Gain

Av = gm RD

Av = 0.00074 × 3750

Av ≈ 2.47

---

## 6.3 Gain in dB

Gain(dB) = 20 log10(2.47)

Gain ≈ 8.84 dB

---

# 7. AC ANALYSIS RESULTS

Midband Gain ≈ 2.47  
Gain ≈ 8.84 dB  

-3dB Bandwidth ≈ 477 kHz  

Gain Bandwidth Product:

GBW = Av × BW  
GBW = 2.47 × 477 kHz  

GBW ≈ 982 kHz  

---

# 8. TRANSIENT ANALYSIS

Input: Small sinusoidal signal  
Output: Amplified and inverted waveform  

Observed:

Vin ≈ 19.4mV  
Vout ≈ 43.82mV  

Voltage Gain ≈ 2.25 – 2.47  

Output is 180° phase shifted.

---

# 9. DC ANALYSIS

Operating point:

VD ≈ 0.75V  
ID ≈ 200µA  

MOSFET satisfies:

VGS > VT  
Device operates in saturation region.

---

# 10. CIRCUIT DESCRIPTION

Components used:

- NMOS (180nm)
- Drain Resistor RD = 3.75kΩ
- Supply VDD = 1.5V
- Input at Gate
- Source grounded

---

# 11. ADVANTAGES

- Simple design
- Moderate voltage gain
- Good bandwidth
- Low power operation

---

# 12. APPLICATIONS

- Analog front-end circuits
- Signal amplification
- CMOS analog design
- Pre-amplifier stages

---

# 13. CONCLUSION

A Common Source amplifier was successfully designed using 180nm CMOS technology.

The amplifier achieved:

- Voltage Gain ≈ 2.47
- Gain ≈ 8.84 dB
- Bandwidth ≈ 477 kHz
- GBW ≈ 982 kHz

The MOSFET operated correctly in saturation region and showed proper inversion with stable gain.

---

# 14. RESULTS

The designed Common Source (CS) Amplifier using 180nm technology produced the following results:

## 14.1 DC Analysis Results

- Drain Voltage (VD) ≈ 0.75V  
- Drain Current (ID) ≈ 200µA  
- Gate-Source Voltage (VGS) = 0.9V  
- Threshold Voltage (VT) = 0.36V  

Since VGS > VT and VDS ≥ (VGS − VT),  
the MOSFET operates in Saturation Region.

---

## 14.2 Small Signal Results

- Transconductance (gm) ≈ 0.00074 S  
- Voltage Gain (Av) ≈ 2.47  
- Gain in dB ≈ 8.84 dB  

The amplifier provides moderate voltage amplification.

---

## 14.3 AC Analysis Results

- Midband Gain ≈ 2.47  
- -3dB Bandwidth ≈ 477 kHz  
- Gain Bandwidth Product (GBW) ≈ 982 kHz  

The frequency response shows a flat midband region followed by roll-off after the cutoff frequency.

---

## 14.4 Transient Analysis Results

- Input amplitude ≈ 19.4 mV  
- Output amplitude ≈ 43.82 mV  
- Output waveform is inverted (180° phase shift)  

This confirms proper amplification behavior of CS configuration.

---

# 15. INFERENCE

1. The Common Source amplifier was successfully designed using 180nm CMOS technology.

2. The MOSFET operates in saturation region as required for amplification.

3. The output signal is amplified and inverted, confirming theoretical behavior of CS amplifier.

4. The measured gain (2.47) matches closely with theoretical calculations.

5. The -3dB bandwidth of 477 kHz indicates good frequency response for low-power applications.

6. Gain Bandwidth Product (~982 kHz) verifies the trade-off between gain and frequency.

7. The design demonstrates stable operation at low supply voltage (1.5V).

Hence, the CS amplifier design meets the required specifications and validates theoretical calculations through simulation results.

---
