
# 📊 Outlier Detection using Probabilistic Methods: COPOD & ABOD

This project presents both a **presentation** and a **review paper** exploring two advanced probabilistic outlier detection methods — **COPOD** (Copula-Based Outlier Detection) and **ABOD** (Angle-Based Outlier Detection). The work was completed as part of the coursework at **TU Dortmund University**, Department of Statistics.

---

## 📌 Project Components

- **🎤 Presentation**: Introduced the core concepts of anomaly detection, focusing on the mathematical foundation, methodology, and visualization of COPOD and ABOD. 
- **📄 Review Paper**: Delivered a theoretical and performance-based comparison of COPOD and ABOD, highlighting use cases, strengths, and limitations based on empirical benchmarks.

---

## 🧠 Topics Covered

- **What is Outlier/Anomaly Detection?**
  - The process of identifying rare items/events/observations that deviate from expected patterns.

- **Probabilistic Methods Discussed:**
  - **COPOD**: Uses copulas to estimate joint tail probabilities of feature vectors, modeling multivariate dependency structures.
  - **ABOD**: Measures variance of angles between vectors for each point to estimate its likelihood of being an outlier.

---

## ⚙️ Techniques & Methodologies

### 🔹 COPOD Highlights
- Uses **empirical copula** and **ECDF** to detect tail probabilities.
- Works well with continuous numerical features and high-dimensional data.
- Sensitive to skewness and requires sufficient sample size for accurate tail estimation.
- Efficient and **interpretable** — feature-level contribution to outlier score can be tracked.

### 🔹 ABOD Highlights
- Computes **angle variance** among vector pairs for each observation.
- Robust in high dimensions where distance-based methods fail.
- High computational cost (O(n³)); improved with Fast-ABOD and LB-ABOD using `k-NN`.
- Struggles with angular alignment outliers and lacks density-awareness.

---

## 🔬 Empirical Evaluation

- Performance evaluated on **30 benchmark datasets** from the ODDS repository.
- **COPOD** outperformed **ABOD** in:
  - 24 out of 30 datasets in terms of ROC-AUC
  - Overall average ROC-AUC: COPOD = 0.8247, ABOD = 0.6900
  - Overall precision: COPOD = 0.5649, ABOD = 0.3512

---

## 📈 Key Insights

- **COPOD** is more scalable and interpretable but needs large datasets and continuous features.
- **ABOD** handles complex geometries well but is computationally expensive.
- Dataset characteristics should guide method selection: use COPOD for simpler/structured data, ABOD for geometrically complex data.

---

## 🛠️ Tools & Technologies

- **Python 3.12.6**
- **Libraries**: pandas`, `numpy`, `matplotlib`, `scikit-learn`
- **IDE**: Visual Studio Code

---

## 📚 References

- Li et al., *COPOD: Copula-Based Outlier Detection*
- Kriegel et al., *Angle-Based Outlier Detection in High-Dimensional Data*
- ODDS Repository, PYOD Toolbox

