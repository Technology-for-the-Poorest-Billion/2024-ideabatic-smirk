# Heat transfer analysis

## Objectives

To perform a basic thermal analysis with variable input parameters that can be changed to investigate the effect of insulation thickness, ice block size, insulation material and ambient temperature on the cool-time and temperature range of the vaccine chamber for example.

The aim was to have a tool that could help investigate how much the insulation thickness could be reduced, and also enable the testing of insulation and shell materials with different thermal properties.

## Assumptions made to build code

The cooler was approximated as two simple 2D shapes for the heat transfer analysis. 

The hexagonal face of the cooler was analysed as a circle with a diameter equal to the shortest width of the hexagon. This ensures the analysis will produce an underestimate for the time taken to warm up, so the true model will only outperform the prediction provided by this analysis. On the full sized smile, the isulation is 7cm thick in the side with the door and 4cm thick in the far side. An average thickness was taken for the analysis, however this could be improved in further analysis.

The figure shows the network of thermal resistances used around the hexagonal face, to calculate the heat transfer out of the 6 rectangular faces of the smile cooler. 
<br><img src="Photos/Annotated_hexagonal.png" alt="Annotated hexagonal face of cooler" width="400"/>
<img src="Photos/Radial_resistor_network.jpg" alt="2D approximate model" width="500"/>


The following figure shows the resistor network of thermal resistances out of the flat hexagonal faces of the box, using a linear analysis.
<br><img src="Photos/Rectangular_face_annotated.png" alt="Annotated rectangular face of cooler" width="400"/>
<img src="Photos/Linear_resistor_network.jpg" alt="2D approximate model" width="500"/>

As heat is gained through both the flat hexagonal faces, the box was assumed symmetrical and two identical resistor networks were used in parralel to approximate the heat transferred through these faces.

To calculate the total heat transferred from all faces of the box the radial and two linear resistance networks were all used as resistances in parallel, with the total temperatre difference across the box(from T_atm to T_ice). The total heat ransfer required to melt and warm the ice to a temperature causing the vaccine chamber to exceed the limiting temperature of 8 degrees C for storage. This quantifies the amount of heat tranfer required to reach the end of life of one use of the cool box (i.e. use of 1 ice block before requiring refreezing). Dividing this value by the total rate of heat transfer from all faces gives an esimate for the cool-time of the cool box. 

Further assumptions made include:
* The chamber cntaining the vaccines was assumed to have the thermal properties of air (the prescence of any vaccines was ignored).
  * Convective and conductive heat transfer were ananlyssed in paralell for the heat transfer in the still air of the vaccine chamber.
  * Assuming just conductive heat transfer gives a lower bound for the amout of heat transferred and an upper bound for the temperature in the vaccine chamber, whilst assuming convective heat transfer also, gives an upper bound for the annount of heat transferred from the cool box, and a lower bound for the temperature in the vaccine chamber and cool life.
* The thermal properties of the carosel were assumed to be the same as those of the ABS shell.
* The heat lost out of the hexagonal faces was assumed to happen over the area of the end of the iceblock and vaccine chamber


# Analysis of large box

## Inputs
T_atm = 27 degrees C <br>
T_ice_avg = -10 degrees C <br>
Ice bottle radius = 8cm <br>
Ice bottle height = 14cm <br>
Vaccine chamber radial dimension = 3.5cm <br>
Insulation thickness in radial direction = 4cm <br>
Insulation thickness along flat faces = 4.5cm <br>
Air gap above and below ice pack = 1cm <br>
Air gap around ice pack = 0.5cm <br>
lambda_shell = 0.18 W/mK for ABS shell <br>
lambda_ins = 0.023  W/mK


## Results
### Lower bound for rate of heat transfer - assuming just conduction in air gap

The temperature profile from the top or bottom of the ice pack, out through one of the two hexagonal faces is shown below:
<br><img src="Photos/Big_lin_LB.png" alt="Temperature profile through thickness of smile" width="600"/>
<br>The rate of heat transferred from the two flat faces is, **Q_dot_l = 1.036 J/s**.
The height of the big smile is 26cm.

The temperature profile from the ice block to the rectangular walls, in a radial direction is shown below. Two limits for the vaccine storage temperature have been shown in the figure as dashed red lines. This region is significant in the vaccine storage chamber as the average temperature of the chamber(taken as average, instead of linear temperature gradient as shown, because of mixing effects of air) must lie within these limits for the vaccines to be preserved.
<br><img src="Photos/Big_rad_LB.png" alt="Temperature profile through radial walls" width="600"/>
<br>The rate of heat transferred from the radial face is, **Q_dot_r = 1.542 J/s**.
The diameter of the big smile is approx. 33cm.

