# BHP-Housing-project
Real Estate Price Prediction using Linear Regression. Includes data cleaning, feature engineering, outlier removal, one-hot encoding, model training, evaluation, and persistence for deployment.
# 🏠 Real Estate Price Prediction

## 📌 Overview
This project predicts **real estate property prices** using a structured dataset.  
It demonstrates the complete workflow from data preprocessing to model deployment-ready persistence.  

The pipeline includes:
- Data loading and cleaning
- Feature engineering
- Outlier removal
- Encoding categorical features
- Model training and evaluation
- Optional hyperparameter tuning
- Making predictions with a saved model

---

## 🗂️ Project Workflow

### 1. Load Data
- Imported raw CSV using **`pandas.read_csv`**
- Initial inspection for columns, null values, and data types

### 2. Data Cleaning
- Dropped noisy or irrelevant columns
- Handled missing values
- Tools: `DataFrame.drop`, `isnull()`

### 3. Feature Engineering
- Extracted **BHK (bedroom count)**
- Converted **total_sqft** to numeric
- Computed **price_per_sqft**
- Tools: custom functions with `apply()`

### 4. Outlier Removal
- Removed unrealistic price points per location and BHK
- Applied **groupby logic** and **Z-score method** to detect anomalies

### 5. Encoding
- One-hot encoded **location** column
- Dropped “other” category to avoid multicollinearity
- Tool: `pd.get_dummies()`

### 6. Model Training
- Fitted **Linear Regression** on preprocessed data
- Tool: `sklearn.linear_model.LinearRegression`

### 7. Evaluation
- Metrics: **R² score**, **cross-validation**
- Tools: `train_test_split`, `cross_val_score`

### 8. Hyperparameter Search (Optional)
- Grid search over several regressors to improve performance
- Tool: `GridSearchCV`

### 9. Prediction
- Created a **function** to build a feature vector and call `model.predict()`
- Tool: `numpy` for array manipulation

### 10. Model Persistence
- Saved trained model and column list for deployment
- Tools: `pickle`, `json`

---

## ⚙️ Tech Stack
- **Python**
- **Jupyter Notebook**
- **Pandas, NumPy**
- **Scikit-learn**
- **Matplotlib, Seaborn** (for visualization)
- **Pickle, JSON** (for saving model & metadata)

---

## 🚀 How to Run

```bash
# Clone repository
git clone https://github.com/<DevikaYanamala>/<BHP-Housing-Project>.git

# Enter project directory
cd <BHP-Housing-Project>

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook
