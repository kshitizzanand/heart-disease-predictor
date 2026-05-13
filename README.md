# Heart Disease Predictor

A binary classification project to predict presence of heart disease
using the Kaggle Heart Disease dataset (Cleveland data).

## Key Finding During EDA
Dataset contained 723 duplicate rows (70% of 1025 rows) — removed 
before any processing. All results are on 302 clean, unique records.

## What I Did
- Identified categorical vs numerical features from domain knowledge
- One-hot encoded nominal categoricals (thal, restecg)
- Train-test split → StandardScaler → model training
- Evaluated using recall as primary metric: missing a sick patient 
  is worse than a false alarm in medical context
- Hyperparameter tuned KNN via GridSearchCV (scoring=recall)

## Results
| Model | Accuracy | Recall (disease) | Missed Patients |
|---|---|---|---|
| Logistic Regression | 0.74 | 0.83 | 5 |
| KNN (tuned) | 0.74 | 0.79 | 6 |

## Conclusion
Logistic Regression selected — equal accuracy, higher recall, 
and greater interpretability for clinical use.

## Tools
Python, Pandas, Scikit-learn, Google Colab