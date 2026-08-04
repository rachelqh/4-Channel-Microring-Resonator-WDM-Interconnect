# Custom Photonic Integrated Circuit
3 resonant laser frequencies are coupled into the custom PIC, each correlating to a different communication channel. Based on the analog voltage at the DUT converted into a digital signal, each channel's mach-zehner modulator encodes the digital data onto the intensity of light. Then, all 3 channels, with their respective frequencies and encoded data, are combined via combiner and transmitted over a shared wavelength division multiplexed waveguide. To recover the signal, 3 cascaded ring resonators tuned to their resonant frequencies demultiplex the signal. Finally, a photodetector connected to a microcontroller uses firmware to communicate the original analog voltage to the user.

<p align = "center"><img width="898" height="600" alt="image" src="https://github.com/user-attachments/assets/298cd008-ba54-4b4f-80e7-ddaa28b26c29" /></p>

<p align = "center"><em>Figure 1: Schematic of custom PIC.</em></p>


<p align = "center"><img width="1686" height="396" alt="image" src="https://github.com/user-attachments/assets/a5324b2c-8a82-4dd3-b6bb-f668ab8d9c10" /></p>
<p align = "center"><em>Figure 2: Diagram of centre ring's free spectral range.</em></p>

# Key Design Parameters
- Number of channels: 3
- Waveguide dimensions: 440 nm × 220 nm
- Channel wavelengths: 1580.42 nm, 1575.87 nm, 1571.55 nm
- Ring radii (center ring): 5 μm
- FSR: 34.96 nm

# Ring & Channel Frequency Tuning
<p align = "center"><img width="577" height="374" alt="image" src="https://github.com/user-attachments/assets/cadb0509-c20b-49f3-a370-6af181da71ce" /></p>
<p align = "center"><em>Figure 3: Center ring's transmissions as a function of wavelength graph</em></p>

First, after choosing the ring radius of 5 microns, I used Lumerical INTERCONNECT's Optical Network Analyzer Tool to find the resonant frequency.

<img width="1455" height="648" alt="image" src="https://github.com/user-attachments/assets/bedc03b8-0e4d-4f0d-96b7-b54633d7541e" />
<p align = "center"><em>Figure 4: Screenshot of parameter sweep settings + 3 ring radius sweeps that increase in closeness.</em></p>

<img width="800" height="560" alt="lookingforradiuswithwavelength-ezgif com-video-to-gif-converter" src="https://github.com/user-attachments/assets/c7271efb-c5a6-47c1-82ce-98f002af3266" />

<p align = "center"><em>Figure 5: Animation of transmission spectrum where each frame is a different ring radius, used to find ring radius based on calculated frequency.</em></p>

Based on the centre ring's transmission spectrum, I chose the frequency where transmission = 0 for the second channel, which turned out to be 1571.55 nm. To find the radius which would resonate with that frequency, a used a parameter sweep. By sweeping the radius for a graph of transmission as a function of wavelength, I could match the frequency I wanted to a specific wavelength. This was done by sweeping the radius in large increments; finding the two radiuses the frequency must be between, then sweeping in that smaller interval. After repeating this process 3 times, the closest resonant frequency I could find was chosen. Then, with the ring set to that

# Signal Integrity Debugging

Even after tuning the rings and setting the ONA's perfect frequency for each ring, the cross talk between channels was incredibly high, as shown in figure 6.

With the advice of a senior photonic engineer, I was advised to increase the coupling coefficient which would 
