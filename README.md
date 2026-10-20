# CMP Process Modeling and Planarization Efficiency Study using Sentaurus TCAD

This project models the Chemical Mechanical Planarization (CMP) step of semiconductor fabrication using Synopsys Sentaurus TCAD, to study how effectively CMP flattens an uneven wafer surface. A trench is etched into a silicon substrate, an oxide layer is deposited over it (creating a bump in the surface known as "oxide overburden"), and CMP is then simulated to polish the surface flat. This matters because every advanced chip relies on CMP to keep each layer flat enough for the next layer's lithography to stay in focus — without it, multilayer interconnect stacks in modern CMOS, FinFET, and memory devices would not be manufacturable.

## Skills & Tools Demonstrated

- Synopsys Sentaurus TCAD, specifically the SProcess module, for semiconductor process simulation
- TCL scripting for defining process steps (masking, etching, deposition, planarization) in SProcess
- Process modeling: anisotropic etching, isotropic oxide deposition (Deal–Grove oxidation model), and CMP (Preston-equation-based material removal)
- Surface topography and planarization analysis using Sentaurus Visual
- Quantitative process evaluation: step-height reduction and planarization efficiency calculation
- Technical reporting and literature review of CMP mechanisms, materials, and industrial applications

## What Was Built

- A 2D process flow in Sentaurus SProcess: silicon substrate initialization (phosphorus-doped, 1×10^15 cm⁻³), a lithographic trench mask (3-7 µm opening), and anisotropic silicon etching to a 0.4 µm trench depth.
- An oxide deposition step (~0.7 µm SiO₂, isotropic) that intentionally creates a non-planar surface with oxide overburden above the trench, modeled using the Deal-Grove oxidation approach.
- A CMP planarization model based on the Preston material-removal concept, where elevated regions are preferentially polished down to flatten the surface.
- Pre-CMP vs. post-CMP surface profile extraction and comparison plots generated in Sentaurus Visual to visualize and quantify the planarization.
- A full technical report and presentation covering process methodology, results, industrial relevance, known limitations of current CMP models, and future scope.

## Results

- Achieved a **planarization efficiency of 84.2%**, calculated from step-height reduction: the pre-CMP surface height variation of ~1.9 µm was reduced to ~0.3 µm after CMP.
- Confirmed successful trench formation (0.4 µm depth, near-vertical sidewalls) and complete, uniform oxide gap-fill prior to planarization.
- Demonstrated that CMP, modeled as an ideal transform-cut/Preston-based process, removes essentially all surface topography created by etching and deposition, validating the core CMP mechanism of pressure-driven preferential material removal.

## Repository Structure

- `Reports/` — Full written project report covering methodology, simulation setup, results, and discussion.
- `Presentation/` — Final project presentation slides.
- `Output_Plots/` — Pre-CMP vs. post-CMP surface profile plots generated in Sentaurus Visual.
- `Reference_Papers/` — Literature reviewed on CMP mechanisms, slurry chemistry, materials, and defect formation.

## Author

Jai B Shah, B.Tech VLSI Design and Technology, VIT Vellore.
