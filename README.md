# 🎓 Admission Chance Prediction  

---

## 📌 Project Overview  
This project predicts the **chance of admission for graduate programs** based on students’ academic and exam profiles.  
The dataset includes factors like GRE, TOEFL, university rating, SOP, LOR, CGPA, and research experience.  

We tested multiple regression models to see which one predicts admission chances most accurately.  

---

## 📂 Dataset  
📊 **Dataset Link:** [Graduate Admissions Dataset](https://www.kaggle.com/datasets/mohansacharya/graduate-admissions)  

- Shape → **(400, 8)**  
- Clean dataset → No duplicates  
- Dropped unnecessary columns  
- Train-test split: **80:20**  

---

## ⚙️ Tech Stack & Libraries  
- **Python** 🐍  
- **NumPy, Pandas** → Data handling  
- **Scikit-learn** → ML models, RandomizedSearchCV  
- **Matplotlib / Seaborn** → Visualization  

---

## 🚀 Models & Results  

| Model                     | R² Score | Notes |
|----------------------------|----------|-------|
| 🌲 Random Forest           | **0.81** | Strong baseline |
| Random Forest (RSCV)      | 0.75     | Drop after tuning (random nature) |
| ⚡ AdaBoost                | 0.802    | Good performance |
| AdaBoost (RSCV)           | 0.73     | Dropped after tuning |
| 🌱 Gradient Boosting       | 0.73     | Underperformed |
| 📈 Linear Regression       | **0.82** ✅ | Best overall |
| Ridge Regression          | 0.82     | Same as LR |
| Lasso Regression          | 0.21 ❌  | Performed very poorly |
| 🤝 K-Nearest Neighbors     | 0.71     | Moderate |
| 🌳 Decision Tree           | 0.67     | Weakest |

---

## 💡 Key Insights  
- **Linear Regression (0.82)** was the **best model**, showing the dataset is strongly linear in nature.  
- **Random Forest & AdaBoost** gave competitive results but not better than LR.  
- **Lasso collapsed (0.21)**, showing it over-penalized coefficients.  
- **Decision Trees** didn’t generalize well, confirming weak non-linear relationships.  
- Ridge Regression confirmed that regularization didn’t provide extra benefits over Linear Regression.  

---

## 🎯 Conclusion  
Simple models worked best here.  
- **Linear Regression & Ridge Regression** → Best and most reliable predictors.  
- Ensemble models like **Random Forest & AdaBoost** performed decently but were less consistent after hyperparameter tuning.  
- Lasso and Decision Trees showed significant underperformance.  

This project highlights that **not every dataset needs complex models — sometimes linear methods are the best fit.** ✅  

---
