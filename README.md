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


## 📈 Results Summary

| Model        | Interpolation (R²) | Extrapolation | Physical Consistency |
|--------------|-------------------|---------------|---------------------|
| ANN          | **0.954**         | ❌ Weak       | ❌ Low              |
| Soft PINN    | 0.934             | ✅ Good       | ✅ Moderate         |
| Hybrid PINN  | 0.920             | ✅ **Best**   | ✅ **High**         |

- ANN performs best **within training range**
- Hybrid PINN performs best **under unseen conditions**
- SHAP confirms **spindle speed and feed rate** as dominant features (up to +0.68 influence)


## Reproducibility

Training epochs: 300

Batch size: 32

Optimizer: Adam

Data split: 80% training / 20% testing

Normalization: Min–Max scaling
