# 🚢 Titanic Survival Prediction

Hello! This project serves as a learning space for my very first step into Data Science. I am using the classic Titanic dataset from Kaggle to practice writing code and predict the survival opportunities of passengers.

The primary goal of this project is to practice using fundamental libraries and to understand the thought process behind basic data manipulation, preparation, and building an end-to-end Machine Learning pipeline with multiple models.

## 📂 Project Directory Structure

<blockquote>
titanic_project/<br>
│<br>
├── data/                 # Training and testing datasets (Ignored in Git)<br>
│<br>
├── notebooks/<br>
│   └── titanic.ipynb     # Main Jupyter Notebook for data processing and modeling<br>
│<br>
├── .gitignore            # Git configuration to exclude data and output files<br>
├── README.md             # Project overview and documentation<br>
├── submission.csv        # Final k-NN predictions formatted for Kaggle (Ignored in Git)<br>
└── rf_submission.csv     # Final Random Forest predictions formatted for Kaggle (Ignored in Git)
</blockquote>

## 🛠️ Tools & Libraries I am Practicing

* **Python**: Applying programming concepts to build data processing and Machine Learning pipelines.
* **Pandas & NumPy**: Practicing how to load data, manage dataframes, and handle missing values.
* **Scikit-learn**: Learning how to split datasets, scale features, tune hyperparameters, and implement multiple classifiers.

## 📝 What I Have Done & Learned From This Project

### 1. Feature Engineering
* Extracted **Titles** (e.g., Mr., Mrs., Miss) from the raw `Name` text data to capture social status. 
* Grouped `SibSp` and `Parch` into a logical **FamilyGroup** (Alone, Small, Large) to resolve non-linear survival patterns.

### 2. Data Cleaning & Feature Scaling
* Handled missing values using Median for `Age` and Mode for `Embarked`.
* Applied **StandardScaler** to normalize feature ranges specifically for distance-based algorithms, ensuring all variables are evaluated equally.

### 3. Model 1: k-Nearest Neighbors (k-NN)
* Implemented the baseline **k-NN** algorithm.
* Optimized parameters via manual tuning and grid search using scaled features, achieving a stable local validation accuracy of **82.68%**.

### 4. Model 2: Random Forest Classifier
* Expanded the project by implementing a tree-based ensemble model (**Random Forest**), which natively handles data without requiring scaling.
* The baseline Random Forest model yielded **82.12%** validation accuracy.
* Further applied **GridSearchCV** with 5-fold Cross-Validation to optimize structural parameters (`max_depth`, `n_estimators`, etc.) to prevent overfitting, resulting in a more robust and generalized validation accuracy of **81.56%**.

### 5. Version Control & Repository Management
* Implemented a comprehensive `.gitignore` file to strictly exclude large data files and prediction outputs (`submission.csv`, `rf_submission.csv`) from being tracked, ensuring a clean and production-ready GitHub repository.

## 📈 Progress Log & Future Roadmap

* **Current Status**: The project successfully compares an optimized distance-based model (k-NN, 82.68%) against a robust tree-based ensemble model (Random Forest, 81.56%).
* **Next Steps for Study**:
  * Since both models have provided solid baselines, my next goal is to study advanced gradient boosting techniques, such as **XGBoost**, and experiment with deeper feature engineering on the `Ticket` and `Cabin` columns to push the prediction limits further!

---
*This project is a part of my early learning journey. If you have any suggestions or feedback, please feel free to share. I am always open to learning and improving!*