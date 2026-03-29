# Customer Churn Prediction using Machine Learning

## Objective
The objective of this project is to predict whether a customer will leave a telecom service (customer churn) using machine learning algorithms and compare their performance with a rule-based approach.

---

## Dataset
This project uses the **IBM Telco Customer Churn Dataset**.

Since the assessment specified different fields, the dataset columns were mapped as follows:

| Assessment Field | Dataset Column |
|------------------|---------------|
| Age | tenure |
| Income | MonthlyCharges |
| Purchases | TotalCharges |
| Membership | Contract |
| Churn | Churn |

---

## Project Workflow

### 1. Data Loading
The dataset is loaded using the Pandas library.

### 2. Data Cleaning
- Removed the `customerID` column since it is not useful for prediction.
- Converted `TotalCharges` to numeric format.
- Removed rows with missing values.

### 3. Feature Selection
Selected relevant columns and renamed them to match the assessment requirements.

### 4. Categorical Encoding
Converted categorical variables into numeric values using **Label Encoding**.

### 5. Train-Test Split
The dataset was split into:
- 80% Training data
- 20% Testing data

---

## Machine Learning Models Used

The following machine learning algorithms were implemented:

1. Logistic Regression  
2. Random Forest Classifier  
3. XGBoost Classifier  

Each model was trained and evaluated using **accuracy score** and **classification report**.

---

## Rule-Based Churn Logic

A simple rule-based churn prediction system was implemented to simulate business logic.

Example rules:
- Customers with low purchases and certain membership types may churn.
- Customers with high income but low purchases may churn.
- Customers with short tenure may churn.

This rule-based approach is compared with machine learning models.

---

## Model Performance Comparison

| Model | Accuracy |
|------|---------|
| Logistic Regression | ~77% |
| Random Forest | ~77% |
| XGBoost | **78.18%** |
| Rule-Based Logic | Lower than ML models |

### Best Model
**XGBoost** achieved the highest accuracy because boosting algorithms capture complex patterns in customer behavior more effectively.

---

## Visualization
A bar chart was created to show the distribution of churn vs non-churn customers in the dataset.

---

## Project Outputs

The project generates the following outputs:

- `cleaned_churn_data.csv` – cleaned dataset
- `model_comparison_summary.txt` – model comparison results
- Visualization of churn distribution
- Jupyter Notebook containing the full implementation

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost
- Jupyter Notebook

---

## Conclusion

The machine learning models performed better than the rule-based logic in predicting customer churn. Among the tested models, **XGBoost achieved the highest accuracy**, indicating that boosting-based algorithms are effective for structured customer datasets.

---

## Author

**Anisha Raichel**  
M.Sc Artificial Intelligence and Machine Learning  
Coimbatore Institute of Technology
