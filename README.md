# 📊 Height Prediction Model

## 📌 Overview

This project is a Machine Learning model that predicts a person's **height (in cm)** based on features like age, gender, weight, diet, exercise, and parents' height.

---

## 🚀 Features

* Handles **missing values (NaN)**
* Converts **categorical data (strings)** into numerical format
* Uses **Linear Regression** for prediction
* Includes **data visualization**
* Supports **model evaluation using R² score**

---

## 🧠 Technologies Used

* Python 🐍
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

---

## 📂 Dataset Details

### Input Features:

* Age
* Gender
* Weight (kg)
* Diet (Veg / Non-Veg)
* Exercise (Yes / No)
* Parents Height (cm)

### Target:

* Height (cm)

---

## ⚙️ Data Preprocessing

Steps performed:

1. Handle missing values using mean:

```python
df.fillna(df.mean(numeric_only=True), inplace=True)
```

2. Convert categorical data into numeric:

```python
df = pd.get_dummies(df)
```

---

## 🏗️ Model Training

* Train-Test Split (80-20)
* Feature Scaling using StandardScaler
* Model: Linear Regression

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)
```

---

## 📊 Model Evaluation

* R² Score is used to evaluate performance

```python
from sklearn.metrics import r2_score

y_pred = model.predict(X_test)
print(r2_score(y_test, y_pred))
```

---

## ▶️ How to Run

1. Install dependencies:

```
pip install pandas numpy scikit-learn matplotlib
```

2. Run the notebook or script:

```
python main.py
```

---

