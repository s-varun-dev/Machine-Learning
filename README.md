# Machine-Learning
# 📈 Simple Linear Regression from Scratch and Scikit-Learn

A beginner-friendly Machine Learning project demonstrating **Simple Linear Regression** using Python. This project predicts insurance premiums based on a person's age and includes both **manual evaluation calculations** and **Scikit-Learn implementation**.

---

## 🚀 Project Overview

Simple Linear Regression is one of the most fundamental supervised machine learning algorithms used to model the relationship between:

- **Independent Variable (X):** Age
- **Dependent Variable (Y):** Insurance Premium

This notebook walks through the complete regression workflow, including:

✅ Data Loading  
✅ Data Preprocessing  
✅ Train-Test Split  
✅ Model Training  
✅ Prediction Generation  
✅ Visualization  
✅ Performance Evaluation  
✅ R² Score Calculation (Built-in and Manual)

---

## 📂 Dataset

The dataset consists of two columns:

| Feature | Description |
|----------|-------------|
| Age | Independent Variable |
| Premium | Target Variable |

Example:

| Age | Premium |
|------|---------|
| 25 | 18000 |
| 30 | 25000 |
| 40 | 40000 |
| 50 | 55000 |

---

## 🛠️ Technologies Used

- Python 3.x
- NumPy
- Pandas
- Matplotlib
- Scikit-Learn
- Jupyter Notebook

---

## 📋 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/simple-linear-regression.git
```

Move into the project directory:

```bash
cd simple-linear-regression
```

Install required packages:

```bash
pip install numpy pandas matplotlib scikit-learn
```

---

## ▶️ Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
simple_linear_regression.ipynb
```

Run all cells sequentially.

---

## 🧠 Machine Learning Workflow

### 1. Import Libraries

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
```

### 2. Load Dataset

```python
df = pd.read_csv("simplelinearregression.csv")
```

### 3. Prepare Features and Labels

```python
X = df[['Age']]
y = df['Premium']
```

### 4. Split Dataset

```python
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.3,
    random_state=42
)
```

### 5. Train Model

```python
reg = LinearRegression()
reg.fit(X_train, y_train)
```

### 6. Generate Predictions

```python
predict_ans = reg.predict(X_train)
```

---

## 📊 Model Visualization

Training data and regression line are visualized using Matplotlib.

```python
plt.scatter(X_train, y_train)
plt.plot(X_train, predict_ans)
plt.show()
```

This helps understand how well the regression line fits the training data.

---

## 📈 Performance Evaluation

### Using Scikit-Learn

```python
from sklearn.metrics import r2_score

r2 = r2_score(y_train, predict_ans)
print(r2)
```

### Manual R² Calculation

The notebook also demonstrates how to calculate the R² score manually without using built-in functions.

Formula:

\[
R^2 = 1 - \frac{SS_{res}}{SS_{tot}}
\]

Where:

- **SSres** = Sum of Squared Residuals
- **SStot** = Total Sum of Squares

---

## 🔍 Sample Prediction

Predict insurance premium for a new age:

```python
reg.predict([[29]])
```

Example output:

```text
[35000]
```

---

## 📁 Project Structure

```text
simple-linear-regression/
│
├── simple_linear_regression.ipynb
├── simplelinearregression.csv
├── README.md
└── requirements.txt
```

---

## 🎯 Learning Outcomes

After completing this project, you will understand:

- What is Simple Linear Regression
- Relationship between dependent and independent variables
- Model training and prediction
- Train-test splitting
- R² Score
- Mean Squared Error (MSE)
- Data visualization
- Manual performance metric calculations

---

## 📚 Concepts Covered

- Supervised Learning
- Regression Analysis
- Linear Regression Equation
- Model Evaluation
- Data Visualization
- Feature Engineering Basics

---

## 🔮 Future Improvements

- Multiple Linear Regression
- Polynomial Regression
- Feature Scaling
- Cross Validation
- Model Deployment using Flask or Streamlit
- Interactive Web Interface

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome.

Feel free to fork the repository and submit a pull request.

---

## ⭐ Support

If you found this project useful, please consider giving it a star ⭐ on GitHub.

---

## 👨‍💻 Author

Developed as part of a Machine Learning learning journey using Python and Scikit-Learn.
