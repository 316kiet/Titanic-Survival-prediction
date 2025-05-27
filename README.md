# 🚢 Titanic Survival Prediction

This project builds a *machine learning model* to predict which passengers survived the Titanic disaster using data from [Kaggle's Titanic competition](https://www.kaggle.com/c/titanic).

## 📌 Problem Statement

Given passenger details such as age, sex, ticket class, etc., predict whether a passenger survived (1) or not (0).  
This is a *binary classification problem*.

---

## 💡 Project Goals

- Load and clean the Titanic dataset
- Apply label encoding to convert categorical variables
- Train a *Naive Bayes* classification model
- Optionally train a *Random Forest* model for comparison
- Evaluate model performance with accuracy and confusion matrix
- Predict outcomes on the test set and generate a CSV file for Kaggle submission

---

## 📁 Dataset

- *train.csv* – contains labeled data (used to train the model)
- *test.csv* – contains data for which survival needs to be predicted

You can download the dataset from [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic/data).

---

## 📦 Libraries Used

- pandas – for data manipulation
- numpy – for numerical operations
- sklearn – for machine learning algorithms and metrics
- seaborn & matplotlib – for visualizations

---

## 🧹 Data Preprocessing

- Dropped columns: Name, Ticket, Cabin, PassengerId
- Filled missing values in:
  - Age with median
  - Embarked with mode
  - Fare (in test set) with median
- Converted Sex and Embarked to numeric using *Label Encoding*

---

## 🤖 Models Used

### 1. Naive Bayes Classifier
- Based on probability theory assuming feature independence.
- Trained on 80% of the data and validated on 20%.
- Fast and interpretable for small datasets.

### 2. Random Forest (Optional)
- Ensemble method using multiple decision trees.
- Used to compare performance and view *feature importances*.

---

## 📊 Evaluation Metrics

- *Accuracy Score*
- *Classification Report*
- *Confusion Matrix* Heatmap

---

## 📈 Visualizations

- Confusion Matrix (for both models)
- Feature Importance bar plot (for Random Forest)

---

## 📝 Submission

Generates a CSV file for Kaggle submission:

```csv
PassengerId,Survived
892,0
893,1
...
