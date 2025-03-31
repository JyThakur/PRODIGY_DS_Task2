# Titanic Dataset Analysis  

## Introduction  
The Titanic dataset is widely used for understanding machine learning classification problems. It contains details of passengers aboard the RMS Titanic, including demographics and ticket information, along with their survival status. This project focuses on **Exploratory Data Analysis (EDA)** to identify key factors influencing survival and prepare the data for predictive modeling.  

## Objective  
- Perform **Exploratory Data Analysis (EDA)** to uncover patterns.  
- Analyze the correlation between different features and survival status.  
- Handle missing values, encode categorical variables, and drop irrelevant features.  
- Identify significant predictors of survival.  
- Prepare the dataset for machine learning modeling.  

## Steps Conducted  

### 1. **Data Loading and Initial Exploration**  
- Loaded the dataset using **Pandas**.  
- Identified missing values:  
  - **Age** (19.87% missing) – dropped missing values.  
  - **Cabin** (77.10% missing) – imputed using the mode.  
  - **Embarked** (0.22% missing) – imputed using the mode.  

### 2. **Data Cleaning and Preparation**  
- Converted **Age** from `float64` to `int64`.  
- Binned **Age** into categories: (0-20, 21-40, 41-60, 61-80).  
- Dropped irrelevant columns: **Fare**, **Ticket**, **PassengerId**, **Cabin**, **Name**.  
- Encoded categorical variables:  
  - **Sex**: Male = 0, Female = 1.  
  - **Embarked**: Cherbourg = 0, Queensland = 1, Southampton = 2.  

### 3. **Exploratory Data Analysis (EDA)**  
- **Bivariate Analysis** revealed key patterns:  
  - **Pclass vs Survived**: 1st class passengers had the highest survival rate.  
  - **Sex vs Survived**: Females had a significantly higher survival rate.  
  - **Age vs Survived**: Passengers aged 21-40 had the highest death count.  
  - **SibSp & Parch vs Survived**: Moderate family sizes had better survival rates.  
  - **Embarked vs Survived**: Cherbourg passengers had higher survival rates.  
- **Correlation Matrix** visualized relationships between features and survival.  

### 4. **Feature Importance**  
- Conducted a **Chi-Square Test** to determine key predictors:  
  - **Sex**, **Pclass**, **Parch**, and **Embarked** were most significant.  
  - **Sex** had the highest importance in predicting survival.  

### 5. **Data Preparation for Machine Learning**  
- Split the dataset into features (**X**) and target (**y**).  
- Encoded categorical variables and removed irrelevant features.  
- The cleaned dataset was ready for model training.  

## Results  
- **Sex** and **Pclass** were the strongest predictors of survival.  
- **Females** and **1st class passengers** had the highest survival rates.  
- The **21-40 age group** had the highest fatalities, likely due to many being **3rd class males**.  
- **Cherbourg passengers** had better survival outcomes than those from Southampton or Queensland.  

## Conclusion  
This analysis confirmed that passenger class, gender, and embarkation point played crucial roles in survival rates. The dataset was successfully cleaned and prepared for predictive modeling.  

---  

Feel free to explore the code, tweak the model, and visualize the results further. Contributions and feedback are welcome!  

**Tools Used:**  
- **Python**  
- **Pandas** (Data Manipulation)  
- **NumPy** (Numerical Operations)  
- **Matplotlib** & **Seaborn** (Data Visualization)  
- **Scikit-learn** (Machine Learning)  

**Author:** [Jay Thakur]
