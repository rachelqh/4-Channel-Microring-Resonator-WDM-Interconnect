# Photonics & Photonic Integrated Circuit Studying

Before beginning the project, I read key chapters of the textbooks *Fundamentals of Photonics* by Bahaa E. Saleh and Malvin C. Teich and *Silicon Photonics Design: From Devices to Systems* by Lukas Chrostowski and Michael Hochberg. Reading these relevant textbook chapters gave me significant and helpful background context for designing my first PIC.  

I studied the following chapters from *Fundamentals of Photonics* to develop an understanding of the physics underlying modern photonic devices and systems:

- Chapter 9: Guided-Wave Optics (Modes and Waveguides)
- Chapter 11: Resonator Optics (Including Ring Resonators)
- Chapter 19: Photodetectors
- Chapter 24: Optical Interconnects and Switches

I studied the following chapters from *Silicon Photonics Design: From Devices to Systems* to learn practical silicon photonics design techniques. The textbook also provided MATLAB examples and ANSYS Lumerical-based design workflows that were useful throughout the project.

- Chapter 3: Optical Materials and Waveguides
- Chapter 4: Fundamental Building Blocks (Including Ring Resonators)
- Chapter 5: Optical I/O
- Chapter 6: Modulators
- Chapter 9: Photonic Circuit Modelling

## Key Concepts Studied

- Optical waveguide and coupling theory
- Effective index and group index
- Optical resonators and resonance conditions
- Free Spectral Range (FSR)
- Photonic circuit modelling
- Silicon photonic device design

# Finding Effective Index and Group index
Initally, I used MATLAB Code from *Silicon Photonics Design: From Devices to Systems* to simulate a 1D waveguide and change parameters and get an understanding of how material and wavelength affects effective index.
<p align = "center"><img width="708" height="506" alt="image" src="https://github.com/user-attachments/assets/7d129fba-f436-4f0c-9b2e-d7af47262ad9" /></p>  

<p align = "center"><em>Figure 1: Screenshot of MATLAB interface used to get preliminary numbers for effective index.</p></em>


Based on [Silicon microring resonators (PDF)](https://www.photonics.intec.ugent.be/download/pub_3105.pdf), I chose a substrate of SIO2, a core of pure silicon, and dimensions of 440nm x 220nm for my waveguide.

After getting a basic understanding of effective index, I used a more robust simulation in Lumerical MODE to get the exact index for my 2D waveguide.  

<p align = "center"><img width="570" height="491" alt="Screenshot 2026-07-15 154924" src="https://github.com/user-attachments/assets/d102f6bc-6382-45cf-a70a-71cf40bb10a9" /></p>
<p align = "center"><em>Figure 2: Screenshot of MODE simulation used to find effective index. The black square is the waveguide, while the red colour is optical power.</p></em>

After viewing a few modes with a TE polarization fraction of 100, I chose a MODE which looked strongly confined in the waveguide but still could be reasonably coupled. This gave me an **effective index of 2.5** and a **group index of 4.44**.



