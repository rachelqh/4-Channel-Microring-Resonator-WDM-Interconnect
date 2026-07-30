# INTERCONNECT Circuit
The overall system is intended to be a ultra-fast light speed version of my Continuity-Test-Redesign. This document explains the existing architecture design as well as the original design.

# Overall System design
Current will be injected into 3 DUT's, where the differential voltages at both DUT pins can be used to calculate voltage. 6 ADCs are placed at the 6 DUT pins to convert an analog signal to a binary signal to be transmitted photonically. The information will be transmitted in the photonic IC detailed in [**INTERCONNECT Circuit**](./design%20process/3%20-%20INTERCONNECT%20Circuit.md), then recovered via photodiode and understood by the STM32 MCU.

<p align = "center"><img width="1008" height="579" alt="image" src="https://github.com/user-attachments/assets/c37aec10-524c-40da-8d93-dcf84db78dd5" /></p>
<p align = "center"><em> Figure 1: Overall system schematic of the photonic reimagining of my Continuity Test. </em></p>

# Project Evolution
The original design of the system encoded information onto the frequency of a laser blinking, rather than intensity. The system would simultaneously convert 2 x 13 analog voltages into a representative optical laser blinking at a different frequency. The lasers would still wavelength-division multiplexed, allowing the the MCU would use the frequency detected at the photodetector to determine the voltages of the light.

<p align = "center"><img width="800" height="1067" alt="IMG_7284" src="https://github.com/user-attachments/assets/1f3cde38-9dbf-4519-a9cc-be482db651ec" /></p>
<p align = "center"><em> Figure 1: My original photonic reimagining of my Continuity Test. </em></p>

Ultimately, several challenges resulted in the changes to the project to the current system. Given the advice of a senior photonic engineer, I discovered it's more reliable to modulate data onto intensity, rather than frequency. Therefore, the project was changed to transmit digital data rather than analog data. Due to project scope and simulation complexity, a 3-channel implementation was developed and validated as a proof of concept.
