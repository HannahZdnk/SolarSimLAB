# 🌞 COMSOL Temperature Data Analyzer for Solar Simulation Lab

This repository contains Python notebooks for processing `.txt` files exported from **COMSOL Multiphysics**. It is specifically designed for the **Solar Simulation & Heat Transfer Lab**, where thermal data is analyzed across different depths in a material.

## 📈 Overview

These Jupyter Notebooks are designed to automate the analysis of thermal simulation data exported from **COMSOL**. The workflow begins with a `.txt` file containing simulation output, which is **loaded directly into the notebook code**.

Once loaded, the notebooks:

- **Parse and organize temperature data** as a function of **depth (Z)** from the material surface.
- **Compute key metrics** including:
  - **Average temperature** at each depth
  - **Average temperature change (ΔT)** between data points
- **Fit the cleaned data** to both:
  - A **polynomial model** using `numpy.polyfit`
  - A **logarithmic model** using `scipy.optimize.curve_fit`
- **Evaluate model accuracy** using the **R² score** (coefficient of determination)
- **Automatically generate and export graphs/images** that:
  - Show raw data and fitted curves
  - Visually compare model fits
  - Are ready for inclusion in lab reports
All analysis is performed using **Jupyter Notebooks** with an emphasis on clarity and automation for lab reporting.

---


## 🔧 Requirements

Make sure you have the following Python packages installed:

```python
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
from sklearn.metrics import r2_score
from scipy.optimize import curve_fit
```

Install them with:

```bash
pip install pandas matplotlib numpy scikit-learn scipy
```

---

## 📊 Example Output Plots

### 🔹 Temperature vs Depth – Best Fit Overlay

![Overlay of Best Fit Models - Temperature](overlay_best_fit.png)

---


## 💡 How to Use

1. Place your `.txt` files from COMSOL into the `data/` directory.
2. Open either notebook:
   - `notebook_avg_temp.ipynb` for average temperature
   - `notebook_avg_dT.ipynb` for average temperature change (ΔT)
3. Run the cells to:
   - Load and process data
   - Fit models
   - Generate and save plots

All results (including R² scores and model parameters) are displayed and plotted for use in lab reports or further research.

---
