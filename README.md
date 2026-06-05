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
├── submission.csv        # Final k-NN predictions (Ignored in Git)<br>
├── rf_submission.csv     # Final Random Forest predictions (Ignored in Git)<br>
├── xgb_submission.csv    # Final XGBoost predictions (Ignored in Git)<br>
└── voting_submission.csv # Final Ensemble Voting predictions (Ignored in Git)
</blockquote>

## 🛠️ Tools & Libraries I am Practicing

* **Python**: Applying programming concepts to build data processing and Machine Learning pipelines.
* **Pandas & NumPy**: Practicing how to load data, manage dataframes, and handle missing values.
* **Scikit-learn & XGBoost**: Learning how to split datasets, scale features, tune hyperparameters, and implement multiple classifiers.

## 📝 What I Have Done & Learned From This Project

### 1. Data Cleaning & Feature Engineering
* Extracted **Titles** (e.g., Mr., Mrs., Miss) from the raw `Name` text data to capture social status. 
* Grouped `SibSp` and `Parch` into a logical **FamilyGroup** (Alone, Small, Large) to resolve non-linear survival patterns.
* Handled missing values using Median for `Age` and Mode for `Embarked`.
* Applied **StandardScaler** to normalize feature ranges specifically for distance-based algorithms.

### 2. Advanced Feature Enrichment from String Data
* **Deck Extraction:** Filled massive missing values in `Cabin` with 'U' (Unknown) and extracted the first letter to represent the physical deck level on the ship.
* **Ticket Frequency:** Counted identical `Ticket` numbers to identify hidden group sizes that weren't captured by explicit family relationships.

### 3. Model 1: k-Nearest Neighbors (k-NN)
* Implemented the baseline **k-NN** algorithm using strictly scaled features.
* Optimized parameters via **GridSearchCV** with 5-fold CV, achieving a stable validation accuracy of **82.68%**.

### 4. Model 2: Random Forest Classifier
* Expanded to a tree-based ensemble model, bypassing the need for feature scaling.
* Optimized structural parameters (`max_depth`, `n_estimators`) via **GridSearchCV** to prevent overfitting, resulting in a validation accuracy of **81.56%**.
* **Kaggle Public Score:** **0.77990**

### 5. Model 3: XGBoost Classifier (Extreme Gradient Boosting)
* Implemented an advanced gradient boosting algorithm using the newly enriched string features.
* Applied **GridSearchCV** to control the learning rate, depth, and subsampling. The tuned validation accuracy stabilized at **82.68%**.
* **Kaggle Public Score:** **0.76794**
* *Key Learning:* A crucial realization that highly complex models (like XGBoost) can sometimes overfit on very small datasets (like Titanic) compared to simpler ensemble methods like Random Forest, proving that "more complex is not always better."

### 6. The Ultimate Ensemble: Hard Voting Classifier
* Implemented a Hard Voting mechanism to democratically combine the predictions of k-NN, Random Forest, and XGBoost.
* Applied a Pipeline to automatically handle feature scaling specifically for the k-NN model while allowing tree-based models to use unscaled data.
* **Kaggle Public Score:** **0.77990**
* *Key Learning:* The ensemble score matched the Random Forest baseline perfectly. This demonstrates the concept of 'Highly Correlated Predictions', where highly capable models (like RF and XGBoost) often make similar errors on the same hard-to-predict instances. While the score didn't increase, the ensemble provides a more stable and generalized prediction system.

---
*This project is a part of my early learning journey. If you have any suggestions or feedback, please feel free to share. I am always open to learning and improving!*