# CrimeCast: Forecasting Crime Categories

A machine learning project focused on multi-class classification of crime types using **scikit-learn** and data-driven modeling techniques.

---

##  Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Features](#features)
- [Modeling Approach](#modeling-approach)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)

---

##  Overview
CrimeCast is a predictive analytics project that classifies crime incidents into categories. It demonstrates machine learning workflows from data preprocessing to model evaluation.

---

##  Dataset
- Dataset includes `train.csv`, `test.csv`, and `sample.csv`.
- Available features may include date, time, location, and crime descriptors (based on your actual columns).
- The goal: Predict crime categories given input features.

---

##  Features
- Data cleaning and feature engineering
- Exploratory Data Analysis (EDA)
- Multi-class classification modeling
- Evaluation using metrics like accuracy, precision, recall, and F1-score
- Model comparison for performance tuning

---

##  Modeling Approach
1. **Data Preprocessing**: Cleaning, encoding categorical variables, handling missing values  
2. **Feature Engineering**: Extracting date-time features (like hour, day, month)  
3. **Model Training**: Training algorithms such as Logistic Regression, Random Forest, or SVM  
4. **Evaluation**: Using classification reports and confusion matrices to assess performance  

---

##  Tech Stack
- **Languages**: Python  
- **Libraries**: scikit-learn, pandas, numpy, matplotlib / seaborn (for EDA)  
- **Notebooks**: Jupyter for interactive development and analysis  

---

##  Project Structure
```
CrimeCast/
│
├── train.csv
├── test.csv
├── sample.csv
├── .ipynb               # Main Jupyter notebook for EDA and modeling
└── README.md
```

---

##  Installation
1. Clone the repo:
   ```bash
   git clone https://github.com/LeviTheScout/CrimeCast-Forecasting-Crime-Categories-.git
   cd CrimeCast-Forecasting-Crime-Categories-
   ```
2. Create a Python virtual environment:
   ```bash
   python3 -m venv env
   source env/bin/activate     # Windows: env\\Scripts\\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

##  Usage
- Launch the Jupyter notebook:
  ```bash
  jupyter notebook
  ```
- Open the main notebook to walk through:
  - Data loading and EDA  
  - Feature engineering  
  - Model training, testing, and evaluation  
  - Insights and visualizations

---


## 📊 Results


The performance of various models on the crime classification task is summarized below:

| Model                | Accuracy (%) |
|----------------------|--------------|
| Dummy Model          | 58.0         |
| KNN Classifier       | 91.0         |
| SVM                  | 94.9         |
| Logistic Regression  | 94.5         |
| LGBM Classifier      | 95.4         |
| XGB Classifier       | **95.8**     |
| Voting Classifier    | 95.7         |


<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/1e7eb007-d765-480f-adf9-330a6b562aab" />

**Key Observations:**
- Baseline (Dummy) model achieved **58%** accuracy.
- Non-Ensemble models (Logistic Regression, SVM) performed well (~94–95%).
- Ensemble models (LGBM, XGBoost, Voting) outperformed others, with **XGBoost Classifier** reaching the highest accuracy of **95.8%**.
- Class imbalance was present; SMOTE was tested but did not improve the top result.

**Final Best Model:** XGBoost Classifier — 95.8% Accuracy
