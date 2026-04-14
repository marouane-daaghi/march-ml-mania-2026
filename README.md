# 🏀 March Machine Learning Mania 2026

![Kaggle](https://img.shields.io/badge/Kaggle-Top%2020%25-blue?logo=kaggle)
![Python](https://img.shields.io/badge/Python-3.x-green?logo=python)
![Sklearn](https://img.shields.io/badge/Scikit--Learn-Ensemble-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

> 🥇 **Top 20% Worldwide** out of all competition submissions on Kaggle.

---

## 📌 Overview

This project is my solution to the **[March Machine Learning Mania 2026](https://www.kaggle.com/competitions/march-machine-learning-mania-2026)** Kaggle competition, which challenges participants to predict the outcomes of the NCAA Basketball Tournament using historical game data.

The goal is to predict the **probability** that one team beats another across all possible matchups — evaluated using **Brier Score**.

---

## 🏆 Results

| Metric | Score |
|--------|-------|
| **Brier Score** | **0.1991** |
| **Global Ranking** | **Top 20%** |
| **Evaluation** | Stage 2 (Real tournament results) |

---

## 🧠 Approach

### Strategy: Voting Ensemble of 10 Classifiers

Rather than relying on a single model, I built a **soft-voting ensemble** that averages predicted probabilities across 10 diverse classifiers — reducing variance and improving generalization.

### Models Used

| Model | Library |
|-------|---------|
| Logistic Regression | scikit-learn |
| Random Forest | scikit-learn |
| Extra Trees | scikit-learn |
| Gradient Boosting | scikit-learn |
| K-Nearest Neighbors | scikit-learn |
| Gaussian Naive Bayes | scikit-learn |
| Support Vector Classifier | scikit-learn |
| XGBoost | xgboost |
| LightGBM | lightgbm |
| CatBoost | catboost |

### Validation Strategy
- **K-Fold Cross Validation** to ensure robust evaluation
- **Brier Score Loss** as the primary optimization metric
- Memory management with `gc.collect()` after each model

---

## 📊 Exploratory Data Analysis

Key insight from EDA:

- **Mean score difference** between winning and losing teams: **12.10 points**
- **Median score difference**: **10.00 points**
- Score differences follow a **right-skewed distribution**, indicating most games are relatively close

---

## 🔮 Tournament Simulation

Beyond predicting individual matchups, I built a **Monte Carlo tournament simulator** that:
1. Simulates the full NCAA bracket thousands of times
2. Estimates each team's championship probability

**Top predicted championship contenders:**

| Rank | Team | Win Probability |
|------|------|----------------|
| 1 | Team 1181 | 12.7% |
| 2 | Team 1242 | 9.0% |
| 3 | Team 1314 | 6.6% |
| 4 | Team 1246 | 6.2% |
| 5 | Team 1163 | 6.0% |

---

## 🗂️ Project Structure

```
march-ml-mania-2026/
│
├── notebook.ipynb          # Main Kaggle notebook
├── README.md               # This file
└── .gitignore
```

---

## 📦 Data

The dataset is publicly available on Kaggle:

🔗 [March Machine Learning Mania 2026 - Dataset](https://www.kaggle.com/competitions/march-machine-learning-mania-2026/data)

To use this project locally:
1. Download the data from the link above
2. Place the CSV files in the project folder
3. Run the notebook

## ⚙️ Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm catboost
```

---

## 👤 Author

**Marouane Daaghi**
- 📍 Marrakech, Morocco
- 🔗 [GitHub](https://github.com/marouane-daaghi)
- 🏅 Data Scientist | ML Practitioner | Kaggle Competitor

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
