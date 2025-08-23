# Implementation-Analysis-of-6T-SRAM-Cell
# SRAM 6T Cell: README

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

## Getting Started

1. Open the included schematic in Cadence Virtuoso.
2. Run DC analysis for transfer curve inspection.
3. Extract SNM using the butterfly curve method as shown in the images.

***

## Workflow Recap

- Refer to the topological diagram for transistor connectivity.
- Use Virtuoso for schematic drawing and simulation setup.
- Verify cell operation with DC sweep and analyze noise margins.

***

## Notes

- For layout work, follow TSMC 180nm LDE guidelines.
- The images are exemplary output from Cadence and do not include netlist/LVS data.
- Further extension: integrate into larger memory arrays, enable PVT analysis, and perform layout vs. schematic checks.

***

## Acknowledgments

Images and simulation data generated using **Cadence Virtuoso** and aligned with **TSMC 180nm** process specifications.

***

