# Post-Processing Toolkit for Automated EOS Analysis

**Developed during a project internship at Bhabha Atomic Research Centre (BARC) - Summer 2026**

## 📖 Overview
This Python-based computational toolkit automates the extraction and mathematical analysis of Energy-Volume data generated from Density Functional Theory (DFT) simulations. It was built to replace manual interpolation with a robust, automated curve-fitting architecture, allowing researchers to quickly determine fundamental solid-state properties like Ground State Energy ($E_0$), Equilibrium Volume ($V_0$), and Bulk Modulus ($B_0$).

## ✨ Key Features
* **Smart Data Parser:** Built with custom exception handling to automatically scan messy `.txt` output files, ignore strings/headers, and cleanly extract raw floating-point Volume and Energy data.
* **Multi-Model EOS Support:** Automatically fits the DFT data to four distinct theoretical Equations of State:
  * Murnaghan
  * Birch-Murnaghan (3rd Order)
  * Vinet-Rose
  * Poirier-Tarantola (Logarithmic)
* **Advanced Mathematical Optimization:** Utilizes the Levenberg-Marquardt algorithm via `scipy.optimize.curve_fit` for highly accurate non-linear least-squares fitting. Features a dynamic initial-guess engine that adapts to any element on the periodic table.
* **Theoretical Pressure Engine:** Calculates the theoretical pressure dynamically using the numerical derivative $P = -dE/dV$ and exports the results in GPa.
* **High-Density Data Generation:** Generates and exports ultra-dense 1000-point `.txt` datasets (Volume, Energy, Pressure) for secondary analysis.
* **Publication-Ready Graphing:** Uses `matplotlib` to generate standalone high-density plots and comparative overlays of multiple EOS models.

## 💻 Tech Stack
* **Language:** Python 3.x
* **Core Libraries:** `numpy`, `scipy`, `matplotlib`

## 🚀 How to Run the Software

1. **Clone the repository and install dependencies:**
   Ensure you have the required scientific libraries installed on your machine.
   ```bash
   pip install numpy scipy matplotlib
