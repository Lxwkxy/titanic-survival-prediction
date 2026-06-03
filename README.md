# 🚢 Titanic Survival Prediction

Hello! This project serves as a learning space for my very first step into Data Science. I am using the classic Titanic dataset from Kaggle to practice writing code and predict the survival opportunities of passengers.

The primary goal of this project is to practice using fundamental libraries and to understand the thought process behind basic data manipulation and preparation.

## 📂 Project Directory Structure

<blockquote>
titanic_project/<br>
│<br>
├── data/<br>
│   ├── train.csv         # Training dataset used to train the model<br>
│   └── test.csv          # Testing dataset for making predictions<br>
│<br>
├── notebooks/<br>
│   └── titanic.ipynb     # Main Jupyter Notebook for analysis and modeling<br>
│<br>
└── README.md             # Project overview and documentation
</blockquote>

## 🛠️ Tools & Libraries I am Practicing

* **Python**: Applying programming concepts to build data processing and Machine Learning pipelines.
* **Pandas**: Practicing how to load data, manage dataframes, and handle missing values.
* **Scikit-learn**: Learning how to split datasets, scale features, and tune Machine Learning models.

## 📝 What I Have Done & Learned From This Project

### 1. Exploratory Data Analysis (EDA) & Feature Engineering
* Uncovered hidden trends showing that survival rates differ significantly based on **Sex** and **Ticket Class (Pclass)**.
* Extracted **Titles** (e.g., Mr., Mrs., Miss) from the raw `Name` text data to capture social status. 
* Grouped `SibSp` and `Parch` into a logical **FamilyGroup** (Alone, Small, Large) to resolve non-linear survival patterns.

### 2. Data Cleaning & Feature Scaling
* Handled missing values using Median for `Age` and Mode for `Embarked`.
* Applied **StandardScaler** to normalize feature ranges, allowing distance-based algorithms to evaluate all variables equally.

### 3. Model Training & Hyperparameter Tuning
* Implemented the **k-Nearest Neighbors (k-NN)** algorithm. 
* Learned that combining Feature Scaling with **Hyperparameter Tuning** (adjusting `n_neighbors` from 5 to 9) smoothed out data noise, leading to a significant accuracy boost!

## 📈 Progress Log & Future Roadmap

* **Current Status**: The model is highly optimized with Feature Engineering, Scaling, and Tuning! It achieved an impressive validation accuracy of **82.68%**.
* **Next Steps for Study**:
  * Explore Data Visualization libraries (like Matplotlib or Seaborn) to visually present the findings.

---
*This project is a part of my early learning journey. If you have any suggestions or feedback, please feel free to share. I am always open to learning and improving!*