# Diabetes Prediction Using Machine Learning

## Project Overview
  This project focuses on the development of a predictive model to identify the risk of diabetes in patients based on clinical data. Using medical parameters such as glucose levels, age, cholesterol, and BMI, we implemented and compared several machine learning algorithms to determine the most reliable method for clinical diagnostic support.

  The core of the project involves an end-to-end data science workflow: from rigorous data cleaning and exploratory data analysis (EDA) to hyperparameter tuning. By optimizing a Random Forest classifier, we achieved a high ROC-AUC score of **0.9456**, demonstrating the potential for automated screening tools to assist healthcare professionals in early intervention.

---

## Dataset Description
  The dataset used in this study is the **Diabetes Dataset**, which contains clinical records of **390 patients**.  
It was originally collected to study the prevalence of obesity, diabetes, and other cardiovascular risk factors in central Virginia.

**Source:**  
University of Virginia School of Medicine

---

## Key Features
- **chol**: Total Cholesterol  
- **stab.glu**: Stabilized Glucose  
- **hdl**: High-density Lipoprotein  
- **ratio**: Cholesterol / HDL ratio  
- **glyhb**: Glycosylated Hemoglobin (the target variable)  
- **age**, **gender**, **height**, **weight**, **frame**: Demographic and physical attributes  
- **bp.1s**, **bp.1d**: Blood pressure readings  
- **waist**, **hip**: Body measurements  

---

## Project Architecture & Methodology

### 1. Preprocessing
- Handling missing values using **mean imputation**
- Encoding categorical variables with **One-Hot Encoding**

### 2. Feature Engineering
- Deriving a binary target variable:
  - `glyhb > 6.5` → **Diabetic**
  - `glyhb ≤ 6.5` → **Non-diabetic**

### 3. Model Selection
The following machine learning models were evaluated:
1. Random Forest
2. Logistic Regression
3. Support Vector Machine (SVM)

### 4. Optimization
- Hyperparameter tuning using **GridSearchCV**
- Best Random Forest parameters:
  - `n_estimators = 200`
  - `max_depth = 10`

---

## Model Performance

| Model               | Initial ROC-AUC | Tuned ROC-AUC |
|--------------------|----------------|---------------|
| Random Forest      | 0.9379         | **0.9456**    |
| Logistic Regression| 0.9314         | -             |
| SVM                | 0.9314         | -             |

### 5.2 Discussion
The Random Forest model outperformed the other classifiers, demonstrating superior generalization capability and robustness.

---
## Required Dependencies
To run this project, ensure you have **Python 3.15** and install the following libraries:
- **pandas**  
- **numpy** 
- **matplotlib**
- **seaborn**
- **scikit-learn**

## Reproduction Instructions
Follow these steps to reproduce the results locally:
### 1.	Clone the Repository:
git clone [https://github.com/Youssef-Hadef/diabetes-prediction.git]
### 2.	Install Dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```
# Affiliation:
University Kasdi Merbah - Ouargla (2024/2025)
