# Interim Report


| Part | Reason | Improvement | constraints | Adresses what need | Importance |
| --- | --- | --- | --- | --- | --- |
| Handle | Transportable, Need to think of an easy and durable way to carry<br><br>No handle on SMILE, just a rucksack. Quite expensive, and a whole extra thing to carry | Could look at different designs.<br><br>Satchel style could be comfortable and modular (guitar strap? £2 per)<br><br>Backpack has more pieces but would be more comfortable.  <br>Lunchbox strap is easy and cheap but might get difficult after a while | Comfortable for 1-2 hr of walking - if we will wear a backpack then do we need a handle/is it critical? | Easy to fix, easy to carry, does not add to the cost, and lightweight (as opposed to a large expensive insulative bag) | Medium-high |
| No. Vaccines | Needs to be maximised since the other constraints are already being met for time. Can always underfill, so need to think of a cheap way to store more.at least a certain number, or too many will need to be brought and will no longer be transportable | Could be as simple as making the carousel smaller to fit the 1L box.  <br>Could look at improving attachment mechanisms to add more vaccines? Or make it more versatile.  <br>Maybe a sock/strap type thing like in a toolbox to make it really thin and versatile | Maximise<br><br>Each vaccine could take 20-30mins. Over one full day (12 hours?) would need at least 24 | Probably fewer vaccines than SMILE, but will make it more portable and easier to transport while still having the maximum utility<br><br>Current SMILE has a very large ice pack, and not all slots are always filled (currently 3 vaccines per section \*18 sections).  <br>Smaller journeys will need less vaccines as they would probably be limited by the number of patients in one day | High |
| --- | --- | --- | --- | --- | --- |
| Time cold | Sufficient to fully vaccinate targets. Bottle to be made 1L<br><br>Need to account for loss of insulation due to removal of outer bag of larger SMILE | 1L ice pottle used, so time would be roughly 3 days already. So can make volume 3x smaller to make it 1 day?<br><br>Could also change insulation to be lighter/better | At least 1 working day | Keeps vaccines below 8 degrees so they don’t spoil, while still reducing the overall dimensions. Less than SMILE, but will make it more portable and easier to transport, also will reduce cost of ice pack, and weight. | High priority, but will be changed by real world testing, so only rough estimates at this stage |
| --- | --- | --- | --- | --- | --- |
| Door | Allows access to vaccines whilst still keeping them cool when not in use. Needs to be wide enough to comfortably load and unload. | SMILE had a very good door - aim to achieve same functionality but with a simpler design/fewer parts. Might not even need changing. | IP55 dust and waterproof.<br><br>Needs to be large enough for easy vaccine removal | Allows access to vaccines whilst still keeping them cool when not in use | Low, current design already well thought of |
| --- | --- | --- | --- | --- | --- |
| Weight | Needs to be transportable so cool box can reach difficult-to-reach locations, though less rough terrain so can give up SOME rigidity | Reduce dimensions since weight only goes down by the cube.<br><br>Thin insulation, although insulation is mostly air so limited effectiveness | Under 10kg | Transportable, probably less durable, but enough to withstand standard use | High |
| --- | --- | --- | --- | --- | --- |
| Ice pack attachment mechanism | Ice pack is changing dimensions. So this will need to be rethought<br><br>Needs to stay central to ensure even cooling of vaccines when melting and shrinking | Currently held in place quite loosely, with a rubber part on the cap. Could look at removing that cap and replacing it with foam. Foam would also mean that if the specific bottle goes out of sale, a slightly different one could be used.<br><br>Change bearing design to a design that can be used with off the shelf bottle e.g. a flexible ring constraint around bottle base | Simple so that it is easy to use and repair - use minimal parts and materials | Easy to use, while preventing rattling which the current box does not do. Current part needs a whole rubberised piece so can reduce cost this way too. Ensures no even distance of ice pack from all vaccines | Low |
| --- | --- | --- | --- | --- | --- |
| Shell | Needs to provide a protective, damage resistant layer. Loss of padding of outer bag means it may been to be more durable/waterproof and incorporate carrying mechanism | May not need much improvement, but new materials and manufacturing methods could be considered to reduce cost of product. May need to be changed to be more comfortable to carry against body without the outer padding | Minimum number of parts for repair.<br><br>IP55 dust and waterproof. | Protective outer shell providing waterproofing and rigidity | Low, current design already well thought out |
| --- | --- | --- | --- | --- | --- |
| Vaccine recording method | Vaccine organisation charts will increase efficiency of vaccine use and delivery. | This needs to be integrated into the hard shell somehow, if the outer bag is not being used. Easily changed vaccine labelling system or a slot for this should be included | Cannot affect waterproofing, should not change mass of product or make it more bulky. Ease of use and accessible | Allows health worker to keep track of vaccines being delivered and their location in the cooler. Reduces need to expose all vaccines to heat whilst searching manually | High |
| --- | --- | --- | --- | --- | --- |


Market research:

Current options… £500 gets you an electric vaccine cooler, so need to lower the price towards the £200 range. Looking at insulation is boring but useful to try and reduce cost. Can also just let kitty do this and look for alternatives now.

Current market options:

