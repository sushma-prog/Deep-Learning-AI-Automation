---

# 🚢 Titanic Survival Prediction using H2O AutoML

This project applies **H2O.ai AutoML** to the famous **Titanic dataset** to predict passenger survival.
It automates the process of trying multiple machine learning models and selecting the best-performing one.

---

## 📊 Dataset

* **Source**: Titanic dataset (Kaggle / Seaborn’s Titanic version)
* **Target Column**: `survived` (0 = did not survive, 1 = survived)
* **Features Used**:

  * Age, Sex, Passenger Class, Fare, Siblings/Spouses, Parents/Children, Deck, Embarked, etc.

---

## ⚙️ Methodology

1. **Data Preprocessing**

   * Converted categorical variables into factors for H2O.
   * Dropped leakage columns like `alive` (since it’s basically the same as target).
   * Split data into **train (80%)** and **test (20%)**.

2. **AutoML Training**

   * Used `H2OAutoML` with a runtime budget of 20–60 seconds.
   * Trained multiple algorithms:

     * Gradient Boosting (GBM)
     * Random Forest (DRF)
     * XGBoost
     * GLM
     * Stacked Ensembles

3. **Evaluation**

   * Evaluated models on **AUC, Accuracy, LogLoss**.
   * Selected the **leader model** for testing.

---

## 🏆 AutoML Leaderboard (Top 5 Models)

| Rank | Model                            | AUC   | LogLoss | Accuracy (approx) |
| ---- | -------------------------------- | ----- | ------- | ----------------- |
| 1    | **GBM\_3\_AutoML**               | 0.875 | 0.407   | \~83–84%          |
| 2    | StackedEnsemble\_AllModels\_1    | 0.875 | 0.404   | \~83%             |
| 3    | GBM\_4\_AutoML                   | 0.875 | 0.408   | \~83%             |
| 4    | StackedEnsemble\_BestOfFamily\_2 | 0.873 | 0.408   | \~82–83%          |
| 5    | XGBoost\_2\_AutoML               | 0.870 | 0.417   | \~82%             |

---

## 🔍 Results on Test Data

* **Best Model**: `GBM_3_AutoML`
* **AUC**: **0.967**
* **Accuracy**: \~90%
* **Confusion Matrix**:

```
Confusion Matrix (Act/Pred) for max f1 @ threshold = 0.48
      0    1   Error  Rate
0   106    5   0.045  (5.0/111.0)
1    12   64   0.157  (12.0/76.0)
Total 118   69   0.099  (17.0/187.0)
```

✅ The model correctly predicts \~90% of cases, with a strong AUC score.

---

## 📈 Feature Importance (GBM Model)

Top predictors for survival:

* `adult_male`
* `fare`
* `age`
* `pclass`
* `who`

📌 Interpretation:

* Being an **adult male** reduced chances of survival.
* **Higher fare (wealth)** and **younger age** increased survival chances.
* **Class (1st, 2nd, 3rd)** was also an important factor.

---

## 📂 Files in Repository

* `AutoML_Tools.ipynb` → Full notebook with code & outputs
* `leaderboard.csv` → AutoML leaderboard results
* `feature_importance.csv` → Feature importance values
* `README.md` → Project documentation

---

## 🚀 Conclusion

* AutoML quickly found **highly accurate models** for Titanic survival.
* The best model achieved **AUC \~0.95 and Accuracy \~90%** on test data.
* **GBM + Stacked Ensembles** performed the best.
* Feature analysis confirmed well-known Titanic insights: women, children, and higher-class passengers had higher survival chances.

---

✨ Author: **Sushma Sandanshiv**
🔗 GitHub: [sushma-prog](https://github.com/sushma-prog)

---
