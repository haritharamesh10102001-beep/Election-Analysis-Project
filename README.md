# Election-Analysis-Project
#Predictive Analysis of Election Outcomes Using Machine Learning

## 📝 Project Overview

The objective of this project is to predict election outcomes using various machine learning models. The analysis is performed on a dataset of 220 Indian regions, aiming to identify key influencing factors and understand electoral trends and voter behavior patterns.

## 💾 Dataset Features

The dataset for the analysis includes the following socio-economic and political features for each region:

* **`population`**: Total population of the region.
* **`literacy_rate`**: Literacy rate percentage.
* **`average_income`**: Average income level.
* **`youth_percentage`**: Percentage of the youth population.
* **`urban_percentage`**: Percentage of the urban population.
* **`previous_winner`**: The party that won the last election.
* **`party_X_campaign_spend`**: Campaign expenditure for each party (A, B, C, D, E).
* **`unemployment_rate`**: Unemployment rate percentage.
* **`social_media_support`**: Measure of social media support.
* **`voter_turnout`**: Voter turnout percentage.
* **`region_type`**: Type of region (e.g., Semi-Urban, Rural, Urban).
* **`current_winner`**: The winning party (Target Variable).

## ⚙️ Methodology

### 1. Data Preprocessing

* **Encoding**: Categorical variables (`region_type`, `previous_winner`, `current_winner`) were encoded using `LabelEncoder`.
* **Scaling**: `StandardScaler` was applied to normalize numerical features.
* **Splitting**: The dataset was split into 80% for training and 20% for testing.

### 2. Machine Learning Models

Three different machine learning classification models were employed:

* **Decision Tree Classifier**: Configured with the `entropy` criterion and a `Max Depth` of 6.
* **Random Forest Classifier**: An ensemble of 100 trees used to reduce overfitting and evaluate feature importance.
* **Logistic Regression**: Used as a linear model for baseline comparison, with `Max iterations` set to 5000.

### 3. Model Performance Summary (Accuracy)

| Model | Accuracy |
| :--- | :--- |
| **Logistic Regression** | **88.64%** |
| Random Forest Classifier | 81.82% |
| Decision Tree Classifier | 77.27% |

The **Logistic Regression** model achieved the highest overall accuracy on the test set.

### 4. Key Findings

* **Feature Importance**: The Random Forest model identified **Campaign Spend** as one of the top features influencing election predictions.
* **Best Model Performance**: Logistic Regression showed the best overall metrics, including perfect Precision and Recall (1.0) for Class 0, and a high F1-score (0.952) for Class 4.
