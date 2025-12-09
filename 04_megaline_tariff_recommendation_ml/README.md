# Megaline - Tariff Recommendation (Machine Learning Classification)

This project develops a machine learning model to help the mobile carrier **Megaline** recommend the best tariff plan - **Smart** or **Ultra** — based on user behavior.

> *Completed as part of the TripleTen Data Analysis Bootcamp.*

---

## 🚀 Project Summary

- Built a classification model predicting whether a user should choose **Smart** or **Ultra**.
- Tested Logistic Regression, Decision Tree, and Random Forest.
- **Final accuracy: 0.8165 on the test set (≥ 0.75 target)**.
- Best model: **Random Forest (n_estimators=100, max_depth=12)**.
- The model generalizes well and can be recommended for deployment.

---

## 📘 Dataset

3,214 rows of monthly user behavior:

| Feature | Description |
|--------|-------------|
| calls | Number of calls |
| minutes | Total call duration |
| messages | Number of SMS |
| mb_used | Internet traffic (MB) |
| is_ultra | Target: 1 = Ultra, 0 = Smart |

No missing values, no duplicates. Target moderately imbalanced (69% Smart / 31% Ultra).

---

## 🧪 Model Training & Evaluation

Three models were trained and compared:

| Model | Validation Accuracy | Notes |
|-------|---------------------|-------|
| Logistic Regression | 0.7558 | Baseline; meets threshold |
| Decision Tree | 0.8165 | Performs well with max_depth=5 |
| **Random Forest** | **0.8243** | **Best model** |

### Final Testing
| Dataset | Accuracy |
|---------|----------|
| Validation | 0.8243 |
| Test | 0.8165 |

---

## 📝 Conclusions

- Random Forest demonstrated the best accuracy and stability.
- Logistic Regression is acceptable but inferior.
- Decision Tree performs well but less robust.
- The final model satisfies project requirements and predicts user tariff reliably.

---

## 📁 Project Structure

04_megaline_tariff_recommendation_ml/  
│── README.md  
│── megaline_tariff_ml.ipynb

---

## 💡 What I Learned
This project strengthened my understanding of:
- stratified train/validation/test splitting,
- comparing baseline and tree-based models,
- evaluating model performance using accuracy,
- selecting the best model based on validation results.
