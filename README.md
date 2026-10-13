# energy-recovery-model
Containerised Gas-to-Power (G2P) with CHP Energy Recovery System

Every day, oil wells worldwide flare millions of cubic meters of associated petroleum gas straight into the open air. This isn't just a waste of valuable energy; it is an environmental disaster. Open-air flaring releases massive amounts of raw methane and carbon dioxide directly into our atmosphere, driving global climate change. 

I designed this project to eliminate this waste at the source. Instead of letting this gas burn in the open sky, my system captures the flare line, channels it into a mobile, containerised unit, and transforms a toxic environmental pollutant into two clean, productive resource streams: reliable electricity and industrial heat. 

**Primary Category:** Sustainable Energy Engineering / Clean Technology (CleanTech)
**Sub-Categories:** Thermal-Fluid Systems Design, Decarbonisation Engineering, Applied Computational Engineering
**Project Goal:** Design and validate a decentralised, modular Gas-to-Power (G2P) microgrid system to eliminate wasteful open-air methane flaring at upstream oil wells.

# Engineering Framework

This project bridges data-driven mathematical scripting, 3D Computer-Aided Design (CAD), and cloud-based Computational Fluid Dynamics (CFD) across a unified three-phase engineering pipeline:

# 1. Analytical System Modeling (Python)
* An ordinary differential equation (ODE) algorithm processes raw gas flaring datasets to calculate energy conversion thresholds. 
Pure methane gas combustion releases massive energy. This design successfully captures **716 kW of electrical grid power** and channels **751.8 kW of useful thermal heat** through a co-generation loop, hitting an overall system efficiency of **82.0%**.
**Environmental Impact:** Prevents **47.60 kg of raw, high-potency greenhouse methane gas** from escaping into the environment every single hour.

# 2. 3D Structural Architecture (Onshape)
- Engineered a space-optimised 3D assembly layout inside a standard 20-foot shipping container enclosure corridor.
- Fused the internal machinery components into a single, unified block using the **Boolean Union** tool to avoid multi-material mesh clashing.
**The Geometry:** 
  * Main Engine Block: Modelled as a solid `3.0m x 1.2m x 1.4m` structural base footprint matching a 1 Megawatt industrial class unit.
  * Exhaust Stack: A vertical `0.25m` diameter chimney pipe.
  * CHP Heat Exchanger: A concentric, thin-walled `0.45m` jacket wrapper (with a `0.02m` structural wall thickness) engineered to cycle waste thermal fluid.
  * Ventilation Windows: An unobstructed airflow corridor utilising a `1.5m²` square inlet on the back wall and a `1.2m` diameter circular extractor fan window on the front wall.

# 3. Thermal Ventilation Validation (SimScale)
* Validated system survival and heat mitigation using a high-fidelity **Conjugate Heat Transfer Immersed Boundary Method (IBM)** cloud physics solver.
**The Thermal Load:** The engine's remaining unrecovered waste heat (**306,000 Watts**) is applied directly to the internal machine block faces.
**Flow Configurations:** 
  * Intake (Square Window Sector Faces): Mapped as a **Freestream** boundary driving fresh air forward at **8 m/s** straight down the corridor (Ux axis).
  * Exhaust (Circular Window Sector Faces): Controlled through a **Pressure Outlet** boundary set to 0 Pa gauge pressure to simulate venting into the ambient environment.
  * Thermal Environment: Operational temperature baselines are locked to **303.15 K (30°C)** to replicate local climate conditions.
  * Mesh Parameters: Processed at a highly refined **Level 6 Fineness** grid density to completely prevent surface deformation and preserve the curved paths of the chimney stack and cooling jackets.
  * Gravity: Enabled along the vertical axis at **-9.81 m/s²** to accurately account for natural thermal buoyancy and convective air plumes.


# Repository Structure
Core transient systems ODE script and data visualizer.
Complete Onshape assembly STEP file.
High-resolution screenshots of the Onshape layout and SimScale velocity cut-planes.


# System Results Summary
The CFD wind tunnel calculations verify that drawing fresh ambient air at 8 m/s creates a powerful internal sweeping current. This convective loop successfully prevents thermal trapping, sweeping the 306 kW of engine waste heat cleanly out of the exhaust wind box. The simulation confirms that internal air temperatures stay safely below the **60°C operational limit**, proving that the physical package can reliably operate and survive in extreme ambient climates.
