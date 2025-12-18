# Physics-Informed Neural Network for Energy Modeling in Milling Processes

Nature creates us and gives brain. We observe nature and develops Laws of Physics. We mimic Brain and develop Artificial neural network (ANN). ANN evolved to Physics-Informed Neural Network (PINN) with physical laws. 

This repository contains the implementation, datasets, and experiments for Physics-Informed Neural Networks (PINNs) applied to spindle power / energy prediction in milling operations.  
The work compares **purely data-driven Artificial Neural Networks (ANNs)** with **Soft-Constraint PINNs** and **Hybrid PINNs**, highlighting the advantages of physics-guided learning for **robust extrapolation, physical consistency, and explainability**.


![PINN](https://github.com/user-attachments/assets/4d73039d-d337-441e-b776-5fcfbe2e12eb)

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

## 🧠 Explainability (SHAP)

- Provides **feature-level contribution** to power prediction
- PINNs show **balanced, physics-consistent feature attribution**
- ANN tends to overemphasize spindle speed

## 🤝 Acknowledgment

This work was supported by the Advanced Institute of Manufacturing with High-Tech Innovations (AIM-HI) under the Higher Education Sprout Project, Ministry of Education (MOE), Taiwan.


## Reproducibility

Training epochs: 300

Batch size: 32

Optimizer: Adam

Data split: 80% training / 20% testing

Normalization: Min–Max scaling
