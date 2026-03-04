# 🏠 Multiple Linear Regression – Housing Price Prediction

## 📌 Project Overview

This project demonstrates **Multiple Linear Regression** using Scikit-learn to predict housing prices based on multiple independent variables such as area, number of bedrooms, bathrooms, stories, and additional amenities.

The notebook walks through:

* Data preprocessing
* Exploratory Data Analysis (EDA)
* Feature encoding
* Feature scaling
* Model training
* Model evaluation
* Predicting prices for new custom input data

---

## 📂 Dataset

The dataset used:

* **Housing.csv**
* Target variable: `price`
* Features include:

  * `area`
  * `bedrooms`
  * `bathrooms`
  * `stories`
  * `mainroad`
  * `guestroom`
  * `basement`
  * `hotwaterheating`
  * `airconditioning`
  * `parking`
  * `prefarea`
  * `furnishingstatus`

---

## 🧠 What is Multiple Linear Regression?

Multiple Linear Regression predicts a dependent variable (y) using multiple independent variables (x₁, x₂, x₃ … xₙ).

### Formula:

[
y = m_1x_1 + m_2x_2 + ... + m_nx_n + c
]

It fits a hyperplane in multi-dimensional space to best model the relationship between features and the target.

---

## ⚙️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

---

## 🚀 Project Workflow

### 1️⃣ Import Libraries

* `LinearRegression`
* `train_test_split`
* `StandardScaler`
* Performance metrics (`MAE`, `R² Score`)

---

### 2️⃣ Data Loading

* Load dataset using `pandas.read_csv()`
* Convert to DataFrame

---

### 3️⃣ Exploratory Data Analysis (EDA)

* Correlation heatmap using Seaborn
* Understanding relationships between numeric features

---

### 4️⃣ Encoding Categorical Variables

* Manual mapping (`yes/no → 1/0`)
* `replace()` method
* One-hot encoding using `pd.get_dummies()`

---

### 5️⃣ Train-Test Split

```python
train_test_split(test_size=0.3, random_state=42)
```

* 70% Training data
* 30% Testing data

---

### 6️⃣ Feature Scaling

Standardization using:

```python
StandardScaler()
```

⚠️ Note: Scaling ensures all features contribute equally to the model.

---

### 7️⃣ Model Training

```python
LinearRegression().fit()
```

The model learns the relationship between features and housing prices.

---

### 8️⃣ Model Evaluation

Metrics used:

* **MAE (Mean Absolute Error)**
* **R² Score**

```python
mean_absolute_error()
r2_score()
```

* MAE → Measures average prediction error.
* R² Score → Measures how well the model explains variance.

---

### 9️⃣ Predicting New House Price

Steps:

1. Create a new house DataFrame
2. Reorder columns to match training data
3. Scale using the trained scaler
4. Predict using the trained model

```python
lr.predict()
```

---

## 📊 Example Prediction Input

```python
new_house = {
  'area': 1200,
  'bedrooms': 3,
  'bathrooms': 3,
  'stories': 2,
  'mainroad': 1,
  'guestroom': 1,
  'basement': 1,
  'hotwaterheating': 1,
  'airconditioning': 0,
  'parking': 0,
  'prefarea': 1,
  'furnishingstatus_semi-furnished': 0,
  'furnishingstatus_unfurnished': 0
}
```

---

## 📈 Results

* Model successfully predicts housing prices.
* Performance evaluated using MAE and R² score.
* Demonstrates end-to-end ML workflow from raw data to prediction.

---

## 📌 Key Learning Outcomes

✔ Handling categorical variables
✔ Feature scaling
✔ Train-test splitting
✔ Model evaluation techniques
✔ Real-world regression implementation
✔ Making predictions on custom input

---

## 🛠 How to Run the Project

1. Clone the repository
2. Install required libraries:

   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
   ```
3. Place `Housing.csv` in the project directory
4. Run the Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

---

## 📬 Future Improvements

* Add cross-validation
* Try regularization (Ridge/Lasso)
* Perform feature selection
* Deploy as a web application
* Add residual analysis

---

## 👨‍💻 Author

Machine Learning Regression Project
Built for learning and practicing supervised learning techniques.

---

⭐ If you found this helpful, consider giving the project a star!
