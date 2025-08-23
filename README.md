# Implementation-Analysis-of-6T-SRAM-Cell
# SRAM 6T Cell: README

This repository demonstrates the design and simulation workflow for a standard 6-transistor (6T) SRAM cell, including schematic construction, DC analysis, and butterfly curve extraction using Cadence Virtuoso. Images from the TSMC 180nm process flow and Cadence environment are provided for reference.

***

## Overview

**SRAM (Static Random-Access Memory) 6T Cell** is a fundamental memory building block in digital and mixed-signal ICs. It comprises six MOSFETs configured to form a bistable latch capable of storing one bit of data.

***

## 6T SRAM Cell Circuit Diagram

The classic 6T SRAM cell schematic shows two CMOS inverters cross-coupled to preserve data, and access transistors (wordline-driven) for read/write operations. The typical layout includes internal storage nodes (`S1` and `S2`), bit-lines (`BL`, `BLB`), and a word-line (`WL`).

![SRAM 6T Schematic Reference][1]

***

## Cadence Schematic Implementation

The schematic below is implemented in Cadence Virtuoso, modeling both the PMOS and NMOS devices, and the required connections for bit-lines, word-line, storage nodes (`Q`, `Qbar`). The setup is compatible with TSMC 180nm design rules.

![SRAM 6T Cadence Schematic][2]

***

## DC Response Analysis

DC analysis is performed to study the voltage transfer characteristics of the cell, confirming its bistable nature and proper switching between logic states.

![SRAM 6T DC Response][3]

***

## Butterfly Curve

The butterfly curve measures the cell's static noise margin (SNM), a key metric in memory robustness. Crossing points represent the stability thresholds.

![SRAM 6T Butterfly Curve & SNM Extraction][4]

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

For questions or detailed setup, please contact the repository maintainer.

