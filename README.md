# 🧠 Addiction Population Data - Exploratory Data Analysis (EDA)

This project explores a dataset related to addiction behavior across different demographics and health indicators. The dataset includes information like age, gender, BMI, sleep patterns, alcohol consumption, smoking behavior, education level, therapy history, and more.

> ✅ Tools used: **Python**, **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**, **Jupyter Notebook**

---

## 📁 Dataset Overview

The dataset includes the following columns (partial list):
- `age`
- `gender`
- `bmi`
- `sleep_hours`
- `drinks_per_week`
- `smokes_per_day`
- `education_type`
- `therapy_history`
- `social_support`
- `children_count`

---

## 📊 Exploratory Data Analysis

### 1. **Missing Values**
- Categorical columns like:
  - `education_type` → 420 nulls
  - `social_support` → 753 nulls
  - `therapy_history` → 1014 nulls
- Handled using **mode imputation** for simplicity.

### 2. **Outlier Detection**
Used boxplots and IQR method for detecting outliers in:
- `bmi`
- `sleep_hours`
- `smokes_per_day`
- `drinks_per_week`

Outliers were visualized and optionally capped using domain knowledge or percentile clipping.

### 3. **Categorical Encoding**
Converted categories to numeric using:
- `gender`: one-hot encoding
- `education_type`, `therapy_history`: label encoding or one-hot based on context

This step prepares the dataset for modeling later.

### 4. **Visualizations**
- **Bar charts** and **histograms** were used to inspect:
  - Smoking habits by gender
  - Drinking habits by gender
  - Distribution of age, BMI, and sleep
- **Top 10 countries** by average smoking and drinking levels
- **Heatmap** of correlation between numerical variables

### 5. **Insights from Correlation**
Correlation values between most variables were low (±0.01 to ±0.04), suggesting weak linear relationships.

However, feature importance from models later revealed non-linear relationships (explored in modeling phase).

---

## 📌 Key Insights
- Smoking behavior is somewhat associated with **age**, **BMI**, and **sleep_hours**.
- Very weak linear correlations between features (but modeling shows better feature importance).
- Categorical variables like `education_type` and `therapy_history` may hold non-obvious value for segmentation.

---

## 📁 Project Structure

📦 addiction-eda/
┣ 📜 addiction_population_data.csv
┣ 📓 addiction_eda.ipynb

## 📌 Author
Shahriar Shourov 
