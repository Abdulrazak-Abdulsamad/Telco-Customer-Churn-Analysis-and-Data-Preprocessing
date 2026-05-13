# Telco-Customer-Churn-Analysis-and-Data-Preprocessing

## Project Overview

This project focuses on analyzing customer churn behavior in a telecommunications company using Python for data analysis, preprocessing, and visualization. The main objective of the project is to explore customer data, identify patterns related to churn, clean and transform the dataset, and prepare the data for future machine learning modeling.

Customer churn is one of the most important business problems in the telecommunications industry because retaining existing customers is usually more cost-effective than acquiring new ones. By analyzing customer demographics, subscription behavior, billing information, and service usage, this project aims to uncover factors that may influence customer retention and customer loss.

The project demonstrates essential data science workflows including:

* Data loading and inspection
* Data cleaning and preprocessing
* Missing value handling
* Duplicate detection
* Exploratory Data Analysis (EDA)
* Correlation analysis
* Distribution analysis
* Feature transformation
* Data visualization
* Preparation for predictive modeling

This project is beginner-friendly and serves as a strong foundation for understanding real-world customer analytics problems.

---

# Objectives

The major objectives of this project are:

1. Explore and understand the structure of the Telco Customer Churn dataset.
2. Clean and preprocess the dataset for analysis.
3. Detect and handle missing values and duplicates.
4. Analyze relationships between numerical features.
5. Identify skewed distributions and apply transformations.
6. Visualize customer-related patterns using charts and graphs.
7. Prepare the dataset for future machine learning classification models.

---

# Dataset Information

The dataset used in this project contains customer information from a telecommunications company. It includes customer demographic details, subscription information, billing history, and service usage behavior.

### Key Features in the Dataset

* **SeniorCitizen** – Indicates whether a customer is a senior citizen.
* **tenure** – Number of months the customer has stayed with the company.
* **MonthlyCharges** – Monthly subscription charges.
* **TotalCharges** – Total amount charged to the customer.
* **Churn** – Indicates whether the customer left the company.

The dataset provides valuable insights into customer behavior and allows the analysis of factors that may contribute to customer churn.

---

# Technologies and Libraries Used

This project was implemented using Python and several popular data science libraries:

* **Python**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical computations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Scikit-learn** – Machine learning utilities and evaluation metrics

---

# Project Workflow

## 1. Data Loading

The dataset was imported into a Pandas DataFrame for analysis.

```python
import pandas as pd

df = pd.read_csv(file_path)
```

---

## 2. Data Exploration

Initial exploration was performed to understand the structure, dimensions, column names, and statistical summary of the dataset.

The following operations were carried out:

* Viewing dataset shape
* Inspecting column names
* Generating descriptive statistics
* Checking data types
* Reviewing dataset information

This step helped identify potential issues such as missing values and incorrect data types.

---

## 3. Data Cleaning

Several preprocessing tasks were performed to improve data quality.

### Converting Data Types

The `TotalCharges` column was converted into a numeric format using:

```python
df['TotalCharges'] = pd.to_numeric(df['TotalCharges'], errors='coerce')
```

### Handling Missing Values

Missing values in the dataset were detected and replaced using the mean value of the `TotalCharges` column.

```python
df = df.fillna(np.mean(df['TotalCharges']))
```

### Duplicate Detection

The dataset was checked for duplicate records to ensure data consistency.

---

# Exploratory Data Analysis (EDA)

Exploratory Data Analysis was performed to uncover trends, relationships, and patterns within the dataset.

## Correlation Analysis

A correlation matrix and heatmap were created to analyze relationships between numerical variables such as:

* SeniorCitizen
* tenure
* MonthlyCharges
* TotalCharges

The heatmap helps visualize how strongly variables are related to one another.

```python
sns.heatmap(corr_matrix, annot=True)
```

---

## Distribution Analysis

Distribution plots and boxplots were used to understand the spread of data and detect outliers.

### Boxplots

Boxplots were generated for numerical features to identify:

* Outliers
* Skewness
* Data spread

### Histograms

Histograms were used to visualize feature distributions before and after transformation.

---

# Feature Transformation

The `TotalCharges` feature showed positive skewness, meaning the data distribution was not symmetrical.

To improve the distribution, a transformation was applied to reduce skewness and make the feature more suitable for machine learning algorithms.

The project compares:

* Distribution before transformation
* Distribution after transformation
* Skewness reduction results

This preprocessing step improves model performance and data interpretability.

---

# Key Insights

Some important insights discovered during the analysis include:

* Customers with longer tenure generally accumulate higher total charges.
* Monthly charges influence the overall total charges significantly.
* Numerical features exhibit varying levels of correlation.
* Certain features contain skewed distributions that benefit from transformation.
* Data preprocessing is essential before building predictive models.

---

# Machine Learning Preparation

Although the primary focus of this notebook is preprocessing and EDA, the project also imports machine learning utilities such as:

* Logistic Regression
* Train-Test Split
* Accuracy Metrics
* Regression Evaluation Metrics

This indicates that the dataset is being prepared for future predictive churn modeling.

Potential future improvements include:

* Building churn prediction models
* Feature engineering
* Encoding categorical variables
* Model optimization
* Hyperparameter tuning
* Model evaluation and comparison

---

# Skills Demonstrated

This project demonstrates several important data science skills:

* Data cleaning
* Data preprocessing
* Exploratory data analysis
* Statistical analysis
* Data visualization
* Handling missing values
* Feature transformation
* Correlation analysis
* Python programming
* Use of machine learning libraries

---

# Conclusion

This project provides a practical introduction to customer churn analysis using Python. By performing data cleaning, exploratory analysis, and feature transformation, the project builds a strong foundation for predictive analytics and machine learning.

The workflow demonstrates how raw customer data can be transformed into meaningful insights that help businesses understand customer behavior and improve retention strategies.

This project is especially useful for beginners in data science who want hands-on experience with real-world datasets, preprocessing techniques, and visualization methods.

---

# Future Enhancements

Possible future improvements for this project include:

* Building classification models for churn prediction
* Applying feature engineering techniques
* Performing advanced statistical analysis
* Comparing multiple machine learning algorithms
* Deploying the model as a web application
* Creating interactive dashboards using Power BI or Tableau

---

# Author

Developed as part of a Data Science learning and practical analytics project focused on customer churn analysis and predictive modeling.


