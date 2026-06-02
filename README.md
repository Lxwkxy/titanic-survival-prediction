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
* Used Pandas to group data and uncover hidden trends, discovering that survival rates differ significantly based on **Sex**, **Ticket Class (Pclass)**, and **Port of Embarkation (Embarked)**. This analytical step guided my feature selection process.

### 2. Feature Engineering 
* Successfully extracted **Titles** (e.g., Mr., Mrs., Miss, Master) from the raw `Name` text data to capture the social status and gender/age hints of the passengers. 
* Grouped rare titles together and encoded them into numerical values, transforming complex string data into a powerful new feature for the model.

### 3. Basic Data Management (Data Cleaning)
* Learned how to check for missing values and experimented with filling missing `Age` values with the **Median** to prevent model errors.
* Filled missing `Embarked` data with the **Mode** and practiced encoding categorical text data into numerical values (0, 1, 2) so that the model can process them mathematically.

### 4. Basic Modeling
* **Applying the Algorithm**: Since I have previously studied the concepts of the **k-Nearest Neighbors (k-NN)** algorithm, I applied that knowledge to a real-world classification problem. By adding the newly engineered `Title` feature, I observed how feature extraction directly impacts and improves model prediction.

## 📈 Progress Log & Future Roadmap

* **Current Status**: The model is successfully running with Feature Engineering implemented! It achieved an accuracy of approximately **81.56%** on the validation set. *(Note: This score is being actively improved)*
* **Next Steps for Study**:
  * Practice creating `FamilySize` by combining `SibSp` and `Parch` columns.
  * Explore Data Visualization libraries (like Matplotlib or Seaborn) to better see the relationships within the data.

---
*This project is a part of my early learning journey. If you have any suggestions or feedback, please feel free to share. I am always open to learning and improving!*