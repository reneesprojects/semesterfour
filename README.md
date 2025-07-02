🧩 *Semester 4 bridges practical web development and analytical thinking. From MongoDB-backed apps to market basket analysis, this semester sharpens both coding and data intuition. One builds full-stack web apps, while the other explores patterns in real-world data.*

# 🌐 Web Systems Development

**Languages & Tools:** HTML, CSS, JavaScript, Node.js, Express.js, MongoDB


###  Project 1: Clinic Reception System (Front-End Only) 🖥️

This project simulates a **clinic reception system**, supporting front-desk operations such as patient registration, appointment scheduling, queue management, billing, and record keeping. Developed fully using **HTML, CSS, and JavaScript**, it follows a modular structure where each core function lives in its own page.

A calendar-style dashboard serves as the main navigation hub, allowing smooth access across modules.

#### Objectives:

* Design a clinic system interface without backend integration
* Practice modular front-end development
* Simulate real-world clinic workflows with basic validation, dynamic forms, and navigation

#### Features:

* **Login Page**: Entry form to restrict access to staff users
* **Dashboard**: Month-view page to view appointment dates and time
* **Patient Registration**: Capture and display patient data in editable tables
* **Appointment Booking**: Create and manage doctor appointments
* **Queue System**: Add, call, and remove patients from a live waiting list
* **Invoice Generator**: Build and edit invoices for consultations
* **Medical Records**: Record patient health history and visit notes

#### Techniques Used:

* Vanilla JavaScript for DOM manipulation
* Form validation and basic interactivity
* Modals and tables to simulate data views
* Responsive CSS layout across all modules

### 💡 Takeaways:

* Modular front-end systems can simulate full workflows even without a backend
* Real-world use cases enhance learning — from billing to patient queues
* Structure and reusability matter when handling multi-page UI systems


### Project 2: Clinic Reception System v2 (MongoDB + Express) 2️⃣ 

*Just like version 1... but better, using MongoDB!*

This upgraded version connects the same system to a **MongoDB database**, allowing real-time storage and retrieval of records and appointment data. It brings full-stack capability using **Node.js**, **Express.js**, and **Mongoose ORM**.

#### Improvements:

* **Persistent data storage** via MongoDB
* **Real-time updates** to patient and appointment records
* **Backend logic** with Express routing
* **Improved file structure** and better code organization

📌 *Purpose: Bring the system closer to real-world healthcare software with full-stack capabilities.*


# Data Mining 📊

### Data Mining Project 📈 

This project explores how different **feature selection techniques** impact the performance of classification models. Using real-world health datasets, it applies the **k-Nearest Neighbors (k-NN)** algorithm to examine how reducing features can improve (or hurt) model accuracy.

#### Objectives:

* Identify the most predictive features in health datasets
* Reduce dimensionality without losing accuracy
* Compare model performance before and after selection

#### Datasets Used:

1. **Breast Cancer Diagnosis**
2. **Sleep Trouble Survey**

#### Techniques Applied:

**1. Baseline Model**

* Trained k-NN on all features (k=5)
* Preprocessing: Label encoding, standardization
  
📌 *To establish a reference accuracy.*

**2. T-Test Feature Selection**

* Ran t-tests between benign and malignant cases
* Selected top 10 lowest p-value features
  
📌 *To isolate statistically different variables.*

**3. Mutual Information**

* Ranked features by information gain
* Focused on non-linear dependencies
  
📌 *To measure relevance beyond linear correlation.*

**4. Chi-Square (Sleep Dataset)**

* Applied chi-square test to categorical data
* Selected top features influencing sleep trouble
  
📌 *To apply categorical feature selection.*

#### 🔧 Summary of Tools:

* **Classifier**: k-NN
* **Feature Selectors**: T-Test, Mutual Info, Chi-Square
* **Libraries**: Pandas, Sklearn, Seaborn

#### 💡 Key Insights:

* Feature selection reduces overfitting and improves interpretability
* Different methods reveal different feature types — linear, categorical, or non-linear
* k-NN is sensitive to irrelevant features; selecting the right ones makes a big difference


### 🧪 Practical Report

This report focuses on predicting survival in patients with cirrhosis by applying **data cleaning**, **statistical analysis**, and **machine learning-based feature selection**.

#### Dataset: CIRRHOSIS.xlsx

Clinical data with missing values and outcome labels (Alive/Deceased).

#### Workflow Breakdown:

**Phase 1: Missing Data Analysis**

*Files: Graph Analysis of Missing Values.py, all data imputed.py*

* Visualized missingness using Seaborn
* Used **mean/median imputation** depending on distribution
  
📌 *To retain dataset integrity without heavy bias.*

**Phase 2: Feature Exploration**

*File: Question 6.py*

* Focused on Albumin, Prothrombin, ALP, and Bilirubin
* Visualized group distributions by stage
* Used correlation heatmaps and scatter plots
  
📌 *To understand patterns and class separation visually.*

**Phase 3: Feature Elimination & Prediction**

*File: Question 7.py*

* Used **t-tests** for significance
* Applied **Backward Elimination** with Random Forest
* Used **Leave-One-Out Cross Validation (LOOCV)**
  
📌 *To identify the smallest, most effective set of predictors.*


#### Techniques Summary:

* **Imputation**: Median for skewed, mean for normal
* **Visualization**: Seaborn, Matplotlib
* **Model**: Random Forest + LOOCV
* **Selection**: T-Test, backward removal


### 💡 Takeaways:

* Missing data doesn’t always require deletion — thoughtful imputation preserves value
* Statistical tests + visual analysis = stronger feature understanding
* Small, well-chosen feature sets often outperform large noisy ones
* ML and statistics can work together to support healthcare decision-making
