# Experiment 2:A

# Design of Common Source (CS) Amplifier using 180nm Technology

## Aim
To design and simulate a **Common Source (CS) Amplifier using CMOS 180 nm technology** and analyze its **DC characteristics, AC gain, bandwidth and transient response**.

---

## Introduction
A **Common Source (CS) amplifier** is one of the most widely used MOSFET amplifier configurations in analog electronics.  
In this configuration, the **input signal is applied to the gate terminal**, the **output is taken from the drain**, and the **source terminal is common** to both input and output.

The CS amplifier provides:

- High voltage gain  
- High input impedance  
- Moderate output impedance  

It is widely used in **analog integrated circuits and signal amplification applications**.

---

## Design Specifications

| Parameter | Value |
|-----------|------|
| Technology | 180 nm |
| Supply Voltage (VDD) | 1.5 V |
| Drain Current (ID) | 200 µA |
| Load Capacitance (CL) | 1 pF |
| Power Dissipation | ≤ 0.5 mW |
| Channel Length (L) | 180 nm |

---

## Basic MOSFET Equations

Drain current equation:

ID = (1/2) μnCox (W/L) (VGS − VT)²

Overdrive voltage:

Vov = VGS − VT

Voltage gain:

Av = − gm RD

Gain in dB:

Av(dB) = 20 log(Av)

---

## Design Calculations

### Given Values

VDD = 1.5 V  
ID = 200 µA  
VT ≈ 0.36 V  

---

### Overdrive Voltage

Vov = 0.25 V

---

### Gate Source Voltage

Vgs = Vov + Vt  
Vgs = 0.25 + 0.36  
Vgs = **0.61 V**

---

### Gate Voltage

Vg = Vs + Vgs  
Vg = 0.2 + 0.61  

Vg ≈ **0.81 V**

---

## PMOS Load Calculations

PMOS threshold voltage

VTp = 0.39 V

Overdrive condition

Vov = Vsg − Vt

Vsg = 0.25 + 0.39  
Vsg = **0.64 V**

Gate voltage

Vg = VDD − Vsg  
Vg = 1.5 − 0.64  

Vg = **0.86 V**

---

## Transistor Width Calculation

Using MOSFET equation

ID = (1/2) μnCox (W/L)(VGS − VT)²

Rearranging

W = (2IDL) / (μnCox (VGS − VT)²)

Calculated transistor width

W ≈ **18 µm**

---

## Output Voltage

Vout = VDD/2 + 0.2  

Vout ≈ **0.95 V**

This ensures MOSFET operation in the **saturation region**.

---

# AC Analysis

AC analysis is used to determine the **frequency response and voltage gain of the amplifier**.

### Observed Results

| Parameter | Value |
|----------|------|
| Voltage Gain | 6 V/V |
| Gain (dB) | 15.7 dB |
| Bandwidth | 351.36 MHz |
| -3 dB Gain | 12.08 |

Gain in decibels

Av(dB) = 20 log(Av)

Av(dB) = 20 log(6)

Av(dB) ≈ **15.7 dB**

---

# Transient Analysis

Transient analysis verifies amplification using time-domain signals.

### Observed Values

Vin = **1.081 V**

Vout = **1.2047 V**

Gain calculation

Gain = (Vout − Vin) / 20 mV

Gain ≈ **6 V/V**

The output waveform is **180° phase shifted**, which confirms the behaviour of a **Common Source amplifier**.

---

# DC Transfer Characteristics

The DC transfer curve shows the relationship between **input voltage and output voltage**.

Three operating regions are observed:

1. Cutoff Region  
2. Saturation Region  
3. Triode Region  

Maximum gain occurs when the MOSFET operates in the **saturation region**.

---

# Results

| Parameter | Result |
|----------|--------|
| Supply Voltage | 1.5 V |
| Drain Current | 200 µA |
| Voltage Gain | 6 V/V |
| Gain (dB) | 15.7 dB |
| Bandwidth | 351 MHz |
| Output Voltage | 0.95 V |

---

# Inference

- The **Common Source amplifier using 180 nm CMOS technology** was successfully designed.
- The amplifier provides **high voltage gain and good bandwidth**.
- AC, DC and transient analyses confirm **proper amplification behaviour**.

---

# Conclusion

The **Common Source amplifier** was designed and simulated using **180 nm CMOS technology**.

The amplifier achieved:

Voltage Gain ≈ **6 V/V**  
Gain ≈ **15.7 dB**  
Bandwidth ≈ **351 MHz**

Hence the experiment successfully demonstrates the **operation and amplification capability of a MOSFET CS amplifier**.

---

