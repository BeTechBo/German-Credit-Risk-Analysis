# ⚖️ Responsible & Ethical AI — German Credit Risk Analysis

A multi-module project applying responsible AI principles to a real-world credit scoring system, built for CSCE 4930 (Ethical AI) at the American University in Cairo. Each module tackles a distinct dimension of AI ethics: fairness auditing, explainability, robustness, and privacy.

*Note: The German Credit Dataset was chosen deliberately for its documented biases across sex, age, and nationality — making it an ideal testbed for stress-testing AI ethics principles in a high-stakes financial decision context.*

---

## 🗂️ Project Structure

| Module | Focus | Key Techniques |
|--------|-------|----------------|
| Module 1 | Fairness Audit & Bias Mitigation | Demographic Parity, Equalized Odds, Reweighting, Adversarial Debiasing |
| Module 2 | Explainability System Design | SHAP, LIME, Statistical Parity, TPR Gap Analysis |
| Module 3 | Robustness & Security Testing | Adversarial Perturbations, Input Noise, Subgroup Degradation |
| Module 4 | Privacy Risk & Privacy-Aware Design | Re-identification Risk, Differential Privacy, k-Anonymity |

---

## 🚀 Key Features

* **Fairness Audit & Bias Mitigation (Module 1)**
    * **Baseline Model Training:** Trained and justified a Decision Tree classifier on the German Credit Dataset, evaluating accuracy, precision, recall, and F1-score.
    * **Fairness Metrics:** Computed demographic parity, equalized odds, and calibration for each protected demographic group (sex, age) separately.
    * **Preprocessing Mitigation:** Applied reweighting/resampling techniques to the training data and measured the fairness-accuracy trade-off before and after.
    * **In-processing Mitigation:** Implemented a training-time fairness intervention (e.g., fairness constraints or adversarial debiasing) and compared results across all three model variants.
    * **Deployment Recommendations:** Analyzed which fairness metrics remained hardest to satisfy, which groups were most affected, and whether real-world deployment would be justifiable.

* **Explainability System (Module 2)**
    * **Global & Local Explanations:** Applied SHAP and LIME to interpret both overall model behavior and individual predictions.
    * **Fairness Metrics:** Measured Statistical Parity Differences and True Positive Rate gaps across protected groups: sex, age, and foreign worker status.
    * **Dual Model Comparison:** Evaluated a Decision Tree and Logistic Regression side-by-side on fairness and interpretability trade-offs.

* **Robustness & Security Testing (Module 3)**
    * **Adversarial Perturbation Testing:** Introduced at least 3 types of input perturbations (noise injection, feature flipping, boundary attacks) to measure model fragility.
    * **Subgroup Degradation Analysis:** Tracked how perturbations disproportionately affect protected demographic groups.
    * **Baseline vs. Perturbed Performance:** Documented accuracy, precision, recall, and F1 drop under each attack type.

* **Privacy Risk & Privacy-Aware Design (Module 4)**
    * **Privacy Threat Assessment:** Identified re-identification risks and sensitive attribute leakage within the dataset.
    * **Privacy-Preserving Techniques:** Implemented and evaluated k-anonymity and differential privacy mechanisms on the credit scoring pipeline.
    * **Privacy-Utility Trade-off Analysis:** Quantified the cost of privacy preservation on model performance.

---

## 📂 Notebook Highlights (For Reviewers)

Each module is self-contained with its own notebook and written report:

* **Module 1:** Focus on Parts 2–3 — preprocessing and in-processing mitigation comparisons, and Part 4 — fairness vs. accuracy trade-off visualizations and deployment recommendations.
* **Module 2:** Focus on Part 6 — TPR gap visualizations and Statistical Parity Difference tables across all three protected attributes.
* **Module 3:** Focus on Sections 5–6 — perturbation experiments, results tables, and subgroup impact analysis.
* **Module 4:** Focus on Part 1 — privacy threat assessment, and Part 2 — implementation of privacy-preserving mechanisms.

---

## 🛠️ Tech Stack

* **Language:** Python
* **Libraries:** scikit-learn, pandas, NumPy, matplotlib, seaborn, SHAP, LIME
* **Core Concepts:** Algorithmic Fairness, Bias Mitigation, Model Explainability, Adversarial Robustness, Differential Privacy, k-Anonymity.
* **Dataset:** [German Credit Dataset](https://archive.ics.uci.edu/ml/datasets/statlog+(german+credit+data)) — 1,000 samples, 20 features, binary creditworthiness classification.

---

## 💻 Usage

### Prerequisites

```
pip install pandas numpy scikit-learn matplotlib seaborn requests shap lime
```

### Running the Notebooks

Each module builds on the same data pipeline. Run them in order for full context:

```
Module_1.ipynb               → Fairness Audit & Bias Mitigation
Module_2.ipynb               → Explainability & Fairness
Module_3_Code.ipynb          → Robustness & Security
module4_full_notebook.ipynb  → Privacy
```

---

## 📁 Project Structure

```
├── Module_1.ipynb
├── Report (Module 1).pdf
├── Module_2.ipynb
├── Final Report Milestone 2 AI ethics.pdf
├── Module_3 Code.ipynb
├── Report (Module 3).pdf
├── module4_full_notebook.ipynb
├── Final Submission Module 4.pdf
└── README.md
```

---

## 🔮 Roadmap & Future Improvements

- [ ] **Module Integration:** Build a unified pipeline that runs all four ethical checks end-to-end on any binary classifier.
- [ ] **Fairness-Aware Retraining:** Extend in-processing mitigation experiments with more advanced techniques (e.g., fairness GAN).
- [ ] **Federated Learning:** Explore federated training as an alternative privacy-preserving approach beyond differential privacy.

---

## 👥 Team

**Ebram Raafat Thabet** | Adham Ali | Omar Saqr | Saif Abd Elfattah
- **Course:** CSCE 4930 — Responsible & Ethical AI, The American University in Cairo
- **Instructor:** Dr. Alia El Bolock
- GitHub: [BeTechBo](https://github.com/BeTechBo)
