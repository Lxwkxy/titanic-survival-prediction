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

### 1. Basic Data Management (Data Cleaning)
* Learned how to check for missing values and experimented with filling missing `Age` values with the **Median** to prevent model errors.
* Practiced encoding categorical text data like `Sex` (male/female) and `Embarked` into numerical values so that the model can process them mathematically.

### 2. Basic Modeling
* **Applying the Algorithm**: Since I have previously studied the concepts of the **k-Nearest Neighbors (k-NN)** algorithm, I wanted to apply that knowledge to a real-world classification problem in this project. This allows me to observe the predictions firsthand and better understand the model's practical implementation.

## 📈 Progress Log & Future Roadmap

* **Current Status**: The baseline model is successfully running! It achieved an accuracy of approximately 80.45% on the validation set.
* **Next Steps for Study**:
  * Explore Data Visualization libraries (like Matplotlib or Seaborn) to better see the relationships within the data.
  * Practice Feature Engineering to transform data for better model performance.

---
*This project is a part of my early learning journey. If you have any suggestions or feedback, please feel free to share. I am always open to learning and improving!*