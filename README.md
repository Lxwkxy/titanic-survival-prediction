# 🚢 Titanic Survival Prediction

Hello! This project serves as a learning space for my very first step into Data Science. I am using the classic Titanic dataset from Kaggle to practice writing code and predict the survival opportunities of passengers.

The primary goal of this project is to practice using fundamental libraries and to understand the thought process behind basic data manipulation, preparation, and the end-to-end Machine Learning pipeline.

## 📂 Project Directory Structure

<blockquote>
titanic_project/<br>
│<br>
├── data/                 # Training and testing datasets (Ignored in Git)<br>
│<br>
├── notebooks/<br>
│   └── titanic.ipynb     # Main Jupyter Notebook for data processing and modeling<br>
│<br>
├── .gitignore            # Git configuration to exclude data and output files<br>
├── README.md             # Project overview and documentation<br>
└── submission.csv        # Final predictions formatted for Kaggle (Ignored in Git)
</blockquote>

## 🛠️ Tools & Libraries I am Practicing

* **Python**: Applying programming concepts to build data processing and Machine Learning pipelines.
* **Pandas & NumPy**: Practicing how to load data, manage dataframes, and handle missing values.
* **Scikit-learn**: Learning how to split datasets, scale features, tune models, and apply Cross-Validation.

## 📝 What I Have Done & Learned From This Project

### 1. Feature Engineering
* Extracted **Titles** (e.g., Mr., Mrs., Miss) from the raw `Name` text data to capture social status. 
* Grouped `SibSp` and `Parch` into a logical **FamilyGroup** (Alone, Small, Large) to resolve non-linear survival patterns.

### 2. Data Cleaning & Feature Scaling
* Handled missing values using Median for `Age` and Mode for `Embarked`.
* Applied **StandardScaler** to normalize feature ranges, allowing distance-based algorithms to evaluate all variables equally.

### 3. Model Training & Hyperparameter Tuning (GridSearchCV)
* Implemented the **k-Nearest Neighbors (k-NN)** algorithm. 
* Upgraded the model using **GridSearchCV** to test multiple parameter combinations with 5-fold Cross-Validation. This prevented data leakage and provided a robust, stable Validation Accuracy of **82.68%**.

### 4. Final Submission & Version Control
* Refactored the notebook into a clean ML pipeline and generated the final `submission.csv` to submit to Kaggle.
* Learned how to use `.gitignore` to keep raw data and output files out of the GitHub repository, maintaining a clean and professional codebase.

## 📈 Progress Log & Future Roadmap

* **Current Status**: The project is successfully completed end-to-end! The optimized k-NN model achieved a stable local validation accuracy of **82.68%**.
* **Next Steps for Study**:
  * Since k-NN has reached its performance limit on this dataset, my next goal is to study and implement Tree-based models (like **Random Forest** or **XGBoost**) to see how much further I can push the prediction accuracy!

---
*This project is a part of my early learning journey. If you have any suggestions or feedback, please feel free to share. I am always open to learning and improving!*