The greater rate of heat loss from the radial faces shows that the heat loss out of the radial faces is the limiting factor for the cool life. 
By approximating the box as the radial and linear resistor systems in parallel the total heat transferred out of the cooler is,
**Q_dot = 2.579 J/s**.

This gives a cool life, with the vaccines below 8 degrees C, of **115.1 Hours**.
The large smile should last approx. 120 hours, so this shows that the software does give an underestimate as expected, but also a relatively close estimate of the cool life, suggesting it could be a useful tool for analysis of a smaller box design.

### Upper bound for rate of heat transfer - assuming conduction and convection in air gap

The temperature profile from the top or bottom of the ice pack, out through one of the two hexagonal faces is shown below:
<br><img src="Photos/Big_lin_LB.png" alt="Temperature profile through thickness of smile" width="600"/>
<br>The rate of heat transferred from the two flat faces is, **Q_dot_l = 1.036 J/s**. This is unchanged by the inclusion if convective effects in the air gap.

The temperature profile from the ice block to the rectangular walls, in a radial direction is shown below, with convection effects now considered in the air gap as well as conduction. Two limits for the vaccine storage temperature have been shown in the figure as dashed red lines. This region is significant in the vaccine storage chamber as the average temperature of the chamber(taken as average, instead of linear temperature gradient as shown, because of mixing effects of air) must lie within these limits for the vaccines to be preserved.
<br><img src="Photos/Big_rad_UB.png" alt="Temperature profile through radial walls" width="600"/>
<br>The rate of heat transferred from the radial face is, **Q_dot_r = 2.772 J/s**.

The greater rate of heat loss from the radial faces shows that the heat loss out of the radial faces is still the limiting factor for the cool life. 
By approximating the box as the radial and linear resistor systems in parallel the total heat transferred out of the cooler is,
**Q_dot = 3.808 J/s**.

This gives a cool life, with the vaccines below 8 degrees C, of **77.9 Hours**.
This is a much lower estimate for the expected cool life of the smile coolbox, but gives a range in which the true value would be expected to lie. This value lies much further from the length of time Kitty said the the large box could stay cool for, (120 hours) suggesting both bounds are underestimates. This error could have been accounted for by the inclusion of the back pack bag that was used in practice with the larger smile however, as this would have added an extra thermal insulation layer, extending the cool life.


# Analysis of small box - 4cm insulation

The small smile box is a new design centred on the use of a smaller, off-the-shelf ice pack, which is a 1l bottle. Analysis has been based on this new icepack volume and shape.

## Inputs
T_atm = 27 degrees C <br>
T_ice_avg = -10 degrees C <br>
Ice bottle radius = 5cm <br>
Ice bottle height = 15cm <br>
Vaccine chamber radial dimension = 3cm <br>
Insulation thickness in radial direction = 4cm <br>
Insulation thickness along flat faces = 3cm <br>
Air gap above and below ice pack = 0.5cm <br>
Air gap around ice pack = 0.5cm <br>
lambda_shell = 0.18 W/mK for ABS shell <br>
lambda_ins = 0.023  W/mK

## Results
### Lower bound for rate of heat transfer - assuming just conduction in air gap

The temperature profile from the top or bottom of the ice pack, out through one of the two hexagonal faces is shown below:
<br><img src="Photos/small_4_lin.png" alt="Temperature profile through thickness of mini smile" width="600"/>
<br>The rate of heat transferred from the two flat faces is, **Q_dot_l = 0.637 J/s**.
The height of the mini smile with insulation thickness of 4cm is 25cm, so not much smaller that the origional smile in this dimension.

The temperature profile from the ice block to the rectangular walls, in a radial direction is shown below, with only conduction effects considered in the air gap.
<br><img src="Photos/small_4_rad_LB.png" alt="Temperature profile through radial walls" width="600"/>
<br>The rate of heat transferred from the radial face is, **Q_dot_r = 1.130 J/s**.
The diameter of the small smile with 4cm insulation is approx. 26cm which is a reduction of 7cm from the large smile.

This shows the face limiting the cool life is the radial face as in the large model.
By approximating the box as the radial and linear resistor systems in parallel the total heat transferred out of the cooler is,
**Q_dot: 1.767 J/s**.

This gives a cool life, with the vaccines below 8 degrees C, of **70.3 hours**.

### Upper bound for rate of heat transfer - assuming conduction and convection in air gap

The temperature profile out of the two hexagonal faces is unchanged between the upper and lower bound analyses, so only the radial heat transfer analysis and resulting total heat transfer rate and cool time are included for upper bound from this point onwards.

The temperature profile from the ice block to the rectangular walls, in a radial direction is shown below, with convection effects now considered in the air gap as well as conduction.
<br><img src="Photos/small_4_rad_UB.png" alt="Temperature profile through radial walls" width="600"/>
<br>The rate of heat transferred from the radial face is, **Q_dot_r = 1.938 J/s**.

