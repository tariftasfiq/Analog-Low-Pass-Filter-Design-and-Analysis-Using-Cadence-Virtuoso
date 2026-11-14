# Analog Low-Pass Filter Design and Analysis Using Cadence Virtuoso

## 📌 Project Overview

This repository documents the design, mathematical analysis, and simulation of different analog low-pass filter architectures using **Cadence Virtuoso**.

The project currently covers:

1. First-Order RC Low-Pass Filter
2. Sallen-Key Active Low-Pass Filter

The designs involve circuit schematic development, theoretical analysis, AC frequency-response analysis, transient simulation, and pole-zero analysis. The objective is to understand the characteristics of different low-pass filter architectures and verify their theoretical behavior through circuit-level simulations.

---

# 1. First-Order RC Low-Pass Filter

## Circuit Specifications

| Parameter | Value |
|---|---:|
| Resistor (R) | 1 MΩ |
| Capacitor (C) | 1 pF |
| AC Input Voltage | 1 V |
| Filter Type | First-Order RC Low-Pass Filter |
| Simulation Tool | Cadence Virtuoso |
| Simulation Environment | ADE L |

## Mathematical Calculation

The cutoff frequency of a first-order RC low-pass filter is:

$$
f_c = \frac{1}{2\pi RC}
$$

Substituting the component values:

$$
R = 1 \times 10^6 \ \Omega
$$

$$
C = 1 \times 10^{-12} \ F
$$

Therefore,

$$
f_c = \frac{1}{2\pi \times 10^6 \times 10^{-12}}
$$

The theoretical cutoff frequency is:

$$
\boxed{f_c \approx 159.154 \text{ kHz}}
$$

## AC Simulation Setup

| Setting | Value |
|---|---|
| Analysis Type | AC |
| Start Frequency | 1 Hz |
| Stop Frequency | 1 GHz |
| Sweep Type | Automatic |

### AC Simulation Results

The AC simulation demonstrates the expected low-pass filter characteristics:

- At low frequencies, the output closely follows the input.
- Near the cutoff frequency, the output begins to decrease.
- At higher frequencies, the capacitor increasingly attenuates the output signal.

### Theoretical vs. Simulated Results

| Parameter | Frequency |
|---|---:|
| Theoretical Cutoff Frequency | 159.154 kHz |
| Simulated Cutoff Frequency | 158.644 kHz |
| Difference | 0.510 kHz |

The simulated result closely matches the theoretical calculation.

## Pole-Zero Analysis

Pole-zero analysis was performed using ADE L to examine the filter's pole location.

For an ideal first-order RC low-pass filter, the transfer function is:

$$
H(s) = \frac{1}{1+sRC}
$$

The filter has one real pole at:

$$
s = -\frac{1}{RC}
$$

The pole determines the filter's natural frequency response and contributes to its first-order roll-off characteristics.

---

# 2. Sallen-Key Active Low-Pass Filter

## Project Overview

Designed and simulated a Sallen-Key active low-pass filter using Cadence Virtuoso. The design extends the project from passive RC filtering to active filter architectures, allowing investigation of frequency response, gain characteristics, and transient behavior.

## Circuit Design

The Sallen-Key topology uses an active amplifier stage together with an RC network to implement a low-pass filtering response.

**Design and simulation objectives:**

- Develop the Sallen-Key filter schematic in Cadence Virtuoso.
- Analyze the frequency-dependent gain and phase response.
- Investigate the loop-gain characteristics of the active circuit.
- Perform transient simulations to observe time-domain behavior.
- Examine the relationship between circuit parameters and filter performance.

## AC Frequency Response Analysis

AC analysis was performed to investigate the frequency-dependent behavior of the Sallen-Key filter.

The analysis focused on:

- Magnitude response.
- Phase response.
- Passband gain.
- Cutoff-frequency behavior.
- High-frequency attenuation.

### AC Response Plot

![Sallen-Key AC Frequency Response](Sallen-Key/ac_out.png)

## Loop-Gain Analysis

Loop-gain analysis was performed to examine the feedback characteristics and frequency-dependent behavior of the active filter circuit.

![Sallen-Key Loop Gain Analysis](Sallen-Key/loop%20gain.png)

## Transient Analysis

Transient simulation was performed to examine the time-domain response of the Sallen-Key filter under the applied input signal.

![Sallen-Key Transient Response](Sallen-Key/transient%20output.png)

## Design Implementation

The Sallen-Key filter was designed and simulated using Cadence Virtuoso. The simulation results were examined in both frequency and time domains to understand the behavior of the active filter architecture.

---

# 🛠️ Tools and Technologies

- Cadence Virtuoso
- Analog Design Environment (ADE L)
- GF180MCU
- IHP SG13G2
- AC Frequency Response Analysis
- Transient Analysis
- Pole-Zero Analysis
- Loop-Gain Analysis
- Analog Circuit Design

# 📚 Key Learning Outcomes

- Understanding passive and active low-pass filter architectures.
- Designing and analyzing first-order RC filters.
- Understanding Sallen-Key active filter topology.
- Performing AC frequency-response analysis.
- Investigating loop-gain and feedback characteristics.
- Performing transient simulations.
- Comparing theoretical filter characteristics with circuit-level simulation results.
- Developing practical experience with analog circuit design using Cadence Virtuoso.

---

## 👨‍💻 Author

**Sheikh Tariful Islam**

Electrical and Electronic Engineering  
Bangladesh University of Engineering and Technology (BUET)
