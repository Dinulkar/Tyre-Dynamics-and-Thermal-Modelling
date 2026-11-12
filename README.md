# Tyre-Dynamics-and-Thermal-Modelling

![Project Status](https://img.shields.io/badge/Status-In%20Progress-orange)

## Modelling Framework and Development Methodology

The project will be developed in progressive stages, starting with the fundamental principles of tyre dynamics and advancing towards an integrated tyre force, thermal and degradation simulation framework.

Each stage will include theoretical investigation, mathematical formulation, model implementation, simulation, result analysis and verification wherever suitable reference data are available.

### 1. Tyre Dynamics Theory
**Understand slip, forces and tyre-road interaction.**

The first stage focuses on understanding the physical principles behind tyre force generation during acceleration, braking and cornering.

**Planned approach:**
- Study the fundamentals of tyre-road interaction and friction.
- Understand longitudinal slip ratio and lateral slip angle.
- Investigate the relationship between vertical load and tyre force generation.
- Study the behaviour of longitudinal force (Fx), lateral force (Fy) and normal force (Fz).
- Develop simplified mathematical equations to describe longitudinal and lateral tyre forces.
- Implement the initial models in MATLAB and Python.
- Simulate tyre behaviour under different slip and normal-load conditions.
- Analyse force characteristics and identify the limitations of simplified models.

**Expected outcome:** A basic tyre dynamics model capable of illustrating longitudinal and lateral force characteristics as functions of tyre operating conditions.

### 2. Pacejka Magic Formula Modelling
**Mathematically represent nonlinear tyre force characteristics.**

The second stage introduces the Pacejka Magic Formula to represent the nonlinear relationship between tyre slip and generated forces.

**Planned approach:**
- Study the mathematical structure and physical interpretation of the Pacejka Magic Formula.
- Understand the influence of the B, C, D and E coefficients.
- Implement the Magic Formula for longitudinal and lateral pure-slip conditions.
- Investigate how changes in model parameters influence tyre force characteristics.
- Generate force-versus-slip curves for different parameter combinations.
- Investigate parameter estimation and curve fitting using reference or available tyre datasets.
- Compare the Magic Formula outputs with the simplified tyre models developed in Stage 1.
- Evaluate model behaviour and document assumptions and limitations.

**Expected outcome:** A parameterised tyre force model capable of reproducing nonlinear force-versus-slip characteristics using selected Magic Formula coefficients.

### 3. Tyre Thermal Modelling
**Investigate temperature development, heat transfer and warm-up behaviour.**

The third stage focuses on the thermal behaviour of a tyre under different operating conditions. The objective is to establish a simplified thermal model and progressively improve its representation of tyre temperature development.

**Planned approach:**
- Study the fundamental principles of heat generation and heat transfer in tyres.
- Investigate the effects of friction, slip, load and operating conditions on thermal behaviour.
- Develop an initial lumped-parameter thermal model using an energy-balance equation.
- Represent heat input, heat capacity and heat dissipation to the surrounding environment.
- Implement the thermal model using MATLAB and Python.
- Simulate temperature development under different operating conditions.
- Investigate warm-up and cooling characteristics.
- Study how temperature can influence tyre force characteristics.
- Identify the additional parameters and experimental data required for more realistic thermal modelling.

**Expected outcome:** An initial thermal simulation model capable of investigating tyre temperature development, warm-up and cooling behaviour.

### 4. Tyre Wear and Performance Degradation
**Investigate how tyre performance changes with operating conditions.**

This stage will explore simplified approaches to representing tyre wear and performance degradation.

**Planned approach:**
- Study the factors influencing tyre wear and performance degradation.
- Investigate the relationship between operating conditions, temperature and tyre performance.
- Identify suitable simplified degradation indicators and mathematical relationships.
- Develop an initial degradation model using clearly stated assumptions.
- Simulate the influence of changing degradation parameters on tyre performance.
- Investigate possible interactions between thermal behaviour, tyre forces and degradation.

**Expected outcome:** A preliminary degradation model that can be used to investigate how assumed wear or degradation effects influence tyre performance.

### 5. Combined Tyre Simulation
**Integrate tyre forces, temperature and degradation into a common framework.**

The final development stage aims to bring the individual models together into a combined simulation framework.

**Planned approach:**
- Integrate the longitudinal and lateral tyre force models.
- Incorporate the Pacejka Magic Formula into the force prediction framework.
- Introduce tyre temperature as an additional operating variable.
- Investigate temperature-dependent changes in tyre force characteristics.
- Incorporate the simplified degradation model.
- Define the required model inputs, outputs and internal parameters.
- Develop simulation scenarios representing acceleration, braking and cornering.
- Analyse the combined model response under different operating conditions.
- Compare simulation outputs with reference data where available.
- Document model assumptions, limitations and possible improvements.

**Expected outcome:** A modular tyre simulation framework combining force generation, thermal response and simplified degradation effects.

### 6. Simulation, Parameter Estimation and Validation

Model development will be supported by a consistent simulation and evaluation process.

**Planned workflow:**

1. **Literature and theory review:** Identify the physical principles, equations and modelling approaches relevant to each subsystem.
2. **Mathematical formulation:** Define the governing equations, assumptions, parameters, inputs and outputs.
3. **Model implementation:** Develop modular functions in MATLAB and Python.
4. **Simulation:** Run the models under different operating conditions and parameter combinations.
5. **Visualisation and analysis:** Generate plots, analyse trends and investigate model sensitivity.
6. **Parameter estimation:** Estimate suitable model parameters using reference datasets where available.
7. **Verification and validation:** Check mathematical consistency, numerical behaviour and agreement with available reference or experimental data.
8. **Documentation:** Record the modelling approach, results, assumptions and limitations for each development stage.

**Validation note:** Simulation results generated using assumed or illustrative parameters will be identified as such. Experimental validation will only be claimed when suitable measured data and a documented comparison are available.

### Future Development

Potential extensions of the project include:
- More advanced Pacejka tyre models and combined-slip behaviour.
- Load-, camber- and temperature-dependent tyre characteristics.
- Multi-node tyre thermal models.
- More physically representative heat-generation and heat-transfer mechanisms.
- Improved tyre wear and degradation modelling.
- Integration with vehicle dynamics simulations.
- Investigation of tyre behaviour under motorsport operating conditions.
