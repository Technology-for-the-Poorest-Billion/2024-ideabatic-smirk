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

The chamber cntaining the vaccines was assumed to have the thermal properties of air (the vaccines were ignored). The thermal properties of the carosel were assumed to be the same as those of the ABS shell.

https://colab.research.google.com/gist/oca21/c965887e9c410e554f906086208de843/mini_smile.ipynb

### Analysis of large box

#### Inputs
T_atm = 27 degrees C <br>
Ice bottle radius = 7cm <br>
Ice bottle height = 16cm <br>
Vaccine chamber radial dimension = 4cm <br>
Insulation thickness in radial direction = 6cm <br>
Insulation thickness along flat faces = 5cm <br>
Air gap above and below ice pack = 1cm <br>

#### Results
![image](https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/assets/99027288/65d47a94-4ca5-4fed-a1b2-4611a804b697)
<br>The rate of heat transferred from the two flat faces is, Q_dot_l = 0.930 J/s.

![image](https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/assets/99027288/1aaf6683-04cd-4798-bac7-194b526001e2)
<br>The rate of heat transferred from the radial face is, Q_dot_r = 1.469 J/s.

This shows the face limiting the cool life is the radial face.
By approximating the box as the radial and linear resistor systems in parallel the total heat transferred out of the cooler is,
Q_dot = 2.376 J/s.

This gives a cool life, with the vaccines below 8 degrees C, of **109.3 Hours**.
The large smile should last approx. 120 hours, so this shows that the software does give an underestimate as expected, but also a relatively close estimate of the cool life, suggesting it could be a useful tool for analysis of a smaller box design.

### Analysis of small box

#### Inputs
T_atm = 27 degrees C <br>
Ice bottle radius = 5cm <br>
Ice bottle height = 13cm <br>
Vaccine chamber radial dimension = 3cm <br>
Insulation thickness in radial direction = 4cm <br>
Insulation thickness along flat faces = 3cm <br>
Air gap above and below ice pack = 1cm <br>

![image](https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/assets/99027288/569b1ef1-ce7e-4865-b09f-4b56d15ed520)
Q_tot_l: 0.712877294969478 J/s

![image](https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/assets/99027288/7f307e86-c14b-4363-9d65-4676029b83eb)
Q_dot_r: 1.1285677410290333 J/s

Q_dot: 1.8414450359985115 J/s

58.46221879265923
