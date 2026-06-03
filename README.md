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
* **Scikit-learn**: Learning how to split datasets and implement built-in Machine Learning models.

## 📝 What I Have Done & Learned From This Project

### 1. Exploratory Data Analysis (EDA)
* Used Pandas to group data and uncover hidden trends, discovering that survival rates differ significantly based on **Sex**, **Ticket Class (Pclass)**, and **Port of Embarkation (Embarked)**. 

### 2. Feature Engineering 
* Successfully extracted **Titles** (e.g., Mr., Mrs., Miss) from the raw `Name` text data to capture social status. 
* Grouped `SibSp` and `Parch` into a logical **FamilyGroup** (Alone, Small, Large) after realizing that raw numerical sizes confused the model due to non-linear survival patterns.

### 3. Basic Data Management (Data Cleaning)
* Handled missing values by experimenting with filling missing `Age` values with the **Median** to prevent model errors.
* Filled missing `Embarked` data with the **Mode** and practiced encoding categorical text data into numerical values so that the model can process them mathematically.

### 4. Basic Modeling
* **Applying the Algorithm**: Implemented the **k-Nearest Neighbors (k-NN)** algorithm. Through iterative testing of engineered features, I successfully improved the model's predictive capabilities.

## 📈 Progress Log & Future Roadmap

* **Current Status**: The model is running successfully with advanced Feature Engineering implemented! It achieved a validation accuracy of **81.56%**.
* **Next Steps for Study**:
  * Explore Feature Scaling techniques to optimize distance-based algorithms like k-NN.
  * Explore Data Visualization libraries (like Matplotlib or Seaborn) to visually uncover more complex relationships within the data.

---
*This project is a part of my early learning journey. If you have any suggestions or feedback, please feel free to share. I am always open to learning and improving!*