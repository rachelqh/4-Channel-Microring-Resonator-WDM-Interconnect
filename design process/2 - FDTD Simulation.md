# FDTD Simulation
To create a visualization of the optical power coupling in a microring resonator, I had to move to Lumerical FDTD. Following [this tutorial by Ansys](https://optics.ansys.com/hc/en-us/articles/360042800293-Ring-resonator-getting-started-Design-and-initial-simulation) and changing some parameters such as waveguide dimensions and radius, I modeled my ring resonator. 

# Creating the ring resonator
<p align = "center"><img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/1419d91a-0d31-47b0-8b9f-6f3eaebc6f76" /></p>
<p align = "center"><em>Figure 1: Screenshot of the FDTD model of the microring resonator. </em></p>

## Future Improvements
Due to the significant compute times it took to generate these visualizations, I was unable to significantly iterate on my design. However, key things could be improved in the future:
- More experienced photonic engineers have informed me that my ring is over coupled and has a gap too small to be manufactured. The design could be improved with a proper, manufaturable waveguide gap at critical coupling.
- The ring resonator visualization was designed with a radius of 3um, while the INTERCONNECT circuit ring resonators use a radius of 5um. The visualization could be improved by making the radius match the circuit it's simulation.
  
