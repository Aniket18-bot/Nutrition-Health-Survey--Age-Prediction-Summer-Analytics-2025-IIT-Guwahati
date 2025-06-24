
# Nutrition Health Survey - Age Group Prediction

**Summer Analytics 2025, IIT Guwahati**

This project is part of **Summer Analytics 2025**, organized by the **Consulting and Analytics Club, IIT Guwahati**. The challenge focuses on using machine learning to predict age groups (Adult / Senior) based on health and nutrition survey data from the **National Health and Nutrition Examination Survey (NHANES)**.

---

### About the Dataset

NHANES is a nationally representative health study conducted by the **CDC’s National Center for Health Statistics**. It combines interviews, physical exams, and lab tests to assess the health and nutritional status of U.S. residents.

For this challenge:

- **Train Data**: 2,016 rows with labels (age_group)
- **Test Data**: 312 rows without labels (to predict)

⚠️ **Target Classes**

- `0` → **Adult** (below 65 years)
- `1` → **Senior** (65 years and above)

📌 **Features**

| Feature  | Description                           |
| -------- | ------------------------------------- |
| SEQN     | Unique ID                             |
| RIAGENDR | Gender (1 = Male, 2 = Female)         |
| PAQ605   | Engages in sports/fitness activities? |
| BMXBMI   | Body Mass Index                       |
| LBXGLU   | Glucose level                         |
| DIQ010   | Diabetes status                       |
| LBXGLT   | Glucose tolerance                     |
| LBXIN    | Insulin level                         |

✅ **Missing values**: The dataset contains NaNs that are handled through median/mode imputation.

---

### Objective

Create a machine learning model that predicts whether a person is **Adult (0)** or **Senior (1)** using provided health indicators.The model outputs predictions in this format:

```
age_group
0
0
1
...
```

for each row of the test set.

---

### Project Structure

| File                | Description                                           |
| ------------------- | ----------------------------------------------------- |
| `Train_Data.csv`    | Training dataset                                      |
| `Test_Data.csv`     | Test dataset                                          |
| `Nutrition 1.ipynb` | Baseline model with ensemble classifiers              |
| `Nutrition 2.ipynb` | Model with improved missing value handling and tuning |
| `Nutrition 3.ipynb` | Advanced ensemble + feature engineering               |
| `submission.csv`    | Example output file                                   |

---

### Models Used

✅ **Random Forest Classifier**✅ **LightGBM Classifier**✅ **XGBoost Classifier**✅ **Ensemble Voting (majority rule)**

Each notebook builds models, evaluates accuracy, and generates test predictions.

---

### Evaluation

Models were evaluated using:

- **Accuracy**
- **Classification report (precision, recall, f1-score)**

Ensemble predictions aimed to balance performance across Adult and Senior categories, though Seniors being the minority class posed additional challenges.

---

### Notes

- Models can be further improved through hyperparameter tuning, advanced feature engineering, or SMOTE/oversampling techniques to address class imbalance.
- The code follows clean practices, with missing values handled carefully for both train and test data.

---

### Acknowledgment

- Dataset: [CDC NHANES](https://www.cdc.gov/nchs/nhanes/index.htm)
- Hackathon: **Summer Analytics 2025, Consulting and Analytics Club, IIT Guwahati**

⚠️ **Disclaimer**: We do not own the data. This dataset has been pre-processed for educational purposes only.

👉 **Feel free to use this repo for learning, and contribute improvements!**
