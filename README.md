# Smart Outcome Predictor – Supervised Learning

## Project Overview

This project focuses on predicting student learning outcomes using Supervised Machine Learning techniques.

The project uses student activity, course information, quiz performance, attendance and other learning-related data to predict:

- **Classification:** Student completion status.
- **Regression:** Student final score.

The main goal is to understand student performance and identify useful patterns using different machine learning and ensemble learning algorithms.

## Dataset Information

- **Dataset:** Smart Outcome Predictor Dataset
- **Total Records:** 5,200
- **Original Features:** 19
- **Target Variables:**
  - `completion_status` – Classification target
  - `final_score` – Regression target

### Features

The dataset contains information such as:

- Student age and country/region
- Device type and education background
- Course level and course category
- Course start date and week of year
- Sessions and time spent
- Videos watched and quiz attempts
- Assignments submitted and forum posts
- Average quiz score and attendance rate

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- LightGBM
- XGBoost

## Project Workflow

### 1. Data Loading and Understanding
- Loaded the dataset.
- Checked rows, columns and data types.
- Analyzed missing values and duplicate records.

### 2. Data Preprocessing
- Handled missing values using median imputation.
- Converted course start date into datetime format.
- Converted course level into numerical values.
- Applied One-Hot Encoding to categorical features.
- Removed unnecessary columns such as student ID and course start date.
- Prepared separate target variables for classification and regression.

### 3. Train-Test Split
- Training data: 80%
- Testing data: 20%
- Random state: 32

### 4. Feature Scaling
Applied StandardScaler to scale numerical features for classification and regression tasks.

### 5. Ensemble Learning Techniques

Implemented the following ensemble algorithms:

**Classification Models**
- Bagging Classifier
- AdaBoost Classifier
- Gradient Boosting Classifier
- LightGBM Classifier
- XGBoost Classifier
- Voting Classifier
- Stacking Classifier

**Regression Models**
- AdaBoost Regressor
- Gradient Boosting Regressor
- LightGBM Regressor
- Stacking Regressor

## Model Evaluation

### Classification Metrics
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

### Regression Metrics
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R2 Score

## Results and Best Models

### Classification Results

| Model | Accuracy | F1-Score |
|---|---:|---:|
| Bagging | 69.52% | 0.5426 |
| AdaBoost | 65.48% | 0.5344 |
| Gradient Boosting | 70.87% | 0.5786 |
| LightGBM | 70.96% | 0.5806 |
| XGBoost | 71.25% | 0.5910 |
| Voting | 69.42% | 0.5000 |
| Stacking | 70.29% | 0.5400 |

**Best Classification Model: XGBoost Classifier**

- Accuracy: 71.25%
- F1-Score: 0.5910

### Regression Results

| Model | MAE | RMSE | R2 Score |
|---|---:|---:|---:|
| AdaBoost | 74.3263 | 74.6350 | -23765.9667 |
| Gradient Boosting | 74.5115 | 75.0190 | -24011.1455 |
| LightGBM | 74.3821 | 74.9895 | -23992.2484 |
| Stacking | 9.2060 | 11.2153 | 0.2844 |

**Best Regression Model: Stacking Regressor**

- MAE: 9.2060
- RMSE: 11.2153
- R2 Score: 0.2844

## Final Model Recommendation

- **Classification:** XGBoost Classifier is recommended because it achieved the highest accuracy and F1-score among the tested classification models.
- **Regression:** Stacking Regressor performed best among the tested regression models.

The regression model still needs improvement before real-world deployment because its R2 score is relatively low.

## How to Run the Project

1. Clone this repository:

   ```bash
   git clone YOUR_GITHUB_REPOSITORY_URL
   ```

2. Open the project folder.

3. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

4. Open Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open the project notebook and run all cells.

## Project Files

```text
Smart-Outcome-Predictor-Supervised-Learning/
│
├── Smart_Outcome_Predictor.ipynb
├── dataset.csv
├── requirements.txt
└── README.md
```

## Conclusion

This project demonstrates how supervised machine learning and ensemble learning techniques can be used to predict student completion status and final scores.

Different ensemble algorithms were trained and evaluated. XGBoost performed best for classification, while Stacking Regressor performed best for regression based on the available results.

The project helped develop practical knowledge of data preprocessing, feature engineering, model training, evaluation and model comparison.
