# Delta-Sigma Modulator – Cadence Virtuoso

This repository contains the design and simulation of a **first-order
Delta-Sigma (ΔΣ) Modulator** implemented using **Cadence Virtuoso**.
The modulator is constructed by **integrating previously designed and
verified blocks**, namely the **Comparator, Integrator, and Quantiser**.

## Tool Used
- Cadence Virtuoso (Analog Design Environment)
- Spectre Simulator

## Libraries Used
- comparator
- integrator
- quantiser
- delta_sigma_modulator

## Cells Included
- **slope_1** : Top-level Delta–Sigma modulator schematic

## Block-Level Description
The Delta-Sigma Modulator is implemented using the following blocks:

- **Integrator**  
  Accumulates the difference between the input signal and the feedback
  signal (sigma operation).

- **Quantiser (Comparator-based)**  
  Converts the integrator output into a 1-bit digital signal.

- **Comparator**  
  Used inside the quantiser to perform threshold-based decision making.

- **Feedback DAC (1-bit)**  
  Converts the quantiser output back into an analog level and feeds it
  to the summing node (delta operation).

## Architecture
The modulator follows a **first-order Delta-Sigma architecture**:
- Input summing node (error calculation)
- Integrator
- Quantiser
- 1-bit feedback DAC loop

This structure performs noise shaping and oversampling of the input
analog signal.

## Simulations
- Transient analysis
- Input: Analog signal (DC / ramp / sinusoidal)
- Output: High-frequency 1-bit digital bitstream
- The density of ones and zeros represents the input signal amplitude

## Delta–Sigma Modulator Schematic
Schematic of the first-order Delta–Sigma Modulator designed in Cadence Virtuoso.

![Delta Sigma Modulator Schematic](images/delta_sigma_schematic.png)

## Simulation Results
Transient simulation results showing the 1-bit digital output of the Delta–Sigma Modulator.

![Delta Sigma Modulator Output](images/delta_sigma_output.png)

## Project Team
This project was carried out as a **group mini-project**.

### Team Members
- Likhith Gowda H R
- Dhruthi Sridhar
- Adith Soragu