This shows the face limiting the cool life is the radial face as in the large model.
By approximating the box as the radial and linear resistor systems in parallel the total heat transferred out of the cooler is,
**Q_dot: 2.574 J/s**

This gives a cool life, with the vaccines below 8 degrees C, of **48.3 hours**.
This implies the true cool life of a small smile will lie between 48.3 hours < t < 70.3 hours. The use case for the smaller smile requires it to last up to 24 hours for shorter last mile journeys. This criterion is met by the design with the off the shelf smaller ice pack and 4cm thick insulation above, below and radially surrounding the ice pack and vaccine chamber.

In all analyses so far, the radial heat transfer has been the limiting factor. This implies the insulation thickness above and below could be reduced relative to the thickness of the insulation around the vaccine chamber's circumference.


# Analysis of small box - Using predictions from Dan's scaling analysis

Following the thermal scaling analysis conducted by Dan, suggestion for insulation thickness was 2.6cm. This is tested in the following analysis with the higher fidelity coded model.

## Inputs - 2.6cm insulation
T_atm = 27 degrees C <br>
T_ice_avg = -10 degrees C <br>
Ice bottle radius = 5cm <br>
Ice bottle height = 15cm <br>
Vaccine chamber radial dimension = 3cm <br>
Insulation thickness in radial direction = 2.6cm <br>
Insulation thickness along flat faces = 2.6cm <br>
Air gap above and below ice pack = 0.5cm <br>
Air gap around ice pack = 0.5cm <br>
lambda_shell = 0.18 W/mK for ABS shell <br>
lambda_ins = 0.023  W/mK

## Results
### Lower bound for rate of heat transfer - assuming just conduction in air gap

The temperature profile from the top or bottom of the ice pack, out through one of the two hexagonal faces is shown below:
<br><img src="Photos/small_2.6_lin.png" alt="Temperature profile through thickness of mini smile" width="600"/>
<br>The rate of heat transferred from the two flat faces is, **Q_dot_l = 0.912 J/s**.
The height of the mini smile with insulation thickness of 4cm is 22cm, so has a lightly greater improvement on the large smile in this dimension.

The temperature profile from the ice block to the rectangular walls, in a radial direction is shown below, with only conduction effects considered in the air gap.
<br><img src="Photos/small_2.6_rad_LB.png" alt="Temperature profile through radial walls" width="600"/>
<br>The rate of heat transferred from the radial face is, **Q_dot_r = 1.156 J/s**.
The diameter of the small smile with 4cm insulation is approx. 26cm which is a reduction of 7cm from the large smile.

This shows the face limiting the cool life is the radial face as in the large model.
By approximating the box as the radial and linear resistor systems in parallel the total heat transferred out of the cooler is,
**Q_dot: 2.068 J/s**.

This gives a cool life, with the vaccines below 8 degrees C, of **60.1 hours**.

### Upper bound for rate of heat transfer - assuming conduction and convection in air gap

The temperature profile out of the two hexagonal faces is unchanged between the upper and lower bound analyses, so only the radial heat transfer analysis and resulting total heat transfer rate and cool time are included for upper bound from this point onwards.

The temperature profile from the ice block to the rectangular walls, in a radial direction is shown below, with convection effects now considered in the air gap as well as conduction.
<br><img src="Photos/small_2.6_rad_UB.png" alt="Temperature profile through radial walls" width="600"/>
<br>The rate of heat transferred from the radial face is, **Q_dot_r = 2.220 J/s**.

This shows the face limiting the cool life is the radial face as in the large model.
By approximating the box as the radial and linear resistor systems in parallel the total heat transferred out of the cooler is,
**Q_dot: 3.132 J/s**

This gives a cool life, with the vaccines below 8 degrees C, of **39.7 hours**.
This implies the true cool life of a small smile will lie between 48.3 hours < t < 70.3 hours. The use case for the smaller smile requires it to last up to 24 hours for shorter last mile journeys. This criterion is met by the design with the off the shelf smaller ice pack and 4cm thick insulation above, below and radially surrounding the ice pack and vaccine chamber.

In all analyses so far, the radial heat transfer has been the limiting factor. This implies the insulation thickness above and below could be reduced relative to the thickness of the insulation around the vaccine chamber's circumference.




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
Main issuee with this design is keeping the vaccines within the safe operating range - could be affected by running analysis assuming convection in chamber however.



# Next steps

Produce analysis with convective heat transfer in vaccine chamber to produce an upper bound for heat transfer.

Investigate materials to support bottle in cavity - high thermal conductivity but also compressibility

Prototype bottle support mechanism with this in mind

Perform experiments to measure expansion of bottle when frozen, once the ordered bottle arrives.



