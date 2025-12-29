# 🔧 Predictive Maintenance Model for a Delivery Company (Classification)

This project focuses on building a **predictive maintenance classification model** for a delivery company to estimate the **risk of equipment failure**.  
The goal is to identify maintenance needs in advance, reduce unexpected breakdowns, and improve operational efficiency.

---

## 🎯 Project Objective

- Predict whether a piece of equipment is at **risk of failure**
- Handle **imbalanced data** effectively
- Compare multiple classification models
- Select the best-performing model using **ROC-AUC**
- Save the final model for future deployment

---

## 📂 Problem Description

Equipment failures can cause delays, increased costs, and customer dissatisfaction in delivery operations.  
This project applies **machine learning classification techniques** to predict failure risk based on historical equipment data.

The target variable is a **binary class**:
- `0` → No failure  
- `1` → Failure  

---

## ⚖️ Handling Imbalanced Data

The dataset was **imbalanced**, with fewer failure cases compared to non-failure cases.  
To address this issue, **SMOTE (Synthetic Minority Over-sampling Technique)** was applied.

### Why SMOTE?
- Generates synthetic samples for the minority class
- Prevents models from being biased toward the majority class
- Improves recall and overall predictive performance

---

## ⚙️ Modeling Approach

Multiple classification algorithms were evaluated to identify the most effective model.

### Models Tested
- Bernoulli Naive Bayes  
- Gaussian Naive Bayes  
- Random Forest Classifier  
- Gradient Boosting Classifier  
- K-Nearest Neighbors (KNN)

---

## 🔁 Model Evaluation Strategy

- **Cross-validation:**  
  - Repeated Stratified K-Fold  
  - 10 folds, 3 repeats  
  - Preserves class distribution
- **Evaluation Metric:**  
  - ROC-AUC (Area Under the ROC Curve)

---

## 📊 Model Performance

| Model | Mean ROC-AUC |
|-----|-------------|
| Bernoulli Naive Bayes | 0.745 |
| Gaussian Naive Bayes | 0.822 |
| **Random Forest Classifier** | **0.944** |
| Gradient Boosting Classifier | 0.934 |
| K-Nearest Neighbors | 0.936 |

---

## 🏆 Best Model

- **Model:** Random Forest Classifier  
- **Mean ROC-AUC:** **0.944**

### Why Random Forest?
- Strong performance on tabular data
- Handles non-linear relationships well
- Robust to noise and feature interactions
- Outperformed all other tested models

---

## 💾 Model Persistence

The final Random Forest model was trained on the full balanced dataset and saved using **pickle**, enabling reuse in production or future inference pipelines.

---

## 📈 Business Impact

This predictive maintenance model can help a delivery company to:

- Detect high-risk equipment before failure occurs  
- Reduce unexpected downtime and repair costs  
- Optimize maintenance scheduling  
- Improve operational reliability  
- Support data-driven maintenance decisions  

---

## 🛠️ Technologies Used

- Python  
- Pandas, NumPy  
- Scikit-learn  
- imbalanced-learn (SMOTE)  
- Pickle  

---

## 🧾 Conclusion

- Imbalanced data was successfully handled using SMOTE  
- Tree-based ensemble methods significantly outperformed simpler models  
- Random Forest achieved the highest predictive performance  
- The project demonstrates an end-to-end **predictive maintenance pipeline**, from data balancing to model deployment  

---
