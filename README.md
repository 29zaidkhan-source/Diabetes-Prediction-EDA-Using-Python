# 🩺 Diabetes Prediction — Exploratory Data Analysis Using Python

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on a Diabetes Prediction dataset using Python.

The analysis explores different factors that may be associated with diabetes, including:

* Gender
* Age
* Hypertension
* Heart Disease
* Smoking History
* BMI
* HbA1c Level
* Blood Glucose Level

The project focuses on **data cleaning, preprocessing, visualization, categorical encoding, and correlation analysis** to understand patterns in the dataset.

---

## 🎯 Objectives

The main objectives of this project are:

* Understand the structure of the diabetes dataset.
* Identify and remove duplicate records.
* Check and handle missing values.
* Clean unnecessary categorical values.
* Analyze the distribution of important variables.
* Explore relationships between diabetes and other health-related factors.
* Recategorize smoking history.
* Apply one-hot encoding to categorical variables.
* Generate correlation matrices and visualize relationships with the diabetes target variable.

---

## 📊 Dataset

The dataset contains **100,000 records and 9 columns**.

### Features

| Column                | Description                                        |
| --------------------- | -------------------------------------------------- |
| `gender`              | Gender of the individual                           |
| `age`                 | Age of the individual                              |
| `hypertension`        | Indicates whether the individual has hypertension  |
| `heart_disease`       | Indicates whether the individual has heart disease |
| `smoking_history`     | Smoking history of the individual                  |
| `bmi`                 | Body Mass Index                                    |
| `HbA1c_level`         | HbA1c level                                        |
| `blood_glucose_level` | Blood glucose level                                |
| `diabetes`            | Target variable indicating diabetes status         |

### Target Variable

`diabetes`

* `0` → No diabetes
* `1` → Diabetes

---

## 🧹 Data Cleaning & Preprocessing

The following preprocessing steps were performed:

### 1. Duplicate Removal

Duplicate records were identified and removed from the dataset.

```python
duplicate_rows_data = df[df.duplicated()]
df = df.drop_duplicates()
```

### 2. Missing Value Check

Missing values were checked using:

```python
df.isnull().sum()
```

### 3. Removing Unnecessary Category

The `Other` category from the `gender` column was removed because it represented a very small portion of the dataset.

```python
df = df[df['gender'] != 'Other']
```

### 4. Smoking History Recategorization

The original smoking categories were grouped into three categories:

* `non-smoker`
* `current`
* `past_smoker`

This was done to simplify the smoking-history analysis.

### 5. One-Hot Encoding

Categorical variables such as `gender` and `smoking_history` were converted into numerical dummy variables using one-hot encoding.

---

## 📈 Exploratory Data Analysis

Several visualizations were created to understand the dataset.

### Visualizations Included

* Age Distribution
* Gender Distribution
* BMI Distribution
* Hypertension Distribution
* Heart Disease Distribution
* Diabetes Distribution
* Smoking History Distribution
* BMI vs Diabetes
* Age vs Diabetes
* Gender vs Diabetes
* HbA1c Level vs Diabetes
* Blood Glucose Level vs Diabetes
* Age vs BMI
* BMI vs Diabetes by Gender
* Age vs Diabetes by Gender
* Correlation Matrix Heatmap
* Correlation with Diabetes

These visualizations help identify patterns and relationships between different variables and diabetes status.

---

## 🔥 Correlation Analysis

A correlation matrix was created after preprocessing the categorical variables.

The project also calculates the correlation of individual features with the `diabetes` target variable.

```python
correlation_matrix = data.corr()

corr = data.corr()
target_corr = corr['diabetes'].drop('diabetes')
target_corr_sorted = target_corr.sort_values(ascending=False)
```

This helps identify which numerical and encoded variables have stronger relationships with diabetes.

---

## 🛠️ Technologies & Libraries

The project was developed using **Python** and the following libraries:

* 🐍 Python
* 🐼 Pandas
* 🔢 NumPy
* 📊 Matplotlib
* 📈 Seaborn
* 🤖 Scikit-learn
* ⚖️ Imbalanced-learn

### Machine Learning Libraries Imported

The notebook also imports tools for:

* Train-test splitting
* Standard scaling
* One-hot encoding
* Random Forest Classification
* Grid Search
* Classification metrics
* SMOTE
* Random Under Sampling
* Machine learning pipelines

---

## 📁 Project Structure

```text
Diabetes-Prediction-EDA-Using-Python/
│
├── diabetes_prediction.ipynb
├── diabetes_prediction_dataset.csv
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Diabetes-Prediction-EDA-Using-Python.git
```

### 2. Navigate to the Project Folder

```bash
cd Diabetes-Prediction-EDA-Using-Python
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```

### 4. Open the Notebook

```bash
jupyter notebook diabetes_prediction.ipynb
```

Run the notebook cells sequentially to reproduce the analysis.

---

## 🔍 Key Areas Explored

The project investigates relationships such as:

* **Age vs Diabetes**
* **BMI vs Diabetes**
* **HbA1c Level vs Diabetes**
* **Blood Glucose Level vs Diabetes**
* **Gender vs Diabetes**
* **Smoking History vs Diabetes**
* **Hypertension vs Diabetes**
* **Heart Disease vs Diabetes**

---

## 📌 Project Outcome

This project provides a structured exploration of a diabetes dataset through data cleaning, visualization, categorical preprocessing, and correlation analysis.

The analysis helps understand how demographic, lifestyle, and health-related variables are distributed and how they relate to the diabetes target variable.

---

## 👨‍💻 Author

**Mohd Zaid Khan**

BCA — Data Science & Artificial Intelligence
Babu Banarasi Das University, Lucknow

---

## ⭐ If You Like This Project

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---

## 📜 License

This project is intended for **educational and learning purposes**.
