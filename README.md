# EV Thermal & Energy Analysis Notebooks

This repository contains small, explainable Python notebooks for exploring **auxiliary thermal loads and their impact on EV energy consumption and range**.

The goal of these notebooks is to build **transparent, physics-inspired system models** that help visualize how thermal systems (HVAC, cabin cooldown, battery heat generation) interact with overall vehicle energy usage.

These models are intentionally simplified and designed as **concept-level engineering tools** rather than full OEM simulation environments.

---

# Notebook Series

### 1️⃣ HVAC Energy Budget and Range Impact
**hvac_energy_budget.ipynb**

Introductory notebook estimating how steady auxiliary HVAC loads influence overall EV energy consumption and range.

Focus:
- Auxiliary load estimation
- Range sensitivity to HVAC power
- Basic energy accounting

---

### 2️⃣ Coupled HVAC + Battery Energy Interaction
**hvac_battery_combined_energy_thermal.ipynb**

Explores the interaction between traction energy usage, HVAC loads, and battery thermal behavior.

Focus:
- Combined traction and HVAC energy consumption
- City vs highway driving comparisons
- Simplified battery thermal coupling

---

### 3️⃣ Battery Thermal Trade Study
**battery_thermal_trade_study.ipynb**

Physics-based estimation of battery heat generation using a lumped thermal model.

Focus:
- \(I^2R\) heat generation
- Lumped battery thermal capacitance
- Sensitivity analysis to current and cooling effectiveness

---

### 4️⃣ Closed-Loop HVAC + Battery Conditioning
**closed_loop_hvac_battery_conditioning_hot_cold.ipynb**

Concept-level exploration of how HVAC systems may interact with battery thermal management during hot and cold conditions.

Focus:
- Coupled thermal loads
- Cabin conditioning vs battery conditioning interactions
- Simplified control behavior

---

### 5️⃣ Transient Cabin Cooldown Model
**01_aux_thermal_transient_model.ipynb**

A simplified transient model that simulates **hot-soak cabin cooldown and auxiliary energy consumption** during the first minutes of vehicle operation.

Focus:
- Cabin air and interior thermal mass modeling
- Transient HVAC cooling load
- Compressor power estimation using COP
- Battery thermal node interaction
- Ambient temperature sensitivity study

Example insight:

| Ambient | Cooldown Time | Compressor Energy |
|--------|---------------|------------------|
| 30°C | 6.47 min | 0.517 kWh |
| 35°C | 8.70 min | 0.604 kWh |
| 40°C | 11.57 min | 0.710 kWh |
| 45°C | 15.40 min | 0.826 kWh |

This illustrates how **environmental conditions alone can increase auxiliary energy consumption by ~60% during cabin cooldown events.**

---

# Modeling Philosophy

These notebooks prioritize:

- **Transparency over complexity**
- **Physics-based intuition**
- **Clear engineering assumptions**

Rather than replicating detailed OEM simulation environments, the goal is to build **lightweight models that clearly illustrate system-level trade-offs**.

---

# Key Simplifying Assumptions

Across the notebooks, several simplifying assumptions are commonly used:

- Lumped thermal masses
- Simplified heat transfer relationships
- Constant or simplified drive load assumptions
- Simplified HVAC COP models
- No detailed refrigerant cycle modeling
- No solar radiation or infiltration modeling (in Version 1 studies)

Future versions may expand the models to include:

- Temperature-dependent HVAC efficiency
- Air infiltration and cabin leakage effects
- Battery thermal derating interactions
- Transient drive cycles
- Cabin preconditioning scenarios

---

# Purpose of This Repository

This repository serves as a collection of **engineering exploration notebooks** for:

- EV thermal system intuition
- Auxiliary energy impact analysis
- Simple system-level modeling

The notebooks are intentionally written to remain **readable, modifiable, and explainable**, allowing engineers to quickly explore "what-if" thermal scenarios.

---

# Author

Srikantan Natarajan  
Automotive Systems Engineer – Thermal Systems / HVAC Development