[1](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/images/52466036/bdee8ab4-bc7c-43e0-93ba-782d6bcf847a/425996657-c22930fc-f396-4787-807d-51088ad7959e.jpg?AWSAccessKeyId=ASIA2F3EMEYE4VI364WF&Signature=7pof0IVIhSpokZ3BaSmjzFxmndU%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEM7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJIMEYCIQDlIg3vYmllsIsxK0tL9iUBS2UKgmWav1KTD3e2WOeldAIhAPe%2FwVRyudPLIkrpFg5X5ax2zHnJlyr6a66asCTONZOnKvEECCYQARoMNjk5NzUzMzA5NzA1Igwcy2NlrPoiAmic7loqzgRgqBxXbLc%2BH3PH%2F8xRKQDGHbiITps4jxS2obMlXa4g4mHuXUW1wUKjZj5OqEY%2B4BXdHSQ43w0DCxSflaFO8zRG5vIKNORDq2L7WeL7ljJ9WJZ5tumUh3vkFKdzjZ10gCxsBx5xm8ztsn1NVaVCVjWAtvQZrMwnvUKHNbGV5MJEA5syXAYu3BYWOuvyfQu0R%2BdkxiGYB1eRJxATcqVjTe9k%2Fa38uuRsX%2FgdRyst42boRjahqtWNnrcztN3OhvOSQaJfMfhQXnWiOUEsVJrxZd25A2WxD7JU%2Fbb%2BwQhzKoegSMVX0wr53wxSlKmHpwaii7lHZ%2FlYIabcgI3XsLBdoVK9BofVoF3om3xefAlDeJeT5gWiZWEuRaeUlELDe39T258xdOCI%2FZ0g%2Fi56q1VRZEajzSyC1Vat3xWqAPuv8i53a7yVn5It8FYOnMvhkzJ6fQVKXIt7oyw8H0anlZKwDYJHGODI6QW2kEWuRd7GghjcR%2B6UZad29SOVmtV2cy9Pyz2bJoldB4w3Rv2jmXVFfnYoOYfk1hpu1%2F9aFmLCmsQwUmNwDlp3f9LU3aypcBeoq7%2FvQosUEkIdN0fzcuDuJvNEg11Lbyw0s9koL2DULOBplTIyRch5n1CfFJBrTI3DXu4EJLIJRXMfV1Pd5fOVO8kDdoTJRREQq8zE4bESliBbNA8z0mAbevhZBAhVeCLsSBl9drx1eSjBtXMK%2BfaZT3HthF05kOUh7pyKOrZB3DPekQF27UrAdozlVdZ799QkSS6yo%2BnX%2FzWU3%2BUPEFsT6TDOnaXFBjqZAdIKwQjS4Quh%2F1RYKaKZZN%2FhtUD9JdwjI0jXD5huJJU%2FQJwCE16NGilTwb7U0ANn5vnc27kJ3ny9dECkB7XQB6vH2mR5OnkBaGIQMH3MnDCG9lB2C2nOnI3hMQYFP8xRm6sc%2BzZ20MrJzImnQEgmZYoTNovRxeQucPRukxF1ORTjIXhSSViFkkvyxizdmtHHHst51a%2Fm83%2F52A%3D%3D&Expires=1755927089)
[2](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/images/52466036/b9ed3e1c-0766-4c9b-9f2d-fa3491933c20/SRAM_6T_Cadence__Schematic.jpg?AWSAccessKeyId=ASIA2F3EMEYE4VI364WF&Signature=9ueahjrtRv2yITYA06mDdgoRT6M%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEM7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJIMEYCIQDlIg3vYmllsIsxK0tL9iUBS2UKgmWav1KTD3e2WOeldAIhAPe%2FwVRyudPLIkrpFg5X5ax2zHnJlyr6a66asCTONZOnKvEECCYQARoMNjk5NzUzMzA5NzA1Igwcy2NlrPoiAmic7loqzgRgqBxXbLc%2BH3PH%2F8xRKQDGHbiITps4jxS2obMlXa4g4mHuXUW1wUKjZj5OqEY%2B4BXdHSQ43w0DCxSflaFO8zRG5vIKNORDq2L7WeL7ljJ9WJZ5tumUh3vkFKdzjZ10gCxsBx5xm8ztsn1NVaVCVjWAtvQZrMwnvUKHNbGV5MJEA5syXAYu3BYWOuvyfQu0R%2BdkxiGYB1eRJxATcqVjTe9k%2Fa38uuRsX%2FgdRyst42boRjahqtWNnrcztN3OhvOSQaJfMfhQXnWiOUEsVJrxZd25A2WxD7JU%2Fbb%2BwQhzKoegSMVX0wr53wxSlKmHpwaii7lHZ%2FlYIabcgI3XsLBdoVK9BofVoF3om3xefAlDeJeT5gWiZWEuRaeUlELDe39T258xdOCI%2FZ0g%2Fi56q1VRZEajzSyC1Vat3xWqAPuv8i53a7yVn5It8FYOnMvhkzJ6fQVKXIt7oyw8H0anlZKwDYJHGODI6QW2kEWuRd7GghjcR%2B6UZad29SOVmtV2cy9Pyz2bJoldB4w3Rv2jmXVFfnYoOYfk1hpu1%2F9aFmLCmsQwUmNwDlp3f9LU3aypcBeoq7%2FvQosUEkIdN0fzcuDuJvNEg11Lbyw0s9koL2DULOBplTIyRch5n1CfFJBrTI3DXu4EJLIJRXMfV1Pd5fOVO8kDdoTJRREQq8zE4bESliBbNA8z0mAbevhZBAhVeCLsSBl9drx1eSjBtXMK%2BfaZT3HthF05kOUh7pyKOrZB3DPekQF27UrAdozlVdZ799QkSS6yo%2BnX%2FzWU3%2BUPEFsT6TDOnaXFBjqZAdIKwQjS4Quh%2F1RYKaKZZN%2FhtUD9JdwjI0jXD5huJJU%2FQJwCE16NGilTwb7U0ANn5vnc27kJ3ny9dECkB7XQB6vH2mR5OnkBaGIQMH3MnDCG9lB2C2nOnI3hMQYFP8xRm6sc%2BzZ20MrJzImnQEgmZYoTNovRxeQucPRukxF1ORTjIXhSSViFkkvyxizdmtHHHst51a%2Fm83%2F52A%3D%3D&Expires=1755927089)
[3](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/images/52466036/23992b49-0637-455a-b0aa-c3e58bde052c/DC-response.jpg?AWSAccessKeyId=ASIA2F3EMEYE4VI364WF&Signature=yjObYips%2F6ZODXuS2HQSz1dwcpk%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEM7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJIMEYCIQDlIg3vYmllsIsxK0tL9iUBS2UKgmWav1KTD3e2WOeldAIhAPe%2FwVRyudPLIkrpFg5X5ax2zHnJlyr6a66asCTONZOnKvEECCYQARoMNjk5NzUzMzA5NzA1Igwcy2NlrPoiAmic7loqzgRgqBxXbLc%2BH3PH%2F8xRKQDGHbiITps4jxS2obMlXa4g4mHuXUW1wUKjZj5OqEY%2B4BXdHSQ43w0DCxSflaFO8zRG5vIKNORDq2L7WeL7ljJ9WJZ5tumUh3vkFKdzjZ10gCxsBx5xm8ztsn1NVaVCVjWAtvQZrMwnvUKHNbGV5MJEA5syXAYu3BYWOuvyfQu0R%2BdkxiGYB1eRJxATcqVjTe9k%2Fa38uuRsX%2FgdRyst42boRjahqtWNnrcztN3OhvOSQaJfMfhQXnWiOUEsVJrxZd25A2WxD7JU%2Fbb%2BwQhzKoegSMVX0wr53wxSlKmHpwaii7lHZ%2FlYIabcgI3XsLBdoVK9BofVoF3om3xefAlDeJeT5gWiZWEuRaeUlELDe39T258xdOCI%2FZ0g%2Fi56q1VRZEajzSyC1Vat3xWqAPuv8i53a7yVn5It8FYOnMvhkzJ6fQVKXIt7oyw8H0anlZKwDYJHGODI6QW2kEWuRd7GghjcR%2B6UZad29SOVmtV2cy9Pyz2bJoldB4w3Rv2jmXVFfnYoOYfk1hpu1%2F9aFmLCmsQwUmNwDlp3f9LU3aypcBeoq7%2FvQosUEkIdN0fzcuDuJvNEg11Lbyw0s9koL2DULOBplTIyRch5n1CfFJBrTI3DXu4EJLIJRXMfV1Pd5fOVO8kDdoTJRREQq8zE4bESliBbNA8z0mAbevhZBAhVeCLsSBl9drx1eSjBtXMK%2BfaZT3HthF05kOUh7pyKOrZB3DPekQF27UrAdozlVdZ799QkSS6yo%2BnX%2FzWU3%2BUPEFsT6TDOnaXFBjqZAdIKwQjS4Quh%2F1RYKaKZZN%2FhtUD9JdwjI0jXD5huJJU%2FQJwCE16NGilTwb7U0ANn5vnc27kJ3ny9dECkB7XQB6vH2mR5OnkBaGIQMH3MnDCG9lB2C2nOnI3hMQYFP8xRm6sc%2BzZ20MrJzImnQEgmZYoTNovRxeQucPRukxF1ORTjIXhSSViFkkvyxizdmtHHHst51a%2Fm83%2F52A%3D%3D&Expires=1755927089)
[4](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/images/52466036/864dd454-e6a0-4b0b-b30d-537450beacd7/Butterfly-Curve.jpg?AWSAccessKeyId=ASIA2F3EMEYE4VI364WF&Signature=KxPvFEOtwN1Zy64YP5d1QNdiJZQ%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEM7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJIMEYCIQDlIg3vYmllsIsxK0tL9iUBS2UKgmWav1KTD3e2WOeldAIhAPe%2FwVRyudPLIkrpFg5X5ax2zHnJlyr6a66asCTONZOnKvEECCYQARoMNjk5NzUzMzA5NzA1Igwcy2NlrPoiAmic7loqzgRgqBxXbLc%2BH3PH%2F8xRKQDGHbiITps4jxS2obMlXa4g4mHuXUW1wUKjZj5OqEY%2B4BXdHSQ43w0DCxSflaFO8zRG5vIKNORDq2L7WeL7ljJ9WJZ5tumUh3vkFKdzjZ10gCxsBx5xm8ztsn1NVaVCVjWAtvQZrMwnvUKHNbGV5MJEA5syXAYu3BYWOuvyfQu0R%2BdkxiGYB1eRJxATcqVjTe9k%2Fa38uuRsX%2FgdRyst42boRjahqtWNnrcztN3OhvOSQaJfMfhQXnWiOUEsVJrxZd25A2WxD7JU%2Fbb%2BwQhzKoegSMVX0wr53wxSlKmHpwaii7lHZ%2FlYIabcgI3XsLBdoVK9BofVoF3om3xefAlDeJeT5gWiZWEuRaeUlELDe39T258xdOCI%2FZ0g%2Fi56q1VRZEajzSyC1Vat3xWqAPuv8i53a7yVn5It8FYOnMvhkzJ6fQVKXIt7oyw8H0anlZKwDYJHGODI6QW2kEWuRd7GghjcR%2B6UZad29SOVmtV2cy9Pyz2bJoldB4w3Rv2jmXVFfnYoOYfk1hpu1%2F9aFmLCmsQwUmNwDlp3f9LU3aypcBeoq7%2FvQosUEkIdN0fzcuDuJvNEg11Lbyw0s9koL2DULOBplTIyRch5n1CfFJBrTI3DXu4EJLIJRXMfV1Pd5fOVO8kDdoTJRREQq8zE4bESliBbNA8z0mAbevhZBAhVeCLsSBl9drx1eSjBtXMK%2BfaZT3HthF05kOUh7pyKOrZB3DPekQF27UrAdozlVdZ799QkSS6yo%2BnX%2FzWU3%2BUPEFsT6TDOnaXFBjqZAdIKwQjS4Quh%2F1RYKaKZZN%2FhtUD9JdwjI0jXD5huJJU%2FQJwCE16NGilTwb7U0ANn5vnc27kJ3ny9dECkB7XQB6vH2mR5OnkBaGIQMH3MnDCG9lB2C2nOnI3hMQYFP8xRm6sc%2BzZ20MrJzImnQEgmZYoTNovRxeQucPRukxF1ORTjIXhSSViFkkvyxizdmtHHHst51a%2Fm83%2F52A%3D%3D&Expires=1755927089)
