# 🏦 Loan Prediction System

A Machine Learning project that predicts whether a loan application is likely to be approved or rejected based on applicant information. The project explores multiple classification algorithms, performs data preprocessing, and evaluates model performance to understand how machine learning can support loan approval decisions.

## 📌 Project Overview

Loan approval is an important process in the banking and financial sector. Evaluating applications involves considering various factors, including applicant income, credit history, employment status, loan amount, and property area.

This project uses supervised machine learning techniques to analyze applicant data and predict loan approval status.

The project implements seven classification algorithms and evaluates their performance using cross-validation. Logistic Regression is used in the notebook's primary prediction workflow.

## 🎯 Objectives

- Analyze loan applicant data.
- Perform data cleaning and preprocessing.
- Handle missing values in the dataset.
- Convert categorical variables into numerical representations.
- Explore relationships between features using correlation analysis.
- Implement and compare multiple machine learning classification algorithms.
- Evaluate model performance using cross-validation.
- Predict loan approval status using a trained classification model.

## 🤖 Machine Learning Algorithms

The project explores the following seven classification algorithms:

| No. | Algorithm | Description |
|---|---|---|
| 1 | Logistic Regression | Predicts the probability of loan approval using a classification model. |
| 2 | Decision Tree Classifier | Uses decision rules to classify loan applications. |
| 3 | Linear Discriminant Analysis (LDA) | Uses statistical class separation for classification. |
| 4 | Random Forest Classifier | Combines multiple decision trees to generate predictions. |
| 5 | Support Vector Classifier (SVC) | Classifies observations using a separating decision boundary. |
| 6 | K-Nearest Neighbors (KNN) | Classifies applicants based on neighboring observations. |
| 7 | Gaussian Naive Bayes | Applies Bayes' theorem with a Gaussian likelihood assumption. |

### Primary Prediction Model

**Logistic Regression** is used in the notebook's primary prediction workflow.

The model is trained on the prepared training data and used to predict loan approval outcomes. Its performance is evaluated using accuracy, a confusion matrix, and a classification report.

The notebook also explores the other six algorithms through cross-validation.

## 📊 Dataset

The project uses training and test datasets containing loan applicant information.

- `train.csv` — Contains applicant features and loan approval labels.
- `test.csv` — Contains applicant features for prediction.

The notebook loads these files from the `Loan_Data` directory.

### Important Features

| Feature | Description |
|---|---|
| `Loan_ID` | Loan application identifier |
| `Gender` | Applicant's gender |
| `Married` | Marital status |
| `Dependents` | Number of dependents |
| `Education` | Education level |
| `Self_Employed` | Employment category |
| `ApplicantIncome` | Applicant's income |
| `CoapplicantIncome` | Co-applicant's income |
| `LoanAmount` | Requested loan amount |
| `Loan_Amount_Term` | Loan repayment term |
| `Credit_History` | Credit history indicator |
| `Property_Area` | Property location category |
| `Loan_Status` | Loan approval outcome |

The `Loan_Status` column is the target variable in the training dataset.

## 🛠️ Technologies Used

- **Python** — Programming language
- **Pandas** — Data manipulation and analysis
- **NumPy** — Numerical computations
- **Matplotlib** — Data visualization
- **Seaborn** — Correlation heatmaps
- **Scikit-learn** — Machine learning algorithms and model evaluation
- **Jupyter Notebook** — Interactive development and experimentation
- **Pickle** — Model serialization

## 🔄 Project Workflow

```text
        Loan Applicant Dataset
                  |
                  v
          Data Exploration
                  |
                  v
       Missing Value Analysis
                  |
                  v
          Data Preprocessing
                  |
                  v
       Categorical Data Encoding
                  |
                  v
         Correlation Analysis
                  |
                  v
         Feature Preparation
                  |
                  v
       Training and Validation
                  |
                  v
       Classification Algorithms
                  |
                  v
        10-Fold Cross-Validation
                  |
                  v
        Logistic Regression Model
                  |
                  v
          Model Evaluation
                  |
                  v
       Loan Approval Prediction
```

## 🧹 Data Preprocessing

The notebook performs several preprocessing operations before training the models.

### 1. Missing Value Handling

Missing values are identified using Pandas. The notebook applies imputation strategies to selected features, including median and mean imputation, as well as random assignments for certain categorical or binary values.

### 2. Categorical Encoding

Categorical features are converted into numerical representations so they can be used by the classification algorithms.

### 3. Correlation Analysis

Correlation heatmaps are generated to examine relationships between numerical features.

### 4. Feature Preparation

The `Loan_ID` column is removed from the model features, and the remaining features are prepared for training and prediction.

### 5. Training and Validation

The labeled data is divided into training and validation subsets. The training data is used to fit the model, while the validation data is used to assess its predictive performance.

## 📈 Model Evaluation

The project uses **10-fold cross-validation** to evaluate classification algorithms.

The primary Logistic Regression workflow also uses the following evaluation metrics:

- **Accuracy:** Measures the proportion of correct predictions.
- **Confusion Matrix:** Summarizes correct and incorrect classifications.
- **Precision:** Measures how many predicted positive cases are actually positive.
- **Recall:** Measures how many actual positive cases are correctly identified.
- **F1-Score:** Combines precision and recall into a single metric.

Actual performance values should be taken from the notebook's execution results. No specific accuracy score or best-model claim is reported here without verified results.

## 📂 Project Structure

The following structure represents the expected files referenced by the notebook:

```text
Loan-Prediction-System/
│
├── Loan_Data/
│   ├── train.csv
│   └── test.csv
│
├── Model/
│   └── ML_Model1.pkl
│
├── Str_Loan_ML.ipynb
│
└── README.md
```

The actual repository structure may differ. Update this section to match the files committed to GitHub.

## ⚙️ Installation and Setup

### Prerequisites

- Python 3.9 or later
- Jupyter Notebook
- Git

### Step 1: Clone the Repository

```bash
git clone https://github.com/Tusharbunny06/Loan-Prediction-System.git
```

### Step 2: Navigate to the Project Directory

```bash
cd Loan-Prediction-System
```

### Step 3: Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment on Windows:

```bash
venv\Scripts\activate
```

### Step 4: Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Step 5: Run Jupyter Notebook

```bash
jupyter notebook
```

Open `Str_Loan_ML.ipynb` and execute the cells in sequence.

**Note:** The notebook contains a hardcoded local directory path. Update or remove that path before running the notebook on another machine. Ensure the expected dataset files are available in the appropriate directory.

## 🚀 Future Improvements

Potential improvements include:

- Implementing a consistent preprocessing pipeline.
- Using reproducible imputation methods.
- Preventing data leakage by fitting preprocessing transformations on training data only.
- Comparing all seven algorithms using a results table.
- Performing hyperparameter tuning.
- Evaluating precision, recall, F1-score, and other relevant metrics.
- Saving and loading the intended trained model consistently.
- Developing a Streamlit web application for interactive predictions.
- Evaluating model fairness and potential bias in lending-related predictions.




---

⭐ If you find this project interesting, consider starring the repository!
