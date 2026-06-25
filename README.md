# Customer_Segmentation_And_Churn_Prediction
# 📊 Telco Customer Churn Prediction

## 📖 Overview
This project is a complete end-to-end machine learning pipeline for predicting customer churn using the **Telco Customer Churn dataset**. It covers:
- Exploratory Data Analysis (EDA)
- Data preprocessing and cleaning
- Model building with Random Forest
- Cross-validation and ROC-AUC evaluation
- Customer segmentation using K-Means clustering

The goal is to identify high-risk customers and provide actionable insights for retention strategies.

---

## 📁 Dataset
- **File:** `Telco_customer_churn.xlsx`
- **Target Variable:** `Churn Value` (1 = Churned, 0 = Retained)
- **Key Features:** Tenure Months, Monthly Charges, Total Charges, Contract Type, Internet Service, Payment Method, Tech Support, etc.

---

## 🔧 Libraries Used
- **Data Handling:** pandas, numpy  
- **Visualization:** matplotlib, seaborn  
- **Machine Learning:** scikit-learn (RandomForestClassifier, KMeans, StandardScaler, train_test_split, metrics)

---

## 🛠️ Workflow

### 1. Exploratory Data Analysis (EDA)
- Distribution of churn labels and class imbalance check  
- Tenure, Monthly Charges, and Contract Type analysis  
- Correlation heatmap and cross-tabulations  
- Visualizations with histograms, boxplots, and countplots  

### 2. Data Cleaning
- Converted `Total Charges` to numeric  
- Filled missing values (customers with 0 tenure → 0 charges)  
- Dropped irrelevant columns (IDs, location info, churn reason, etc.)  

### 3. Encoding
- One-Hot Encoding applied to categorical variables  
- Expanded dataset with binary numeric features  

### 4. Feature Selection
- Extracted feature importance from Random Forest  
- Dropped least important features to improve efficiency  

### 5. Train-Test Split
- 80% training / 20% testing split  
- Random state fixed for reproducibility  

### 6. Random Forest Models
- **Baseline Model**  
- **Balanced Model** (class_weight='balanced')  
- **Tuned Model** (grid search with n_estimators & max_depth)  
- Feature importance analysis  

### 7. Cross-Validation
- 5-Fold CV for accuracy and recall  
- Reliable performance estimation  

### 8. ROC-AUC Evaluation
- Probability-based predictions  
- ROC curve plotted, AUC score computed  

### 9. Customer Segmentation (K-Means)
- Features: Tenure, Monthly Charges, Total Charges, Churn Probability  
- StandardScaler applied  
- Elbow method → Optimal K = 3  
- Segments: Budget Loyal, High Risk, Loyal Premium  

### 10. Data Visualization
- Histograms, boxplots, countplots  
- Elbow curve for clustering  
- Scatter plots for churn probability vs tenure/charges  

---

## 🚀 How to Run
1. Clone or download this repository  
2. Place `Telco_customer_churn.xlsx` in the project directory  
3. Install dependencies:  
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
