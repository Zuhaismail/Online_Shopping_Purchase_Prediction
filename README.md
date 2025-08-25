# 🛒 Online Shoppers Purchase Intentions

## 📌 Project Overview

The goal of this project is to analyze **online shopper browsing behavior** and predict whether a user will complete a purchase during a session.
We use **Exploratory Data Analysis (EDA)** and a machine learning model (**XGBoost**) to extract insights and build an accurate predictive model.

This project is based on the **Online Shoppers Purchasing Intention Dataset** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Online+Shoppers+Purchasing+Intention+Dataset).

---

## 📂 Dataset

* **File name:** `online_shoppers_intention.csv`
* **Size:** 12,330 sessions, 18 features + 1 target (`Revenue`).
* **Target variable:**

  * `Revenue = True` → Purchase made
  * `Revenue = False` → No purchase

### Key Features

* **Administrative, Administrative\_Duration** → Visits & time on admin pages
* **Informational, Informational\_Duration** → Visits & time on info pages
* **ProductRelated, ProductRelated\_Duration** → Interaction with product pages
* **BounceRates, ExitRates** → Session behavior
* **PageValues** → Value assigned to visited pages
* **SpecialDay** → Closeness to special holidays
* **OperatingSystems, Browser, Region, TrafficType** → Technical info
* **VisitorType** → New/Returning/Other visitor
* **Weekend** → Session occurred on a weekend

---

## 🛠️ Project Workflow

### 1. Data Cleaning & Preprocessing

* Loaded and cleaned dataset
* Encoded categorical variables (`VisitorType`, `Weekend`, `Month`)
* Converted `Revenue` into binary target

### 2. Exploratory Data Analysis (EDA)

* Distribution plots of key features
* Correlation heatmap
* Comparison between purchase vs non-purchase sessions
* Insights into features like `PageValues`, `ExitRates`, and `VisitorType`

### 3. Modeling with XGBoost

* Train-test split
* Implemented **XGBoost Classifier**
* Hyperparameter tuning with `RandomizedSearchCV`
* Extracted **feature importance**

### 4. Model Evaluation

* Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC
* Confusion matrix 

### 5. Insights

* **Most influential features:** `PageValues`, `ExitRates`, `ProductRelated_Duration`
* Returning visitors and sessions close to special days have higher purchase rates
* Purchases are rare (\~15%), highlighting class imbalance

---

## 📊 Results

| Metric    | Score  |
| --------- | ------ |
| Accuracy  | \~89%  |
| Precision | \~76%  |
| Recall    | \~68%  |
| F1-Score  | \~72%  |
| ROC-AUC   | \~0.93 |

---

## 📌 Learning Outcomes

* Gained insights into how browsing behavior influences purchases
* Learned to apply **EDA** on real-world e-commerce data
* Trained and tuned **XGBoost** for classification
* Evaluated model with multiple metrics
* Identified **key features** driving online shopping purchases

---

## ✅ Conclusion

This project demonstrates how **browsing patterns strongly influence purchase decisions** in online shopping.

* Features like **PageValues**, **ExitRates**, and **Product-related interactions** are the most reliable predictors of conversion.
* Returning visitors and sessions closer to **special days/holidays** show higher purchase intent.
* XGBoost model achieved a strong **ROC-AUC of \~0.93**, making it suitable for real-world applications such as:

  * Customer targeting
  * Personalized recommendations
  * Marketing campaign optimization

Overall, this project highlights the power of **data-driven insights** in e-commerce, where businesses can increase conversions by focusing on **high-value sessions and key behavioral signals**.

