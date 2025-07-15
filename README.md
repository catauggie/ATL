# Machine Learning-Based Modular Framework for ATL

A modular deep learning framework for real-time control and defect prediction in Automated Tape Laying (ATL), implemented in Python using PyTorch.

## 🧠 Key Features

- **Feature Encoder**  
  Extracts latent representations from:
  - Thermal profiles (e.g., moving average-filtered \( T_P(t) \))
  - 3D point cloud features (geometry, surface normals, curvatures)
  - Process parameters (e.g., speed, power)

- **Thermal Surrogate Head**  
  Predicts peak temperature \( T_{\max} \) and melt dwell time \( \tau_{\text{melt}} \) using a fully connected regression model.

- **Defect Segmentation Head**  
  Classifies point cloud data into defect classes (e.g., normal, wrinkle, gap, overlap) using fused latent features and a segmentation network.

- **Control Policy Head**  
  Outputs deterministic control actions (e.g., laser power, head velocity) to regulate process conditions via a policy network.

- **Training Loop & Inference**  
  Example forward pass, loss computation (including thermal loss, cross-entropy segmentation loss with total variation), and placeholder reinforcement learning head.

---

## 📦 Metadata

| Field              | Value                                                                 |
|-------------------|-----------------------------------------------------------------------|
| **Title**          | Machine Learning-Based Modular Framework for ATL                     |
| **Version**        | v1.0.0                                                                |
| **Authors**        | Your Name, Collaborator Name                                         |
| **Repository**     | [GitHub Repository](https://github.com/your-username/atl-ml-framework) |
| **License**        | MIT                                                                  |
| **Language**       | Python 3.10+                                                         |
| **Dependencies**   | `torch`, `numpy`                                                     |
| **License**        | MIT License                                                          |
| **Keywords**       | ATL, PyTorch, Defect Detection, Thermal Modeling, Control, ML        |

---

## 📚 Description

This framework supports the development of ML-enhanced ATL digital twins. It provides modular components for:

- **Surrogate modeling**: Physics-aware regression of thermal behavior.
- **Semantic segmentation**: Real-time classification of geometric anomalies.
- **Policy control**: Closed-loop control via reinforcement learning strategies.
- **Training & Inference**: Easily extendable pipeline for supervised and hybrid model learning.

The system can be integrated with:
- Custom data loaders (e.g., FEM results, thermal logs, 3D scans)
- Real-time sensor feedback and embedded deployment
- Offline or online policy refinement

---

## 🚀 Use Cases

- Training surrogate models for ATL thermal behavior
- Real-time prediction of defects using 3D geometric data
- Closed-loop adaptive control of process parameters
- Benchmarking FEM vs. ML-driven ATL predictions
- Building hybrid digital twins for composite manufacturing

---

## 📇 Citation

If you use this framework, please cite it as:

```bibtex
@software{yourname2025atl,
  author = {Your Name and Collaborator Name},
  title = {Machine Learning-Based Modular Framework for ATL},
  year = {2025},
  version = {1.0.0},
  url = {https://github.com/your-username/atl-ml-framework}
}
