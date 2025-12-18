# Physics-Informed Neural Network for Energy Modeling in Milling Processes

This repository contains the implementation, datasets, and experiments for Physics-Informed Neural Networks (PINNs)** applied to **spindle power / energy prediction in milling operations.  
The work compares **purely data-driven Artificial Neural Networks (ANNs)** with **Soft-Constraint PINNs** and **Hybrid PINNs**, highlighting the advantages of physics-guided learning for **robust extrapolation, physical consistency, and explainability**.



## 📌 Key Contributions

- Comparison of **ANN, Soft PINN, and Hybrid PINN** for milling power prediction  
- Validation using **25 real gear-profile milling experiments**
- **Extrapolation testing** under unseen cutting conditions (e.g., 4 mm depth of cut, 1920 rpm)
- Integration of **machining physics (cutting force & power models)** into neural training
- **Explainable AI (SHAP)** analysis to interpret feature influence
- Demonstrates superior **generalization and robustness** of Hybrid PINNs

## Project Structure 
├── data/
│ ├── raw/ # Experimental milling power data
│ ├── processed/ # Normalized and curated datasets
│
├── models/
│ ├── ann.py # Baseline ANN model
│ ├── pinn_soft.py # Soft-constraint PINN
│ ├── pinn_hybrid.py # Hybrid PINN (multi-task formulation)
│
├── training/
│ ├── train_ann.py
│ ├── train_pinn_soft.py
│ ├── train_pinn_hybrid.py
│
├── evaluation/
│ ├── metrics.py # MSE, MAE, R²
│ ├── extrapolation_tests.py
│
├── explainability/
│ ├── shap_analysis.py # SHAP feature attribution
│
├── figures/ # Generated plots for paper
├── requirements.txt
├── README.md
└── LICENSE
