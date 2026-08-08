# Titanic Survival Prediction

A Data Science and Machine Learning practice project based on Kaggle's [Titanic - Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic) dataset. The goal is to predict whether a passenger survived.

## What This Project Covers

- Exploring data from 891 passengers and understanding the `Survived` target
- Handling missing values with `SimpleImputer`
- Encoding categorical data with One-Hot Encoding
- Using `Pipeline` and `ColumnTransformer` to prevent data leakage
- Evaluating models with Stratified 5-Fold Cross-Validation
- Tuning a Decision Tree's `max_depth` with `GridSearchCV`
- Creating features from raw data:
  - `FamilyGroup`: Alone, Small, and Large
  - `Title`: honorifics such as Mr, Miss, Mrs, Master, and Rare

## Project Structure

```text
titanic_project/
├── data/                         # train.csv and test.csv (not tracked by Git)
├── notebooks/
│   └── titanic.ipynb             # Main notebook; runs from top to bottom
├── decision_tree_submission.csv  # Kaggle submission file (not tracked by Git)
├── requirements.txt              # Python package requirements
└── README.md
```

## Model Workflow

1. Load `train.csv` and `test.csv`.
2. Create `FamilySize`, `FamilyGroup`, and `Title` features.
3. Split the training data while preserving the survival-rate distribution with `stratify=y`.
4. Preprocess data inside a Pipeline:
   - Numerical features: median imputation and scaling
   - Categorical features: most-frequent imputation and One-Hot Encoding
5. Use `GridSearchCV` to find an appropriate Decision Tree `max_depth`.
6. Evaluate the model with a validation split and 5-Fold Cross-Validation.
7. Refit the selected model on all labeled training data and generate a submission file.

## Latest Results

| Evaluation | Score |
|---|---:|
| Validation accuracy | 0.832 |
| 5-Fold CV accuracy (Decision Tree) | 0.829 |
| Kaggle Public Leaderboard | 0.76315 |

> The Kaggle Public Leaderboard score is measured on external test data, so it may differ from local validation and Cross-Validation scores.

## Installation and Usage

Python 3.12 or later is required.

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Open `notebooks/titanic.ipynb` in VS Code and select the `Python (titanic-project)` kernel, or choose the interpreter from `.venv`. Run all notebook cells in order.

After execution, `decision_tree_submission.csv` will be created in the project root and is ready to upload to Kaggle.

## Possible Next Steps

- Compare Logistic Regression, Random Forest, and XGBoost using the same CV setup.
- Add features from `Ticket` and `Cabin`, then validate their impact with Cross-Validation.
- Reserve an internal test set for final evaluation before submitting to Kaggle.
- Try an ensemble only when the component models make meaningfully different errors.