Ice packs 500ml-700ml per

Surprisingly limited commercial options seemingly

Versapak:
Up to 30 hours (assuming unopened at room temperature, not 40 degrees outside)

35L = 200 (bundle with 5x700 ice packs = 260)

18L = 155

6L = 136

Quite expensive, need to look at how many vaccines can fit

Small - 305 x 305 x 170mm

Internal Capacity: 6 Litres

Weight (Empty): 1.658kg

Medium - 460 x 305 x 255mm

Internal Capacity: 18 Litres

Weight (Empty): 2.151kg

Large - 650 x 380 x 255mm

Internal Capacity: 35 Litres

Weight (Empty): 3.657kg

Too large to comfortably carry in any way other than handle, probably not great for long walks. Current smile improves on: weight, size, no.vaccines, cold time with only 1 ice pack.

VaccinePorter:

8 hour plus time

2.2L capacity

£160

CorrMed:

£261.75Sale Price (350 otherwise)

20L capacity

7 hour cold time

Comes with 4 seemingly 1L ice packs

All options seem to be just boxes with handles and seem to be very expensive. Col box can be easily cheaper if CNC is removed from process, so need to focus on it being better


# Dan

## Scaling Thermal Analysis

Time that the Smirk can maintain vaccine between 2 and 8 degrees:
### $\frac{t_1}{t_2} = \frac{x_1^2A_2V_1\lambda_2}{x_2^2A_1V_2\lambda_1}$
where $A$ is the surface area of the bottle, $V$ is the volume of the bottle, $x$ is the wall thickness and $\lambda$ is the heat conductivity of the insulation material. We know that $t_1$ is approximately 120 hours, $x_1$ is approximately 5cm and $V_1$ is 2.5L for the original Smile.
We want $t_2 > 24$ hours for Smirk, and we know that $V_2 = 1$L, $\frac{\lambda_2}{\lambda_1} = 1$ and $\frac{A_2}{A_1} = 0.54$, therefore we need:
### $x_2 > 2.6$ cm


## Mass Scaling Analysis

Mass of the Smirk:
### $m = \rho_wV_1+\rho_mA_1x_1$, therefore:
### $\frac{m_1}{m_2} = \frac{\rho_wV_1+\rho_mA_1x_1}{\rho_wV_2+\rho_mA_2x_2}$
where $A$ is the surface area of the bottle, $V$ is the volume of the bottle, $x$ is the wall thickness, $\rho_w$ is the density of water and $\rho_m$ is the approximate calculated density of the insulaton and shell combined.
$V_1 = 0.0025 m^3$, $V_2 = 0.001 m^3$, $\rho_w = 1000 kgm^{-3}$, $x_1 = 0.055 m$ and $m_1 = INSERT NUMBERkg$. Therefore,
### $\rho_m = \frac{m_1 - \rho_wV_1}{A_1x_1} = INSERT NUMBER

Hence:

### $m_2 = INSERT EQUATION = INSERT NUMBER$

## Strap Design

I have started prototyping different modular strap designs to test for both the Smile and the Smirk. I started by creating a mock-up of the Smile out of cardboard, shown below:

https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/blob/main/interim/photographs/IMG_20240525_181334368.jpg

https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/blob/main/interim/photographs/IMG_20240525_181316953.jpg

I then designed and prototyped modular attaching clips which can be glued to botht the Smile and the Smirk. These allow interchangeable straps to be attached to the Smile/Smirk, and thus allow user customisability to attach whatever strap configuration is most comfortable for them. The straps can also be removed, allowing the box to be used un-altered as before. Photographs of the attachment points are below:

https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/blob/main/interim/photographs/IMG_20240525_181409278.jpg

https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/blob/main/interim/photographs/IMG_20240525_181402553.jpg

Straps were then prototyped out of cardboard with a width of 40mm. I plan on trying these out, along with 70mm-wide straps on a field test where I walk around with the Smile protoype weighted to the correct mass. This will allow me to identify which set of straps is more ergonomic, and the modularity of the strap-retaining mechanism glued to the box means that both I, and any end user, can easily swap of straps for the most comfortable for them. Perhaps it will be suggested that the default Smile straps are thicker than the default Smirk ones due to the higher anticipated weight of the Smile. However the straps will of course be interchangeable. Here are some photographs of the straps:

https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/blob/main/interim/photographs/IMG_20240525_181429904.jpg

And how they attach to the box:

https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/blob/main/interim/photographs/IMG_20240525_181504778.jpg

https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/blob/main/interim/photographs/IMG_20240525_181500103.jpg

I have completed some preliminary field tests with the straps, and these are photographed below:

https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/blob/main/interim/photographs/IMG_3840.jpeg

https://github.com/Technology-for-the-Poorest-Billion/2024-ideabatic-smirk/blob/main/interim/photographs/IMG_3839.jpeg

I have also explored the possibility of front-mounting the Smirk. Advantages of this include enhanced protection for the vaccines (unlikely to bump the Smirk into things), and possible on-the-fly acces to the Smirk's contents.

At the moment the straps have to be held to keep the Smirk in place, but I am exploring options for lengthening the straps and attaching both ends to the Smirk so that it can be carried hands-free.
