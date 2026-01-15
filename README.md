# EV Thermal & Energy Analysis Notebooks

This repository contains small, explainable Python notebooks for estimating auxiliary (HVAC/thermal) energy usage
and its impact on EV range.

These are intended as concept-level engineering tools with transparent assumptions.

## Notebooks
- HVAC auxiliary energy budget and range impact (starter)

## Planned additions
- Battery heat generation estimation
- Cooling power vs thermal load trade studies
- 
## Engineering Assumptions

- Constant auxiliary load during trip
- Fixed traction energy consumption
- No transient HVAC dynamics modeled

Future versions will include temperature-dependent loads and compressor efficiency curves.
- **battery_thermal_trade_study.ipynb** – Physics-based battery heat generation and lumped thermal model with sensitivity analysis.
- **hvac_battery_combined_energy_thermal.ipynb** – Coupled traction, HVAC, and battery thermal model comparing city vs highway driving scenarios.
