# bike-throw

This is a problem I saw from [SCUDEM 2020](https://qubeshub.org/community/groups/scudem/wiki/SCUDEMV2020) that interests me as a cyclist.

## Background
In the 2021 Brabanste Pijl Dames bicycle race, Demi Vollering throught she won the race and celebrated early. However, Ruth Winder just before reaching the finish line decided to stop cycling and threw her bike. Winder ended winning the race by a very small margin.

## Assumptions
We employ the following assumptions that simplify our problem:
* Bike Throw is instantaneous.
* Flat asphalt surface
* Weather is dry.
* Velocity is constant before the bike throw.
* Bike has 100% efficiency, i.e., bike parts have negligible resistance among them.

## Model

We use Newton's second law of motion as the inspiration for the model
```math
M\ddot{x} = F_B(t)-F_D-F_r+F_P(t) = F_B(t)-\frac{1}{2}\rho\left(\frac{dx}{dt}\right)^2C_DA - \sigma*g*M + F_P(t)
```
where $F_B$ is the bike throw force, $F_P$ is the pedaling force, $F_D$ is the drag force, $\rho$ is the density of the fluid (e.g., air), $C_D$ is the drag coefficient, $A$ is cross-sectional of the moving body, $F_r$ is the rolling resistance force, $\sigma$ is the rolling resistance coefficient, and $g$ is the acceleration due to gravity. Moreover, we define $F_B$ to be nonzero at the point when the bike throw happens and 0 otherwise, and we define $F_P$ to be nonzero before the bike throw and 0 on and after the bike throw.
