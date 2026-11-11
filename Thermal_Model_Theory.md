# Tyre Thermal Modelling: Lumped Approximation

## First-order energy balance

The single-state model is:

\[
C_{th}\frac{dT}{dt}=Q_{in}-H(T-T_{amb})
\]

where T is effective tyre temperature, \(C_{th}\) effective thermal capacity [J/K], \(Q_{in}\) supplied heat input [W], H effective heat-loss coefficient [W/K] and \(T_{amb}\) ambient temperature.

The code uses forward Euler integration and a trapezoidal average of heat input between time samples. Time must increase strictly. Check time-step sensitivity before interpreting results.

## Physical interpretation and limitations

Real tyres have spatial gradients and separate tread surface, tread bulk, belt, carcass and inner-liner temperatures. Heat can arise from slip work, hysteresis and deformation, and is transferred to road, air and internal layers. This repository accepts heat input as an external signal; it does not derive heat generation from tyre mechanics.

The single-node response cannot predict real warm-up time or an optimum operating window without calibrated parameters and suitable measurements.

## Development path

1. Introduce tread-surface, tread-bulk and carcass nodes.
2. Estimate heat generation from slip work and hysteresis.
3. Add thermal paths to road and ambient air.
4. Couple temperature to force-model parameters using measurements.
5. Validate against suitable embedded or infrared temperature measurements, accounting for sensor location and response.

The degradation demonstration is only an accumulated illustrative state, not a predictive tyre wear model.
