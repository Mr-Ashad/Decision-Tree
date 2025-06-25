# Decision-Tree and Random Forest

This project uses **Decision Tree** and **Random Forest** classifiers to predict survival outcomes of Titanic passengers using scikit-learn.

---

## 📁 Dataset

- **Source:** `train.csv` (Kaggle Titanic dataset)
- **Target:** `Survived` (0 = No, 1 = Yes)
- **Features used:** `Sex`, `Age`, `SibSp`, `Parch`, `Fare_log`, `Embarked`, `Pclass`

---

##  Preprocessing

- Imputed missing `Age` using median grouped by `Pclass` & `Sex`
- Filled missing `Embarked` with mode
- Converted `Sex` to numeric (male: 1, female: 0)
- One-hot encoded `Embarked` and `Pclass` (dropped first category to avoid multicollinearity)
- Log-transformed `Fare` → `Fare_log`
- Dropped: `PassengerId`, `Name`, `Ticket`, `Fare`, `Cabin`

---

##  Models

| Model            | Train Acc | Test Acc | 
|------------------|-----------|----------|
| Decision Tree    | 0.85      | 0.82    |
| Random Forest    | 0.85      | 0.82     | 


---

##  Evaluation

- **Metrics:** Accuracy, Classification Report, Confusion Matrix
- **Feature Importance:** Visualized using horizontal bar plots
- **Tuning:** GridSearchCV used for Random Forest hyperparameters

---

##  Libraries

- `pandas`, `numpy`, `matplotlib`
- `sklearn`: models, metrics, preprocessing

---


