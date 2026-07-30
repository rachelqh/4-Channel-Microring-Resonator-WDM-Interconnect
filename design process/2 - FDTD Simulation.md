# FDTD Simulation

## Setting up in FDTD
Following [this tutorial by Ansys](https://optics.ansys.com/hc/en-us/articles/360042800293-Ring-resonator-getting-started-Design-and-initial-simulation) and changing some parameters such as waveguide dimensions and radius, I modeled a ring resonator with a power input source. 
<p align = "center"><img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/1419d91a-0d31-47b0-8b9f-6f3eaebc6f76" /></p>
<p align = "center"><em>Figure 1: Screenshot of the FDTD model of the microring resonator. </em></p>

To find the resonant wavelength that would couple into the ring and into the output bus, I swept wavelengths on the DFT Monitor to visually find to the resonant wavelength.
<p align = "center"><img width="800" height="496" alt="differentwavelengthsinringresonator-ezgif com-video-to-gif-converter" src="https://github.com/user-attachments/assets/7ee1b60f-36f6-4fce-ae04-5c95cdf4af36" /></p>
<p align = "center"><em>Figure 2: A gif exported from FDTD where each frame is a different wavelength. Given red represents optical power, some wavelengths resonated stronger than others.</em></p>

## Making the visualization
Using the resonant wavelength I found earlier, I set the global power source to "frequency" and set the pulse time to be roughly the same as my simulation time. This was to emulate a continuous laser at resonant frequency. I used a movie monitor to export a video, which I compressed into this gif.

<p align="center">
<img width="480" height="360" alt="6secmicroringresonator-ezgif com-optimize" src="https://github.com/user-attachments/assets/e61b717b-dcf0-44a5-9a4f-fcd88e70355c" /></p>

<p align="center">
<em>Figure 1: Final result of FDTD Simulation of microring resonator. The red power at the top is the pulse emulating a continuous laser. </em>  </p>    


## Future Improvements
Due to the significant compute times it took to generate these visualizations, I was unable to significantly iterate on my design. However, key things could be improved in the future:
- More experienced photonic engineers have informed me that my ring is over coupled and has a gap too small to be manufactured. The design could be improved with a proper, manufacturable waveguide gap at critical coupling.
- The ring resonator visualization was designed with a radius of 3um, while the INTERCONNECT circuit ring resonators use a radius of 5um. The visualization could be improved by making the radius match the circuit it's simulation.
  
