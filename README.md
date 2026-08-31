# Multivariable-Influence-of-Process-Parameters-on-Bead-Geometry-in-Wire-Arc-Additive-Manufacturing
Complete reproducible dataset and analysis pipeline for 796 WAAM single-bead depositions, investigating how voltage, WFS, TS, and CTWD influence bead geometry, melt-pool behavior, and deposition stability across AISI 316 and ER70S-6 steels.

# 📘 README.md  
## Multivariable Influence of Process Parameters on Bead Geometry in Wire Arc Additive Manufacturing (WAAM)

This repository contains the full dataset, processing pipeline, and documentation for our study on how voltage (V), wire feed speed (WFS), travel speed (TS), and contact tip‑to‑work distance (CTWD) influence bead geometry, melt‑pool behavior, and deposition stability in Wire Arc Additive Manufacturing (WAAM). The dataset includes **796 single‑bead depositions** collected using high‑resolution profilometry and in‑situ electrical measurements.

The project establishes a **material‑aware, physics‑informed process–geometry mapping** for AISI 316 stainless steel and ER70S‑6 low‑carbon steel, supported by a reduced heat‑input model:

\[
Q \approx nVI/TS
\]

with current approximately proportional to WFS. Beyond mean bead height and width, the repository introduces **variance‑based stability metrics** that reveal stable, marginal, and unstable deposition regimes.

---

## Key Features

- **Large, traceable WAAM dataset** (796 depositions)  
- **High‑resolution profilometry** for bead height/width extraction  
- **WAAM Logger metadata** (V, I, WFS, TS, CTWD, material)  
- **Variance‑based stability metrics** for continuous stability assessment  
- **Material‑dependent geometric response** for AISI 316 vs ER70S‑6  
- **Physics‑informed heat‑input scaling**  
- **Reproducible analysis scripts** for geometry processing and heat‑input evaluation  

---

## Repository Structure

```
/WAAM-dataset/
│
├── raw_data/
│   ├── profilometry_scans/
│   ├── electrical_signals/
│   ├── machine_logs/
│   └── material_labels.csv
│
├── processed_geometry/
│   ├── bead_height_profiles/
│   ├── bead_width_profiles/
│   ├── variance_metrics/
│   └── summary_statistics.csv
│
├── metadata/
│   ├── parameter_table.csv
│   ├── calibration_notes.txt
│   └── equipment_specifications.pdf
│
├── analysis/
│   ├── geometry_processing.py
│   ├── stability_metrics.py
│   ├── heat_input_calculations.py
│   └── plotting_scripts/
│
└── schema/
    ├── data_dictionary.json
    ├── variable_definitions.md
    └── preprocessing_pipeline.md
```

---

## Scientific Summary

The dataset demonstrates that bead geometry and stability arise from **nonlinear interactions** among V, WFS, TS, and CTWD. Key findings include:

- **Voltage** increases melt‑pool fluidity, widening beads and increasing variance.  
- **WFS** increases current and heat input; high WFS causes spreading in AISI 316 but stable height‑dominated growth in ER70S‑6.  
- **Travel speed** inversely controls heat input; higher TS narrows beads and improves stability.  
- **CTWD** reduces current and heat input; low CTWD strengthens substrate bonding, while high CTWD enables controlled detachability.  
- **Material differences** arise from thermal diffusivity:  
  - ER70S‑6 dissipates heat rapidly → confined, stable beads  
  - AISI 316 retains heat → larger melt pools, higher variance  

---

## Example Results

Representative conditions (V = 12 V, TS = 150 mm/min, n = 0.8):

- Increasing WFS from 200 → 400 mm/min raises heat input from **384 → 768 J/mm**  
- AISI 316: height **3.8 → 2.6 mm**, width **5.2 → 8.0 mm**, variance ↑  
- ER70S‑6: height **3.5 → 4.2 mm**, width **4.8 → 6.5 mm**, variance remains low  

These trends highlight the importance of **material‑aware parameter selection**.

---

## Data & Code Availability

This repository includes:

- **Raw profilometry scans**  
- **Processed geometric descriptors**  
- **Complete parameter metadata**  
- **Analysis scripts** for geometry processing, stability metrics, and heat‑input calculations  
- **Full schema and documentation** for reproducibility  

---

## Applications

- WAAM process optimization  
- Physics‑informed machine learning  
- Melt‑pool modeling  
- Closed‑loop control development  
- Material‑aware parameter selection  
- Benchmarking for academic and industrial WAAM research  

---

## Citation

If you use this dataset or analysis pipeline, please cite:

```
Ebika, B., Ramasamy, V., Lewandowski, J., Loparo, K., & Ekeamadi, J.
"Multivariable Influence of Process Parameters on Bead Geometry in Wire Arc Additive Manufacturing."
2026.
```

---

## 🔧 Contact

For questions or collaboration inquiries, please contact:  
**BATHLOMEW EBIKA** — Case Western Reserve University

