# 🧬 Pathway-Based AI Detection of Pemphigus Vulgaris

> A deep learning diagnostic system for early detection of Pemphigus Vulgaris using pathway-informed Transformer architecture and proteomic microarray data.

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Research%20Complete-brightgreen)

---

## 📌 Overview

Pemphigus Vulgaris (PV) is a rare, life-threatening autoimmune blistering disorder caused by autoantibodies targeting desmosomal proteins (DSG1, DSG3). Conventional diagnosis is invasive and slow. This project builds an AI-powered early detection system using biological pathway knowledge and deep learning.

---

## 🏆 Key Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| **Pathformer (Ours)** | **91.29%** | **0.90** | **0.91** | **0.90** |
| Random Forest | 78% | — | — | — |
| SVM | 74% | — | — | — |

---

## 🧠 Architecture
Input (Proteomic Features)
↓
Pathway Sparse Neural Network (PSNN)
[14,280 proteins → 347 pathway embeddings via KEGG + Reactome]
↓
Transformer Encoder (Criss-Cross Attention)
↓
Fully Connected Classifier
↓
Output: PV Patient / Healthy Control

---

## 📊 Dataset

- **Source:** Kalantari-Dehaghi et al. (2013) — Protein microarray study
- **Type:** Proteomic reactivity profiles (autoantibody microarray)
- **Classes:** PV Patients vs. Healthy Controls
- **Note:** Raw patient data is not included (privacy compliance). Contact original authors for access.

---

## 🗂️ Project Structure
PathformerPV/
├── notebooks/    → Full model pipeline
├── app/          → Streamlit diagnostic web app
├── reports/      → Synopsis and final report
└── assets/       → Diagrams and result figures

---

## 🚀 How to Run

**1. Clone the repo**
```bash
git clone https://github.com/reshma-begam/PathformerPV.git
cd PathformerPV
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the notebook**
```bash
jupyter notebook notebooks/mini_prjc_pathformer.ipynb
```

**4. Launch the app**
```bash
streamlit run app/app.py
```

---

## 🔬 Methodology

1. **Data Preprocessing** — Missing value imputation, normalization, SMOTE for class imbalance
2. **Pathway Mapping** — KEGG + Reactome → 347 unique biological pathways
3. **Model** — Pathformer-inspired Transformer with criss-cross attention
4. **Training** — Adam optimizer, Stratified K-Fold CV, early stopping
5. **Explainability** — SHAP values for pathway-level biological interpretation

---

## 🧬 Top SHAP Pathways

| Pathway | SHAP Score |
|---|---|
| Immune Response Activation | 0.084 |
| Cell Adhesion Molecules | 0.079 |
| Keratinocyte Differentiation | 0.074 |
| Cytokine Signaling | 0.068 |
| Apoptosis Regulation | 0.062 |

---

## 🛠️ Tech Stack

`Python` `TensorFlow` `PyTorch` `Scikit-learn` `SHAP` `Pandas` `NumPy` `Streamlit` `Matplotlib` `Seaborn` `KEGG` `Reactome`

---

## 📄 References

- Liu et al. (2024) — Pathformer: multi-scale transformer using biological pathways
- Kalantari-Dehaghi et al. (2013) — Pemphigus vulgaris autoantibody profiling
- Hao et al. (2018) — P-NET: Biologically informed deep neural network

---

## 👩‍💻 Author

**Reshma Begam K** — M.Sc. Data Science, SASTRA Deemed University

[LinkedIn](https://linkedin.com/in/reshma-begam) · [GitHub](https://github.com/reshma-begam)

---

## 📜 License

MIT License
