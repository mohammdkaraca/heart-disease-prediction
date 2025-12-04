# Heart Disease Detection & Model Comparison

## 🏥 Project Overview
This project is a comprehensive machine learning analysis designed to predict the presence of heart disease in patients. The goal is to identify the most effective classification algorithm and data preprocessing strategy for accurate medical diagnosis.

We conducted a rigorous "showdown" between five major classification algorithms, evaluating them across different categorical encoding techniques and hyperparameter optimization methods to find the optimal configuration.

---

## 📊 The Dataset
The project utilizes a heart disease dataset (e.g., Cleveland UCI) containing patient health metrics.
* **Target Variable:** `Target` (1 = Heart Disease Present, 0 = Healthy)
* **Key Features:**
    * **Numerical:** Age, Resting Blood Pressure (RestBP), Cholesterol (Chol), Max Heart Rate (MaxHR), ST Depression (Oldpeak).
    * **Categorical:** Chest Pain Type, Thalassemia (Thal), Resting ECG, Slope, Number of Major Vessels (Ca).

---

## 🛠️ Methodology

### 1. Data Preprocessing & Encoding
To handle categorical variables effectively, we implemented and compared three encoding strategies for every algorithm:
* **One-Hot Encoding:** Creates binary columns for each category (Good for nominal data, can increase dimensionality).
* **Label Encoding:** Assigns a unique integer to each category (Simple, but introduces ordinal relationships).
* **Target Encoding:** Replaces a category with the mean of the target variable (Captures relationship with target, prone to overfitting).

### 2. Machine Learning Models
We trained and evaluated five distinct algorithms to cover linear, tree-based, and ensemble approaches:
* **Decision Tree:** A baseline tree model for interpretability.
* **Logistic Regression:** A robust linear baseline for binary classification.
* **Random Forest:** An ensemble of bagging trees to reduce variance.
* **Gradient Boosting:** A powerful boosting ensemble to reduce bias.
* **Support Vector Machine (SVM):** A kernel-based method for finding optimal hyperplanes.

### 3. Hyperparameter Optimization
For every combination of Model + Encoding, we applied two tuning strategies to maximize performance:
* **Grid Search:** An exhaustive search over a manually defined parameter space.
* **Bayesian Optimization (`scikit-optimize`):** A probabilistic approach that "learns" from previous iterations to find optimal parameters more efficiently.

---

## 📂 Repository Structure

project/
│
├── Decision_Tree/
│ ├── data.csv # Dataset used for this algorithm
│ ├── decision_tree_model.ipynb # Jupyter notebook for Decision Tree implementation
│ └── model_pkl_files/ # Serialized model files (.pkl)
│ ├── model_one_hot.pkl
│ ├── model_label_encoded.pkl
│ └── model_target_encoded.pkl
│
├── Logistic_Regression/
│ ├── data.csv
│ ├── logistic_regression_model.ipynb
│ └── model_pkl_files/
│ ├── model_one_hot.pkl
│ ├── model_label_encoded.pkl
│ └── model_target_encoded.pkl
│
├── Random_Forest/
│ ├── data.csv
│ ├── random_forest_model.ipynb
│ └── model_pkl_files/
│ ├── model_one_hot.pkl
│ ├── model_label_encoded.pkl
│ └── model_target_encoded.pkl
│
├── Gradient_Boosting/
│ ├── data.csv
│ ├── gradient_boosting_model.ipynb
│ └── model_pkl_files/
│ ├── model_one_hot.pkl
│ ├── model_label_encoded.pkl
│ └── model_target_encoded.pkl
│
├── SVM/
│ ├── data.csv
│ ├── svm_model.ipynb
│ └── model_pkl_files/
│ ├── model_one_hot.pkl
│ ├── model_label_encoded.pkl
│ └── model_target_encoded.pkl
│
└── final_verdict.ipynb # Final comparison and conclusions notebook

Usage
Navigate to any algorithm folder to explore specific implementations

Open the Jupyter notebook to see the complete workflow

Check final_verdict.ipynb for the comprehensive comparison and conclusions