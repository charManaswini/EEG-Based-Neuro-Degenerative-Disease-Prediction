# EEG-Based-Neuro-Degenerative-Disease-Prediction
This project leverages graph-based deep learning and statistical connectivity features to classify neurodegenerative diseases such as Alzheimer's and Frontotemporal Dementia (FTD) using EEG signals. 

## 📌 Project Highlights

- **99% classification accuracy** for AD vs. FTD vs. Healthy controls
- Combines **time-domain**, **frequency-domain**, and **graph-based features** (e.g., PLV, MI, Correlation)
- Gender-specific analysis to explore biomarker differences
- Models validated with **cross-validation and overfitting checks**
- Graph connectivity visualizations for spatial electrode interpretability

---

## 🔍 Methodology

### 1. Data Acquisition
- EEG recordings from OpenNeuro dataset (88 participants)
- Preprocessing via `MNE` (filtering, epoching, re-referencing)

### 2. Feature Extraction
- **Time-Domain**: Signal energy, variance, zero-crossing
- **Frequency-Domain**: Band power (delta, theta, alpha, beta)
- **Graph Features**: Adjacency matrices based on:
  - Phase Locking Value (PLV)
  - Mutual Information (MI)
  - Pearson Correlation

### 3. Modeling & Evaluation
- Classifiers: Random Forest, XGBoost, MLP
- Dimensionality reduction via PCA and Autoencoder
- Evaluation metrics: Accuracy, Precision, Recall, F1-Score

### 4. Explainability
- Gender metadata appended to feature set
- Channel-specific analysis for region-wise importance
- Visual t-SNE plots and electrode-wise performance comparison

---

## 🛠 Tech Stack

- **Python**
- **MNE** for EEG preprocessing
- **NetworkX** for graph feature computation
- **Scikit-learn**, **XGBoost** for modeling
- **Matplotlib**, **Seaborn** for visualization

---

## 📈 Results

- **99% Accuracy** (AD vs FTD) using fused features
- High interpretability across dominant electrodes (Fp2, Pz, Cz)
- Clear separation in t-SNE plots confirming feature discrimination
