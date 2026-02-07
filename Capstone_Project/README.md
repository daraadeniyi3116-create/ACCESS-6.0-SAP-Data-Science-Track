# 🏥 Medical Insurance Cost Prediction Capstone

## 📌 Project Overview
In this capstone project, I analyzed a dataset of 1,338 medical insurance records to understand the factors driving healthcare costs. I built machine learning models to predict individual medical charges and identify high-risk patients.

The goal of this project was to provide data-driven insights that can help insurance companies set fair premiums and implement targeted wellness programs.

## 📂 Dataset Used
* **Source:** Medical Cost Personal Datasets (Insurance.csv)
* **Size:** 1,338 rows, 7 columns
* **Features:**
    * `age`: Age of primary beneficiary
    * `sex`: Insurance contractor gender (female, male)
    * `bmi`: Body mass index
    * `children`: Number of children covered by health insurance
    * `smoker`: Smoking status (yes, no)
    * `region`: The beneficiary's residential area in the US (northeast, southeast, southwest, northwest)
    * `charges`: Individual medical costs billed by health insurance

## 🎯 Problem Statements
1.  **Regression Task:** Can I accurately predict the exact medical cost (`charges`) for a new patient based on their demographic and health data?
2.  **Classification Task:** Can I categorize patients into "High Cost" or "Low Cost" groups to better manage financial risk?

## 🛠️ Models Built
I followed a rigorous machine learning workflow, including **EDA**, **Feature Engineering**, and **Pipeline Construction**.

### 1. Regression Models (Predicting Costs)
* **Baseline:** Linear Regression
* **Advanced:** Random Forest Regressor (Implemented via Scikit-Learn Pipeline)
* **Performance:** The Random Forest model achieved an **R² score of ~87%**, significantly outperforming the linear baseline.

### 2. Classification Models (High vs. Low Risk)
* **Target:** Created a `high_paying` binary target based on the median cost split.
* **Baseline:** Logistic Regression
* **Advanced:** Random Forest Classifier
* **Performance:** The Random Forest Classifier achieved an **Accuracy of ~94%** and a high **ROC-AUC score**.

## 💡 Key Findings
Through Exploratory Data Analysis (EDA) and Feature Importance analysis, I discovered:

1.  **Smoking is the #1 Cost Driver:** Smoking status is the single strongest predictor of medical charges. Smokers pay significantly more than non-smokers across all age groups.
2.  **The "Obesity Trap":** I identified a critical interaction between BMI and smoking. High BMI (Obesity) drastically increases costs *only* for smokers. For non-smokers, obesity has a much smaller financial impact.
3.  **Age Progression:** Medical costs increase linearly with age, but the slope is much steeper for smokers.

## 🚀 Technologies Used
* **Python:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Pipelines, RandomForest, Cross-Validation)
