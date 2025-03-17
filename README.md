# Credit Card Fraud Detection Project Report

## 1. Introduction

This report details a project focused on detecting fraudulent credit card transactions using a dataset of credit card transactions. The project utilized Python, Pandas, Matplotlib, and Scikit-learn for data preprocessing, exploratory data analysis (EDA), and feature scaling. The primary goal was to analyze the dataset, understand the distribution of fraudulent and genuine transactions, and prepare the data for future predictive modeling.

## 2. Objectives

The primary objectives were:

* To load and inspect the credit card transaction dataset.
* To perform exploratory data analysis to understand the distribution of fraudulent and genuine transactions.
* To preprocess the data, including handling missing values and scaling numerical features.
* To visualize the distribution of transaction classes.

## 3. Methodology

The project followed these steps:

1.  **Data Loading and Initial Inspection:**
    * Imported necessary Python libraries: Pandas, NumPy, and Matplotlib.
    * Loaded the "creditcard.csv" dataset into a Pandas DataFrame.
    * Displayed the first few rows of the DataFrame to understand the data's structure.
    * Checked for missing values using `isna().any().sum()`.
    * Handled missing values by dropping rows with `dropna()`.
    * Used `describe()` to get the statistical description of the "Amount" column.
2.  **Exploratory Data Analysis (EDA):**
    * Calculated the number and percentage of genuine and fraudulent transactions.
    * Visualized the distribution of transaction classes using a bar plot.
3.  **Data Preprocessing:**
    * Scaled the "Amount" column using `StandardScaler` from Scikit-learn to normalize the data.
    * Removed the original "Amount" and "Time" columns.
    * Separated the target variable ("Class") from the features.

## 4. Dataset Description

The "creditcard.csv" dataset contains the following columns:

* **Time:** Time elapsed in seconds between each transaction and the first transaction in the dataset.
* **V1-V28:** Anonymized features obtained through PCA transformation.
* **Amount:** Transaction amount.
* **Class:** Target variable, where 1 represents fraudulent transactions and 0 represents genuine transactions.

## 5. Results and Observations

* The dataset contained a large number of anonymized features (V1-V28) and two original features: "Time" and "Amount."
* The dataset had 19 missing values, which were handled by dropping the rows.
* The "Amount" column had a wide range of values.
* The dataset was highly imbalanced, with a significantly larger number of genuine transactions compared to fraudulent transactions.
* The percentage of fraud transactions was 0.4201%.
* The transaction Class was visualized using a bar chart showing the severe imbalance.
* The amount column was normalized using the standard scaler.

## 6. Conclusion

This project successfully loaded, cleaned, and explored the credit card transaction dataset. The EDA revealed the imbalanced nature of the dataset, which is crucial for subsequent modeling. The data was preprocessed by scaling the "Amount" column and removing unnecessary columns, preparing it for further analysis and predictive modeling.

## 7. Future Work

Future work on this project could include:

* Addressing the class imbalance using techniques like oversampling or undersampling.
* Training machine learning models to predict fraudulent transactions.
* Evaluating the performance of the models using appropriate metrics (e.g., precision, recall, F1-score, AUC).
* Trying different scalers, and comparing results.
* Using dimension reduction techniques to reduce the number of V variables.
* Using different classification models.
