## Heat transfer analysis

### Objectives

To perform a basic thermal analysis with variable input parameters that can be changed to investigate the effect or insulation thickness, ice block size, insulation material and ambient temperature on the cool-time and temperature range of the vaccine chamber for example.

We wanted to investigate how much we could reduce the insulation thickness, also have the ability to test insulation, and shell materials with different thermal properties.

### Assumptions made to build code

The cooler was approximated as two simple 2D shapes for the heat transfer analysis. 

The hexagonal face of the cooler was analysed as a circle with a diameter equal to the shortest width of the hexagon. This ensures the analysis will produce an underestimate for the time taken to warm up, so the true model will only outperform the prediction. On the full sized smile, the isulation is 7cm thick in the side with the door and 4cm thick in the far side. An average thickness was taken, however this could be improved in further analysis.
The figure shows the resistor network of thermal resistances in the radial direction.
<img width="652" alt="image" src="https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/assets/99027288/3c45733d-fcb4-45de-909f-c04d2df5ec22">

The following figure shows the resistor network of thermal resistances in the out of the flat face of the box, using a linear analysis.
<img width="784" alt="image" src="https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/assets/99027288/2913d81a-d315-4e45-84b5-dbe128733211">

As heat is gained through both the flat faces, the box was assumed symmetrical and two identical resistor networks were used in parralel to approximate the heat transferred through these faces.
