# TEAM-LAMBDA
## Foundation Of Machine Learning / Group-Project

## REPORT

##**Tax Liability Prediction & Migration-Based Tax Change Classification**

## **Overview**
The project focuses on two machine learning tasks built o the US tax return and migration data:

1. **Regression — Tax Liability Prediction**
   predicting tax liability using the financial indiactors such as AGI, deductions,dependent,exemptions, taxable income , and number of returns
   
2. **Clustering + Classification — Migration Tax Change**
   Identifies migration-based patterns and predicts whether tax liability **increases or decreases** after migration.
  
   goal is to provide data-driven insights for tax planning, income analysis, and understandind miagration impacts

##  **Problem Statement**

### **1️;'
 Regression: Tax Liability Prediction**

The objective is to build a regression model that predicts **total tax liability** for a given region based on key financial indicators such as:

* Adjusted Gross Income (AGI)
* Deductions
* Dependent exemptions
* Taxable income
* Tax before credits
* Number of returns

This model helps estimate tax burden across income groups and locations, supporting fiscal analysis and planning.


### **2️ Clustering + Classification: Migration – Tax Change**

This part of the project examines how migration impacts tax liability.

Using this, a binary target label is derived:
* **1 → Tax increased after migration**
* **0 → Tax decreased after migration**

Clustering (K-Means) is used to group migration patterns before performing classification.

### **Dataset Description**

Include the dataset details here:

* Source of data **https://catalog.data.gov/dataset/income-tax-components-by-size-of-income-by-place-of-residence-beginning-tax-year-1999**
* Number of rows :24,000
* feature inthe dataset:
    1. **Tax Year** :The tax filing year for which the income, deductions, and tax liability data is reported.

    2. **Resident Type**:Indicates whether the filer is:
         **Resident**
         **Nonresident**
         **Part-year resident**
         Shows the type of taxpayer based on where they lived in that tax year.
    3. **Place Of Residence**:The location (usually state/county) where the taxpayer lived when filing the return.

    4. **Country**:The country of residence of the taxpayers (generally “United States” for this dataset)
    
    5. **State**:The U.S. state where the taxpayer resided when filing the return
    
    6. **County**:The county within the state where the taxpayer resides
    
    7. **Income cost**:Categorized income bucket (e.g., $0–$25k, $25k–$50k, etc.).
                       Used to group taxpayers based on their income range.
    8. **Discloser**:Indicates whether the value has been suppressed or adjusted for privacy/IRS rules.
                      “0” or blank → Data is fully reported.
                      “1” → Some suppression has been applied
    9. **Number of returns**:Total number of tax returns filed by residents in that county/state/income class.
    
    10. **NY AGI of All Returns (in thousands)**:Total New York Adjusted Gross Income for all returns, aggregated and expressed in $1,000s.
                                                (AGI = gross income minus specific deductions)
    11. **Deductions of All Returns (in thousands)**:Total deductions claimed by all taxpayers combined, expressed in *$1,000s*Includes either standard or itemized deductions.
    
    12. **Dependent Exemptions of All Returns (in thousands)**:Total dollar amount of dependent exemptions claimed by all tax returns, in   thousands.Represents     deductions for each dependent
    
    13. **Taxable Income of All Returns (in thousands)** :Sum of taxable income reported across all returns after deductions, in thousands.
    
    14. **Tax Before Credits of All Returns (in thousands)**:Total tax owed before applying credits such as child tax credit, education credit, earned income credit
    
    15. **Tax Liability of All Returns (in thousands)**:Final tax owed by all tax returns after applying credits.This is the main target variable for tax prediction ML tasks
    
    16. **Place of Residence Sort Order**:A numeric code used for sorting states/counties in reports.
    
    17. **Income Class Sort Order**:A numeric code representing the ranking of income classes (e.g., 1 = lowest, 10 = highest). Useful for ordering or modeling income   as an ordinal variable.

* Regression target → tax liability
* Classification target → tax change (increase/decrease)

### **Exploratory Data Analysis (EDA)**

Key visualizations and insights:

* Distribution plots of AGI, deductions, taxable income
* Correlation heatmap of financial indicators
* Boxplots to detect outliers
### **Regression Metrics**
* RMSE
* R² Score

### **Classification Metrics**
* Accuracy
* Precision / Recall / F1-Score
* Confusion Matrix
* ROC-AUC Curve

### **Requirements**

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib / Seaborn
* XGBoost


###  **Contributors**
   1. Het Katrodiya
   2. Gaurang jadhav
   3. Aksh Patel
   4. Vrushil Panwala
