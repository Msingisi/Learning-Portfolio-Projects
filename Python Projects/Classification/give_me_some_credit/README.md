# 📊 Credit Default Prediction - Model Evaluation and Selection

## 🔍 Project Overview

This project focuses on predicting **credit default** using the **"Give Me Some Credit"** dataset. The goal is to build, evaluate, and compare multiple classification models to accurately predict whether a customer will default on a loan.

## Objectives

- Perform feature engineering and data preprocessing
- Train multiple classification models on the training dataset
- Evaluate model performance using cross-validation and multiple metrics
- Save trained models and evaluation plots
- Select the best-performing model based on test set results

---

## ⚙️ Models Trained

The following classification models were trained on the preprocessed dataset:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Gradient Boosting Classifier
- XGBoost Classifier
- MLP Classifier

After evaluating performance on the **training set**, the top 3 models were selected for testing:

- Random Forest
- XGBoost
- Gradient Boosting

---

## 📈 Evaluation Metrics (Testing Set)

| Model              | Accuracy | F1 Score | ROC AUC | Average Precision (PR AUC) |
|--------------------|----------|----------|---------|-----------------------------|
| **Random Forest**      | 70%      | 0.70     | 0.81    | 0.81                        |
| **XGBoost**            | 68%      | 0.65     | 0.89    | 0.91                        |
| **Gradient Boosting**  | 71%      | 0.69     | 0.86    | 0.87                        |

---

## 📊 Plot Analysis
### RandomForest Evaluation Plots
![confusion_matrix not found]

![roc_curve not found]

![pr_curve not found]

### XGBoost Evaluation Plots
![confusion_matrix not found]

![roc_curve not found]

![pr_curve not found]

### GradientBoosting Evaluation Plots
![confusion_matrix not found]

![roc_curve not found]

![pr_curve not found]


---

## ✅ Final Recommendation

After comparing model performance on **Accuracy**, **F1-Score**, **ROC AUC**, and **PR AUC**, we recommend using:

### 🏆 **XGBoost Classifier** as the final model

Although it has slightly lower accuracy, it offers the **best performance for capturing defaults (Class 1)** — which is often the most critical class in credit risk scenarios.

---

## 📂 Artifacts

- All trained models are saved in the `models/` directory.
- Evaluation plots (Confusion Matrix, ROC, PR Curve) are stored in the `plots/` folder.
- Evaluation metrics are logged in `metrics_test.csv` for test set results and `metrics_train.csv` for training set results.

---

## 📌 Next Steps

- Deploy the selected model using a Flask or FastAPI backend
- Monitor model drift or retrain with updated data periodically
- Enhance explainability using SHAP or LIME for interpretability
