# 🛠️ Predictive Maintenance of Jet Engines using Machine Learning

This project focuses on early fault detection and **Remaining Useful Life (RUL)** classification for aerospace jet engines using NASA’s **C-MAPSS dataset**. We trained multiple machine learning models to predict engine failure conditions in advance — enabling efficient **predictive maintenance**.

---

## 📊 Goal

To classify jet engine states as either:
- ✅ **Healthy**
- ❌ **Failing**

…using real-time sensor data from simulated engine run-to-failure cycles.

---

## 🧪 Dataset

We used the FD001–FD004 datasets from the **C-MAPSS (Commercial Modular Aero-Propulsion System Simulation)** dataset provided by NASA.

- Simulated sensor data for engines running until failure
- Multivariate time-series with sensor readings and operational settings
- Labeled for binary classification of **health vs failure**

---

## 🧠 Models Trained

| Model           | Description                            |
|----------------|----------------------------------------|
| Random Forest  | Ensemble method using decision trees    |
| XGBoost        | Optimized gradient boosting framework   |
| CatBoost       | **Best performer** – final model chosen |

---

## ✅ Model Performance (AUC Score)

CatBoost delivered the highest classification performance across all test sets.

![Model Comparison](model_auc_comparison_updated.png)

---

## 🏆 Final Model: CatBoost

- Applied `StandardScaler` to normalize features
- Used `SMOTE` to balance the binary class labels
- Tuned hyperparameters using `GridSearchCV`
- Performed explainability analysis with **SHAP values**

---

## 🧠 SHAP Feature Importance (Example)

![SHAP Example](shap_example.png) <!-- Replace with actual SHAP summary plot -->

Key sensors such as `sensor_11`, `sensor_6`, and `sensor_9` were most influential in predicting engine failures.

---

## 🧰 Technologies Used

- Python
- NumPy, Pandas, Scikit-learn
- CatBoost, XGBoost, Random Forest
- SHAP (Model Explainability)
- Matplotlib
- Google Colab / Jupyter Notebooks



---

## 📌 Key Takeaways

- **CatBoost** offered superior predictive power and interpretability.
- Preprocessing (scaling, class balancing) significantly boosted results.
- SHAP made the black-box model transparent and explainable.

---

## 🤝 Contributions

Made by Nishmi Ranathunge.  
Feel free to open issues or submit pull requests!





