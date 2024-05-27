## Heat transfer analysis

### Objectives

To perform a basic thermal analysis with variable input parameters that can be changed to investigate the effect or insulation thickness, ice block size, insulation material and ambient temperature on the cool-time and temperature range of the vaccine chamber for example.

We wanted to investigate how much we could reduce the insulation thickness, also have the ability to test insulation, and shell materials with different thermal properties.

### Assumptions made to build code

The cooler was approximated as two simple 2D shapes for the heat transfer analysis. 

The hexagonal face of the cooler was analysed as a circle with a diameter equal to the shortest width of the hexagon. This ensures the analysis will produce an underestimate for the time taken to warm up, so the true model will only outperform the prediction. On the full sized smile, the isulation is 7cm thick in the side with the door and 4cm thick in the far side. An average thickness was taken, however this could be improved in further analysis.
The figure shows the resistor network of thermal resistances in the radial direction.
![](Photos/Radial_resistor_network.jpg)

The following figure shows the resistor network of thermal resistances in the out of the flat face of the box, using a linear analysis.
![](Photos/Linear_resistor_network.jpg)


As heat is gained through both the flat faces, the box was assumed symmetrical and two identical resistor networks were used in parralel to approximate the heat transferred through these faces.

The chamber cntaining the vaccines was assumed to have the thermal properties of air (the vaccines were ignored). The thermal properties of the carosel were assumed to be the same as those of the ABS shell.


# Analysis of large box

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

# Analysis of small box

#### Inputs
T_atm = 27 degrees C <br>
Ice bottle radius = 5cm <br>
Ice bottle height = 13cm <br>
Vaccine chamber radial dimension = 3cm <br>
Insulation thickness in radial direction = 4cm <br>
Insulation thickness along flat faces = 3cm <br>
Air gap above and below ice pack = 1cm <br>

![](Photos/Small_3cm_linear.png)
<br>The rate of heat transferred from the two flat faces is, Q_tot_l = 0.713 J/s

![](Photos/Small_4cm_radial.png)
<br>The rate of heat transferred from the radial face is, Q_dot_r = 1.129 J/s

This shows the face limiting the cool life is the radial face as before.
By approximating the box as the radial and linear resistor systems in parallel the total heat transferred out of the cooler is,
Q_dot: 1.841 J/s

This gives a cool life, with the vaccines below 8 degrees C, of **58.5 hours**.

## Effect of spacing between bottle and carousel - significant due to shrinkage when it melts
<img width="168" alt="image" src="https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/assets/99027288/020f3c96-e6fc-4635-a14c-e23bae6c5747">

Considering worst case scenario for the heating of the vaccines: we assume full contraction in a radial direction and no contraction in the londitudinal direction.
On freezing the bottle with expand from 1 litre to 1.087 litres which results in a 4% radius increase. This space has been accounted for by a 1cm gap around the unexpanded bottle as it is likely the expansion will not be the same across the height of the bottle, so allows for more expansion at midsection.

The thermal properties of the materials in this gap are found to have a large impact on the temperature of the vaccine chamber.

When the gap is filled with air:
<br>![image](https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/assets/99027288/d6818680-24f0-4a64-86c2-97563e2b60c3)
<br>Q_dot_r: 1.041805845369173 J/s

This gives a cool life, with the vaccines below 8 degrees C, of **61.3 hours**.

## Using predictions from Dan's scaling analysis

When the insulation of the small smile is set as 2.6cm the results are as follows:
<br>![image](https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/assets/99027288/ac4d3e3c-c135-4d36-8572-ac31770020b1)
<br>Q_tot_l: 0.7890635803234574 J/s

![image](https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/assets/99027288/99f6eea9-1bdb-4b2f-a4cb-68d000a168ae)
<br>Q_dot_r: 1.2706851966492552 J/s

This gives a cool life, with the vaccines below 8 degrees C, of **52.3 hours**.
MAin issuee with this design is keeping the vaccines within the safe operating range - could be affected by running analysis assuming convection in chamber however.



# Next steps

Produce analysis with convective heat transfer in vaccine chamber to produce an upper bound for heat transfer.

Investigate materials to support bottle in cavity - high thermal conductivity but also compressibility

Prototype bottle support mechanism with this in mind

Perform experiments to measure expansion of bottle when frozen, once the ordered bottle arrives.



