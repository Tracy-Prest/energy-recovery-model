# energy-recovery-model
There is an increase in the greenhouse gas (GHG) emissions due to the growth of world energy demand. Flaring in the oil and gas industry is common practice that has environmental and economic implications.

The environmental impact of flaring contributes to climate change and global warming. Methane is a potent GHG that is more effctive at trapping heat than carbondioxide (CO2).

This project explores how gas that should be flared can be converted to electricity using publicly available data.

A Gas to power engineering design using Onshape Computer Aided Design (CAD), Simscale computational fluid dynamics (CFD) parameters, and analytical performance modeling scripts. The project integrates a primary engine block, a combined heat and power (CHP) thermal capture jacket, an exhaust stack, and a dedicated ventilation layout housed within an optimized 20-foot shipping container enclosure.

The core objective of this project is to design and validate a decentralized, modular Gas-to-Power (G2P) with Combined Heat and Power (CHP) energy recovery system housed in a standard 40-foot shipping container. The project aims to eliminate wasteful open-air gas flaring at upstream oil wells by capturing associated methane gas and converting it into two productive resource streams: 716 kW of clean electrical power and 751.8 kW of industrial thermal heat. 

# System Specifications and Operating Parameters
•	Location Baseline: Nigeria (Ambient Temperature: 303.15 K / 30 degrees Celsius, Atmospheric Pressure: 101325 Pa).
•	Thermal Power Input: 306 kW absolute power source mapped to the engine block volume.
•	Ventilation Flow Rate: 8 m/s freestream velocity intake balanced through natural pressure relief exhaust venting (Ux).
•	Enclosure Shell: Structural steel framework with internal fluid-solid thermal interaction through SimScale Immersed Boundary Method (IBM) CHT solver.

# Computer Aided Design (Onshape)
I designed the assembly with measurements and parameters to ensure proper multi-material assignment and avoid geometric overlapping errors during thermal meshing. They include:
•	Main Engine Block: The primary source of mechanical and thermal energy generation.
•	CHP Thermal Jacket: It captures high-grade waste heat from the engine core.
•	Exhaust Stack: It directs high-temperature flue gases vertically toward the enclosure exit.
•	Container Enclosure: It houses the machinery while maintaining an optimized cross-flow ventilation corridor.

# Computational Fluid Dynamics Thermal Validation (SimScale)
I used the Conjugate Heat Transfer IBM solver for the simulation workflow to model convective cooling and thermal dissipation across the machinery surfaces.
•	Mesh Fineness: I configured the finessse at level 6 global resolution to prevent edge defeature on complex curved exhaust and CHP jacket geometries.
•	Boundary Conditions: I used freestream velocity intake at 8 m/s and applied it to the forward structural faces, matched with an ambient pressure outlet at 303.15 K on the opposing exhaust sector.
•	Gravity: I used -9.81 m/s2 Z-axis orientation to capture natural buoyancy and thermal plume displacement.

# Performance Metrics and Analytical Model
I executed the python scripts that yielded the following steady-state operational characteristics:
•	Electrical Output: 716 kW of continuous grid-ready electrical generation.
•	CHP Heat Recycled: 751.8 kW of recovered thermal energy for co-generation utility.
•	Overall System Efficiency: 82.0 percent total effective resource utilization.
•	Climate Impact Reduction: 47.60 kg of raw greenhouse methane gas mitigated per operating hour relative to unmanaged baseline releases.

