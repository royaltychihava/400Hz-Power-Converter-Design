## Overview
This project focuses on the design and simulation of a 400 Hz output power converter for aerospace and naval applications, where reduced size, weight, and high power quality are critical.

## Objective
To design a high-performance converter capable of maintaining precise voltage regulation and low harmonic distortion under varying load conditions.

---

## System Design

### Converter Topology
- 5-level cascaded H-bridge converter  
- Modular structure using two H-bridges  
- Reduced voltage stress on switching devices  
- Improved output waveform quality with lower harmonic distortion  

### Switching Strategy
- Unipolar phase-shifted PWM  
- Achieves high effective switching frequency  
- Reduces switching losses in high-power operation  

---

## Control Strategy

### Cascaded Control Structure
- Outer voltage loop: Proportional-Resonant (PR) controller tuned at 400 Hz  
- Inner current loop: Initially multi-resonant PR controller targeting 3rd, 5th, and 7th harmonics  

The inner controller suppresses low-order harmonics while the LC filter attenuates higher-order harmonics.

---

### Controller Simplification
It was observed that:
- Cascaded PR–PR control shows similar performance to PR (voltage) + P (current) control  

This reduced system complexity while maintaining performance.

---

## Filter Design

- LC filter selected to reduce both voltage and current harmonics  
- Inductor (L): smooths current  
- Capacitor (C): smooths voltage  

This ensures improved output waveform quality and reduced total harmonic distortion.

---

## Controller Design Methodology

- Controllers designed in the continuous-time (S-domain)  
- Parameters tuned using:
  - Bode plots  
  - Root locus analysis  
- MATLAB SISO Tool used for gain tuning  

Design objectives:
- Adequate gain margin  
- Sufficient phase margin  
- Stable pole placement in the left half-plane  

---

## Digital Implementation

- Controllers converted from S-domain to Z-domain  
- Discretization performed using Tustin method  
- Prewarping applied to preserve resonance characteristics  

MATLAB tools used:
- `c2d` function  

---

## Simulation and Validation

### Continuous-Time Validation
- Full system modeled and tested in Simulink  
- Verified controller performance under different operating conditions  

### Discrete-Time Validation
- Digital control implementation tested  
- Maintained performance consistency with continuous-time model  

---

## Performance Evaluation

- Tested under:
  - Linear loads  
  - Nonlinear loads  
  - Unbalanced three-phase loads  

- Achieved:
  - Stable voltage regulation  
  - Effective harmonic suppression  
  - Robust system performance  

---

## Tools Used
- MATLAB  
- Simulink  

---

## Files
- Thesis_Report.pdf  
- MATLAB scripts (controller design and discretization)  
- Simulink models (continuous and discrete systems)  

---

## Conclusion
This project demonstrates a complete design and simulation of a 400 Hz power converter, integrating multilevel converter topology, advanced control strategies, and digital implementation. The system achieves high power quality and reliable performance suitable for demanding applications.

---

## Author
Royalty Holyworth Chihava
