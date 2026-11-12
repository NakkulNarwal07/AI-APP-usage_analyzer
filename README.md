
# AI-Powered Adaptive Digital Wellbeing System

## About the Project

The AI-Powered Adaptive Digital Wellbeing System is a machine-learning-based project designed to analyze users' digital usage patterns and identify potential risks of problematic smartphone usage.

The system uses machine learning to analyze factors such as daily screen time, social media usage, gaming time, sleep duration, and other behavioural patterns.

Based on the prediction, the system aims to provide personalized digital wellbeing recommendations, usage warnings, and suggested app time limits.

This project focuses on developing the machine-learning model and the overall digital wellbeing system.

## Objectives

- Analyze users' digital usage patterns.
- Identify patterns associated with problematic smartphone usage.
- Predict digital addiction risk using machine learning.
- Provide personalized usage recommendations.
- Suggest suitable screen-time limits.
- Encourage healthier digital habits.
- Improve recommendations using user feedback.

## Dataset

The project uses the following dataset:

`cleaned_mobile_addiction.csv`

The dataset has previously been described as containing approximately 7,500 records and 14 features.

Some example features include:

- `daily_screen_time_hours`
- `social_media_hours`
- `gaming_hours`
- `sleep_hours`
- `stress_level`
- `notifications_per_day`
- `app_opens_per_day`
- `weekend_screen_time`

### Target Variables

- `addicted_label`: Used for binary classification.
- `addiction_level`: Can be considered for multi-class classification, depending on its definition.

**Note:** Target-derived columns must not be included as input features because this can cause data leakage.

## Project Workflow

The project follows these main steps:

1. Dataset Collection
2. Exploratory Data Analysis (EDA)
3. Data Cleaning
4. Feature Selection
5. Data Preprocessing
6. Train-Test Split
7. Machine Learning Model Training
8. Model Evaluation
9. Best Model Selection
10. Risk Prediction
11. Adaptive Decision Engine
12. Personalized Recommendations
13. User Feedback and Improvement

## Machine Learning Models

The following algorithms will be considered:

- Logistic Regression
- Random Forest Classifier
- Gradient Boosting Classifier
- XGBoost (optional)

The models will be compared to identify the most suitable model for predicting digital usage risk.

## Model Evaluation

The models will be evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- ROC-AUC Score

Accuracy alone will not be used to select the best model, especially if the dataset has imbalanced classes.

## System Functionality

### 1. Usage Analysis

The system analyzes digital usage information and identifies patterns in screen time and app usage.

### 2. Risk Prediction

The trained machine-learning model predicts the likelihood of problematic digital usage.

### 3. Adaptive Decision Engine

Based on the prediction, the decision engine selects an appropriate response.

Example responses:

- Low Risk: Display usage statistics and positive feedback.
- Moderate Risk: Show a gentle screen-time warning.
- High Risk: Suggest a personalized usage limit.

### 4. Personalized Recommendations

The system suggests alternative activities such as:

- Reading
- Walking
- Studying
- Exercising
- Taking a break
- Spending time away from screens

### 5. Feedback System

The system collects user feedback and uses it to improve future recommendations.

## Project Structure

```text
digital_wellbeing_ml/
│
├── dataset/
│   └── cleaned_mobile_addiction.csv
│
├── notebooks/
│   └── 01_exploratory_analysis.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── feature_selection.py
│   ├── train.py
│   ├── evaluate.py
│   ├── predict.py
│   └── decision_engine.py
│
├── models/
│   └── best_model.joblib
│
├── outputs/
│   ├── confusion_matrix.png
│   └── model_metrics.csv
│
├── requirements.txt
└── README.md
```

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Joblib

Optional:
- XGBoost

## Installation and Setup

### Step 1: Clone the Repository

```bash
git clone <your-repository-url>
```

### Step 2: Open the Project Folder

```bash
cd digital_wellbeing_ml
```

### Step 3: Create a Virtual Environment

```bash
python -m venv .venv
```

Activate the environment.

**Windows:**

```bash
.venv\Scripts\activate
```

**Linux / macOS:**

```bash
source .venv/bin/activate
```

### Step 4: Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter joblib
```

## Getting Started

First, place the dataset inside the `dataset` folder.

Start Jupyter Notebook:

```bash
jupyter notebook
```

Create or open:

`notebooks/01_exploratory_analysis.ipynb`

Load the dataset using:

```python
import pandas as pd

df = pd.read_csv("../dataset/cleaned_mobile_addiction.csv")

print(df.head())
print(df.shape)
print(df.info())
print(df.isnull().sum())
```

Start with exploratory data analysis before training the machine-learning models.

## Prediction Example

The prediction module will generate an output similar to the following:

```python
{
    "predicted_class": 1,
    "risk_probability": 0.82
}
```

This is only an illustrative example, not an actual result from the dataset.

The prediction can then be passed to the adaptive decision engine to determine the recommended action.

## Future Enhancements

- Improve prediction accuracy and reliability.
- Add personalized risk thresholds.
- Develop a recommendation system.
- Introduce adaptive usage-limit suggestions.
- Track user progress over time.
- Improve personalization using feedback.
- Evaluate the effectiveness of interventions.

## Responsible Use

- Predictions are estimates, not medical diagnoses.
- Correlation does not establish causation.
- The model should be tested for bias and data leakage.
- Recommendations should be supportive rather than judgmental.
- Users should remain in control of their wellbeing choices.

## Development Status

Currently in the machine-learning development and system-design phase.

## License

A suitable open-source license can be added before publishing the project. Ensure that the dataset's own license and usage conditions are followed.
