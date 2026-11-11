# Pacejka Magic Formula: Compact Pure-Slip Form

## Equation

This project implements the compact form:

\[
y=D\sin\{C\tan^{-1}[Bx-E(Bx-\tan^{-1}(Bx))]\}+S_v
\]

where \(x=x_{\mathrm{raw}}+S_h\).

- \(B\): stiffness factor.
- \(C\): shape factor.
- \(D\): peak/scale factor.
- \(E\): curvature factor.
- \(S_h,S_v\): horizontal and vertical shifts.

For longitudinal force, x may be slip ratio and y force in N. For lateral force, x is commonly slip angle in radians. Coefficient units and interpretation depend on the selected equation and output.

## Implementation and fitting

`Python/pacejka_model.py` and `MATLAB/Pacejka_Magic_Formula/magic_formula.m` implement this compact equation. `Python/parameter_estimation.py` estimates B, C, D and E with zero shifts using nonlinear least squares through SciPy's `curve_fit`.

Check coordinate signs and units first. Group data by load, pressure, temperature and camber. Fit calibration data only, inspect parameter plausibility and residuals, then test on an independent dataset. Nonlinear fitting can be sensitive to initial guesses, parameter correlation, noise and operating-range coverage.

## Limitations

This is not a complete MF-Tyre or MF-Swift implementation. It omits load-dependent coefficient equations, combined slip, camber dependencies, turn slip, pressure and temperature effects, transient relaxation, moments and structural dynamics. Do not imply manufacturer-level model equivalence.
