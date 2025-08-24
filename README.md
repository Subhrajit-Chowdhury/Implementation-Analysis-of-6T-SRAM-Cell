# Implementation-Analysis-of-6T-SRAM-Cell
# SRAM 6T Cell

This repository demonstrates the design and simulation workflow for a standard 6-transistor (6T) SRAM cell, including schematic construction, DC analysis, and butterfly curve extraction using Cadence Virtuoso. Images from the TSMC 180nm process flow and Cadence environment are provided for reference.

***

## Overview

**SRAM (Static Random-Access Memory) 6T Cell** is a fundamental memory building block in digital and mixed-signal ICs. It comprises six MOSFETs configured to form a bistable latch capable of storing one bit of data.

***

## 6T SRAM Cell Circuit Diagram

The classic 6T SRAM cell schematic shows two CMOS inverters cross-coupled to preserve data, and access transistors (wordline-driven) for read/write operations. The typical layout includes internal storage nodes (`S1` and `S2`), bit-lines (`BL`, `BLB`), and a word-line (`WL`).

<img width="649" height="343" alt="Image" src="https://github.com/user-attachments/assets/826163f2-3a1d-4495-8118-a09a2da89dbf" />

***

## Cadence Schematic Implementation

The schematic below is implemented in Cadence Virtuoso, modeling both the PMOS and NMOS devices, and the required connections for bit-lines, word-line, storage nodes (`Q`, `Qbar`). The setup is compatible with TSMC 180nm design rules.

![Image](https://github.com/user-attachments/assets/73d71a23-4da8-476d-99a6-53a7018be2b0)


***

## DC Response Analysis

DC analysis is performed to study the voltage transfer characteristics of the cell, confirming its bistable nature and proper switching between logic states.

![Image](https://github.com/user-attachments/assets/c1569454-03c6-4567-be51-02a4c13bbe61)

***

## Butterfly Curve

The butterfly curve measures the cell's static noise margin (SNM), a key metric in memory robustness. Crossing points represent the stability thresholds.

![Image](https://github.com/user-attachments/assets/734fb470-5bc6-4749-89d5-8d1b90a0d63e)

***

## Features

- **Standard 6T topology**
- Cadence Virtuoso-compatible schematic
- DC transfer and butterfly plot for SNM
- Based on TSMC 180nm process
- Suitable for memory array and testbench integration

***

LTspice Schematic & Simulations
For cross-verification, the cell is simulated in LTspice. Setup includes appropriate pulse and voltage sources to model read/write cycles.

LTspice 6T SRAM Schematic:
![Image](https://github.com/user-attachments/assets/f698290c-35d6-409b-8e10-a272dd9bdfbb)


Waveform Analysis
Transient analysis reveals correct memory cell behavior during various read and write events:

![Image](https://github.com/user-attachments/assets/93e3ea66-c85c-4288-9c45-8c7793d583b5)

Static Noise Margin (SNM) Analysis
The classic "butterfly curve" is obtained by sweeping storage node voltages, which quantifies SRAM cell robustness to noise:

LTspice SNM Circuit:
![Image](https://github.com/user-attachments/assets/81601306-0aaf-4f5f-911a-3d4415d5de8f)

![Image](https://github.com/user-attachments/assets/c7e0e5c0-dcf7-4ce1-9217-5b64879498cc)
![Image](https://github.com/user-attachments/assets/d038b0fd-1626-4ce2-93de-65a4a62730a2)

References & Getting Started
See the main branch for scripts, source files, and netlists.

Open corresponding schematic files in Cadence Virtuoso or LTspice to reproduce results.

For further analysis, refer to documentation and built-in simulation commands.

## Notes

- For layout work, follow TSMC 180nm LDE guidelines.
- The images are exemplary output from Cadence and do not include netlist/LVS data.
- Further extension: integrate into larger memory arrays, enable PVT analysis, and perform layout vs. schematic checks.

***

## Acknowledgments

Images and simulation data generated using **Cadence Virtuoso** and aligned with **TSMC 180nm** process specifications.

***

