# Bayesian Optimization of Barium Titanate Slurry Compositions

This repository contains the code, data, and workflows used to optimize
multi-component BaTiO₃ slurry formulations using Gaussian Process Regression (GPR)
and Bayesian optimization. The project combines rheological characterization with
machine learning–driven exploration of the mixture design space.

---

## 🔮 Notebooks

### **GPR.ipynb**
- Trains a Gaussian Process model on experimental data  
- Predicts the next candidate slurry compositions  
- Visualizes the posterior mean and uncertainty  
- Supports dense sampling of the feasible simplex for posterior mapping  

### **rheometry.ipynb**
- Extracts rheological parameters from measured flow curves  

---

## 📁 Data Structure

- **`all_batches.csv`** contains all mixture compositions and extracted rheological metrics.
- The **`data/`** directory holds the raw viscosity vs. shear-rate curves for each
  sample.

---

## 🚀 Workflow Summary

1. Run `rheometry.ipynb` to process rheological measurements and extract parameters.  
2. Append the processed results to `optimization_data/all_batches.csv`.  
3. Run `GPR.ipynb` to:
   - Train/update the GP model  
   - Evaluate the posterior penalty landscape  
   - Select the next optimal candidate for experimentation  

---

## 📦 Requirements

Main Python packages:
- `botorch`
- `gpytorch`
- `pandas`
- `numpy`
- `matplotlib`
- `scikit-learn`

Install with:

```bash
pip install -r requirements.txt

