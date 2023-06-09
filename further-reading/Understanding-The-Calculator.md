## Understanding the Calculation Algorithm

### Constants

$V_0$ Sun's velocity around the Galactic center, i.e., 220 km/s

$R_0$ Distance from the Sun to Galactic center, i.e., 8.5 kpc

$l$ Galactic longitude of observation

$V$ Velocity of a cloud of gas

$R$ Cloud's distance to the Galactic center

### Equations for Calculating Distance between gas cloud and galactic center

The following equation is always applied to calculate the distance no matter what the value of $l$ is:

$R = \frac{{R_0 V_0 \sin(l)}}{{V_0 \sin(l) + V_r}}$

And If $0&deg < l < 90&deg$ or $270&deg < l < 360&deg$ then the following calculation has to be done to get the correct distance:

$r = {\sqrt{R^2 - R_0^2 \sin^2 l }+ R_0 \cos l}$

Distance calculation implemented in code:
![distance](https://github.com/mrikea4real/salsa-sky-mapper/assets/79717170/1ea517a8-14a3-4ed5-989d-56ad93d04463)

### Equations for converting distance to Cartesian coordinates

${x} = {r cos(l - 90°)}$

${y} = {r sin(l - 90°) + R_0}$

Conversion calculation implemented in code:

![conversion](https://github.com/mrikea4real/salsa-sky-mapper/assets/79717170/63c48d4f-fd3d-4419-a782-747a418870fc)
