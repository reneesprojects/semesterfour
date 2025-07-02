🧩 *Semester 4 bridges practical web development and analytical thinking. From MongoDB-backed apps to market basket analysis, this semester sharpens both coding and data intuition. One builds full-stack web apps, while the other explores patterns in real-world data.*

# Module: Data Mining 📊

# Data Mining Project – Feature Selection & Classification Project 

This project explores how different **feature selection techniques** affect the performance of classification models. Using real-world health-related datasets, we applied the **k-Nearest Neighbors (k-NN)** algorithm and measured how different subsets of features influence prediction accuracy.

# Project Overview

The goal was to:
📈
* Identify which features are most relevant for predicting outcomes
* Apply statistical methods to reduce dimensionality
* Train and test models using **k-NN** and compare performance

Two main datasets were used:

1. **Breast Cancer Diagnosis Dataset** 
2. **Sleep Trouble Health Dataset** 


# Methods Applied

# 1. Baseline k-NN Model (All Features)

* Dataset: Breast cancer data
* Preprocessing: Removed `Patient ID`, encoded `Diagnosis` (M = 1, B = 0), standardized features
* Model: **k-NN with k=5**, trained on all 30 features
* Output: Baseline accuracy
  
*Purpose: Set a reference point for performance with all available data.*

# 2. T-Test Feature Selection

* Statistical method: Independent **t-tests** between benign and malignant samples
* Selected top 10 features with lowest p-values
* Compared accuracy of:

  * All features
  * Top 10 statistically significant features
    
  * Purpose: Use hypothesis testing to isolate features with meaningful differences.*

# 3. Mutual Information Feature Selection

* Calculated **mutual information scores** between each feature and the target label
* Selected top 10 most informative features
* Trained and evaluated:

  * Full-feature k-NN model
  * Reduced-feature k-NN model
    
  *Purpose: Capture non-linear relationships between features and outcomes.*

# 4. Chi-Square Feature Selection (Sleep Trouble Dataset)

* Preprocessing: Label-encoded categorical data
* Applied **Chi-square tests** to find features strongly associated with sleep trouble
* Selected top 10 features for model training
* Evaluated accuracy using **k-NN classifier**
  
*Purpose: Apply categorical feature selection to a different health dataset.*


# Techniques Summary

* **Classification Algorithm**: k-Nearest Neighbors (k-NN)
* **Preprocessing**: StandardScaler, Label Encoding
* **Feature Selection Methods**:
  * Independent T-Test
  * Mutual Information
  * Chi-Square Test

# 💡 Key Outcomes

* Feature selection can **improve model performance** while reducing complexity
* Different methods highlight **different types of relationships** (linear, categorical, non-linear)
* Statistical reasoning supports better data-driven decisions

# 2. Data-Mining Practical Report 🧪

This project focused on identifying **key predictors of survival in cirrhosis patients** through a combination of **data imputation, visualization**, and **feature selection using machine learning and statistics**.

The dataset contained missing values and clinical data for liver patients, with the target outcome being patient survival (alive or deceased). The analysis was broken down into several key phases:

# Dataset Used: `CIRRHOSIS.xlsx`

* Medical dataset with lab results, diagnosis stages, and survival labels
* Required handling of missing values and variable distributions
* Objective: Find the most significant features that influence patient survival

# Phase 1: Missing Data Visualization & Imputation

**Files:**

* Graph Analysis of Missing Values.py

* all data imputed.py

* Used **Seaborn** and **Matplotlib** to visualize missing patterns across lab results (e.g., *Cholesterol*, *Copper*, *Triglycerides*, *Platelets*)

* Performed:

  * **Median imputation** for right-skewed variables
  * **Mean imputation** for normally distributed variables

* Saved final cleaned dataset as `all_data_imputed.xlsx`
*Purpose: Clean the dataset without skewing distributions too heavily*


# Phase 2: Feature Correlation & Class Separation

**File:**: Question 6.py

* Focused on 4 clinical lab features: *Albumin*, *Prothrombin*, *Alkaline Phosphatase*, *Bilirubin*
* Visualized distributions using:

  * **Histograms and Boxplots** by histological stage
  * **Scatter plots** to check class separation
  * **Correlation heatmaps** to understand interrelationships
  *Purpose: Understand how different stages relate to lab readings, and identify possible predictors visually*


# Phase 3: Survival Prediction & Feature Elimination

**File:**: Question 7.py

* Loaded a preprocessed dataset (`cirrhosis_cleaned_for_feat_select.xlsx`)
* Used **t-tests** to rank features by significance
* Performed **Backward Feature Elimination** using:

  * **Random Forest Classifier**
  * **Leave-One-Out Cross Validation (LOOCV)**
    
* Iteratively removed features with the highest p-values
* Tracked how model accuracy changed as fewer features were used
*Purpose: Pinpoint the smallest set of features with the highest predictive power*

# Techniques Used

* **Data Imputation**: Median/Mean strategies
* **Visualization Tools**: Seaborn, Matplotlib
* **Statistical Tests**: T-Test
* **Modeling**: Random Forest, LOOCV
* **Feature Selection**: Backward elimination based on significance and accuracy

# 💡 Key Takeaways

* Missing data doesn’t always require deletion — thoughtful imputation maintains data integrity
* Visuals help explain complex medical data to both technical and non-technical audiences
* Machine learning and statistics can work together to find **minimal yet powerful predictors**

