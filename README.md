---

# Titanic Dataset Analysis

## Introduction
The Titanic dataset is one of the most popular datasets used for understanding machine learning concepts, particularly classification problems. The dataset contains information about the passengers aboard the RMS Titanic, which sank in 1912 after colliding with an iceberg. The dataset includes details such as passenger class, age, gender, number of siblings/spouses aboard, number of parents/children aboard, fare, port of embarkation, and whether the passenger survived or not.

This project focuses on performing **Exploratory Data Analysis (EDA)** to understand the relationships between various features and the target variable (**Survived**). The goal is to identify key factors that influenced survival and prepare the data for predictive modeling using machine learning algorithms.

---

## Objective
The primary objective of this project is to:
- Perform **Exploratory Data Analysis (EDA)** to understand the dataset and identify patterns.
- Analyze the correlation between different features and the target variable (**Survived**).
- Prepare the data for machine learning by handling missing values, encoding categorical variables, and dropping irrelevant features.
- Identify the most important features that influence survival.
- Build predictive models to classify whether a passenger survived or not.

---

## Steps Conducted in the Project

### 1. **Data Loading and Initial Exploration**
   - The dataset was loaded using **Pandas**.
   - Initial exploration was performed to understand the structure of the dataset, including the number of rows, columns, and data types.
   - Missing values were identified and handled:
     - **Age**: Missing values (19.87%) were dropped.
     - **Cabin**: Missing values (77.10%) were imputed using the mode.
     - **Embarked**: Missing values (0.22%) were imputed using the mode.

### 2. **Data Cleaning and Preparation**
   - The **Age** column was converted from `float64` to `int64` since age is typically represented as an integer.
   - **Age** was binned into categories (0-20, 21-40, 41-60, 61-80) for better analysis.
   - Irrelevant columns (**Fare**, **Ticket**, **PassengerId**, **Cabin**, **Name**) were dropped as they were not useful for prediction.
   - Categorical variables (**Sex** and **Embarked**) were converted to ordinal variables:
     - **Sex**: Male = 0, Female = 1.
     - **Embarked**: Cherbourg = 0, Queensland = 1, Southampton = 2.

### 3. **Exploratory Data Analysis (EDA)**
   - **Bivariate Analysis** was performed to understand the relationship between different features and the target variable (**Survived**):
     - **Pclass vs Survived**: 1st class passengers had the highest survival rate, while 3rd class passengers had the lowest.
     - **Sex vs Survived**: Females had a significantly higher survival rate compared to males.
     - **Age vs Survived**: Passengers aged 21-40 had the highest death count, while those aged 61-80 had the lowest.
     - **SibSp vs Survived**: Passengers with 1 sibling/spouse had a higher survival rate.
     - **Parch vs Survived**: Passengers with 1-3 parents/children had higher survival rates.
     - **Embarked vs Survived**: Passengers from Cherbourg had higher survival rates compared to those from Southampton and Queensland.
   - A **correlation matrix** was created to visualize the correlation between all variables and the target variable.

### 4. **Feature Importance**
   - A **Chi-Square Test** was performed to identify the most important features:
     - **Sex**, **Pclass**, **Parch**, and **Embarked** were identified as the most significant features.
   - **Sex** had the highest Chi-Square score, indicating it was the most important predictor of survival.

### 5. **Data Preparation for Machine Learning**
   - The dataset was split into features (**X**) and target (**y**).
   - Categorical variables were encoded, and irrelevant features were dropped.
   - The dataset was now ready for machine learning model building.

---

## Key Insights from EDA
- **Sex** and **Pclass** were the most important factors influencing survival.
- **Females** and **1st class passengers** had the highest survival rates.
- Passengers aged **21-40** had the highest death count, likely due to the majority being **3rd class males**.
- Passengers from **Cherbourg** had higher survival rates compared to those from **Southampton** and **Queensland**.

---

## Tools and Libraries Used
- **Python**
- **Pandas** (Data Manipulation)
- **NumPy** (Numerical Operations)
- **Matplotlib** and **Seaborn** (Data Visualization)
- **Scikit-learn** (Machine Learning)
