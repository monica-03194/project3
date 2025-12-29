# 📘 Training README – Food Classification Using Nutritional Attributes

## Overview

This document describes the **model training and evaluation pipeline** for the Food Classification project.
The objective is to train machine learning models that classify food items into **meal types** (breakfast, lunch, dinner, snack) using nutritional attributes.

---

## Dataset

- **File:** `synthetic_food_dataset_imbalanced.csv`
- **Target Variable:** `Meal_Type`
- **Input Features:**
  - Calories, Protein, Fat, Carbs, Sugar, Fiber
  - Sodium, Cholesterol, Glycemic_Index
  - Water_Content, Serving_Size
  - Preparation_Method, Is_Vegan, Is_Gluten_Free

---

## Training Pipeline

### 1. Data Exploration

- Dataset shape and schema inspection
- Class distribution visualization
- Sample inspection for inter-class variation
- Statistical summaries

### 2. Data Preprocessing

- Missing value imputation:
  - Numerical → Median
  - Categorical → Mode
- Outlier handling using IQR-based capping
- Duplicate removal
- Feature scaling using StandardScaler

### 3. Feature Engineering

- Label encoding of target variable
- One-hot encoding of categorical features
- Dimensionality reduction using PCA (95% variance)
- Feature selection using SelectKBest

### 4. Models Trained

- Logistic Regression
- Decision Tree
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Random Forest
- Gradient Boosting
- XGBoost

### 5. Evaluation Metrics

- Accuracy
- Precision (weighted)
- Recall (weighted)
- F1-score (weighted)
- Confusion matrices

---

## Best Model

**XGBoost** achieved the highest accuracy and balanced performance across all meal categories and was selected as the final model.

---

## How to Run Training

```bash
pip install -r requirements.txt
```

Run notebooks/scripts in the following order:

1. Data Exploration
2. Preprocessing & Feature Engineering
3. Model Training & Evaluation
4. Model Comparison

---

## Output

- Trained model files
- Confusion matrix plots
- Final model comparison table

---

## Conclusion

This training workflow demonstrates a complete machine learning pipeline for food classification using nutritional attributes, highlighting the effectiveness of ensemble learning models for tabular data.
