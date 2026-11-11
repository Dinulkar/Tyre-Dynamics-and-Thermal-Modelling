# Tyre Dynamics Theory

## Tyre force generation

A tyre transmits longitudinal force \(F_x\), lateral force \(F_y\) and vertical load \(F_z\). Its response depends on slip, load, camber, pressure, temperature, speed, road surface and construction.

## Longitudinal slip

A commonly used moving-wheel definition is

\[
\kappa = \frac{R_e\omega-V_x}{\max(|V_x|,\epsilon)}
\]

where \(R_e\) is effective rolling radius, \(\omega\) is wheel angular speed and \(V_x\) is longitudinal speed. Definitions differ, particularly near zero speed. Always document the convention and signs used by the source dataset.

## Slip angle

A simplified expression is

\[
\alpha=\tan^{-1}(V_y/|V_x|)-\delta
\]

where \(V_y\) is lateral velocity and \(\delta\) is steer angle. Models commonly use radians. Sign conventions differ between tools.

## Vertical load and friction

A conceptual friction-circle bound is

\[
\sqrt{F_x^2+F_y^2}\leq\mu F_z
\]

Real tyres exhibit load sensitivity and combined-slip behaviour not captured by this simple bound.

## Educational approximations in this repository

`Python/tyre_forces.py` uses:

\[
F_x=\mu F_z\tanh(\kappa/\kappa_s)
\]

\[
F_y=-\mu F_z\tanh(C_\alpha\alpha/(\mu F_z))
\]

where \(\kappa_s\) is a slip scale and \(C_\alpha\) is an approximate cornering-stiffness parameter. Positive alpha is defined to produce negative lateral force in this implementation. These are illustrative curves, not identified tyre characteristics.

## Data and validation

Record tyre ID, load, pressure, temperature, speed, slip, camber, forces/moments, coordinate system, sensor calibration, sampling and filtering. Fit on calibration data and evaluate on independent data. Inspect residuals across slip, load, temperature and speed rather than relying on a single score.

## Further reading

Hans B. Pacejka, *Tire and Vehicle Dynamics*, 3rd edition, Butterworth-Heinemann, 2012.
