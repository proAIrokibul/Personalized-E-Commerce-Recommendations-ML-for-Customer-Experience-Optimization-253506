# Personalized-E-Commerce-Recommendations-ML-for-Customer-Experience-Optimization-253506
## 🛍️ Project Overview
This project aims to develop a **Personalized Recommendation System** for an e-commerce platform using machine learning techniques. By analyzing customer profiles, product features, and behavioral trends, the system predicts whether a product is likely to be recommended by a customer. This enhances customer experience, improves engagement, and ultimately drives revenue.

---

## 💡 Objectives
- Understand customer behavior and product trends through visual analytics.
- Preprocess and engineer data for predictive modeling.
- Build and compare multiple classification models.
- Deliver business insights and deployable logic for personalization.

---

## 📂 Datasets Used
Two datasets were used for this project:

### 🔹 Customer Dataset
| Feature | Description |
|--------|-------------|
| `Customer_ID` | Unique ID for each customer |
| `Age`, `Gender`, `Location` | Demographics |
| `Browsing_History`, `Purchase_History` | Behavioral features |
| `Customer_Segment`, `Avg_Order_Value` | Segment & value info |
| `Holiday`, `Season` | Temporal context |

### 🔹 Product Dataset (Main)
| Feature | Description |
|--------|-------------|
| `Product_ID`, `Category`, `Subcategory`, `Brand` | Product descriptors |
| `Price`, `Product_Rating`, `Average_Rating_of_Similar_Products` | Pricing and performance |
| `Customer_Review_Sentiment_Score` | Sentiment score extracted from text |
| `Holiday`, `Season`, `Geographical_Location` | Contextual metadata |
| `Probability_of_Recommendation` | Target variable for modeling |

---

## ⚙️ Methodology

### 🔎 Exploratory Data Analysis (EDA)
- Comprehensive visual analysis using **Seaborn** and **Matplotlib**.
- Trends identified in purchase behavior by age, gender, location, product categories, and time (holiday/season).
- Product-level insights including top brands, categories by sentiment, and pricing analysis.

### 🧼 Data Preprocessing
- Removal of irrelevant and null columns (e.g., `Unnamed: 13`, `Unnamed: 14`)
- Categorical encoding:
  - Label Encoding (`Holiday`)
  - One-Hot Encoding (`Category`, `Brand`, etc.)
- Scaling of numerical features using Min-Max Scaler
- Created a binary classification target: `Recommended = 1` if `Probability_of_Recommendation >= 0.5`

---

## 🧠 Model Building and Evaluation

Three classification algorithms were applied:

### 1. 🔹 Logistic Regression
```
Accuracy: 55.20%

Classification Report:
              precision    recall  f1-score   support
           0       0.35      0.03      0.05       876
           1       0.56      0.96      0.71      1124
    accuracy                           0.55      2000
   macro avg       0.46      0.49      0.38      2000
weighted avg       0.47      0.55      0.42      2000
```

---

### 2. 🌲 Random Forest Classifier
```
Accuracy: 53.55%

Classification Report:
              precision    recall  f1-score   support
           0       0.45      0.29      0.35       876
           1       0.57      0.73      0.64      1124
    accuracy                           0.54      2000
   macro avg       0.51      0.51      0.50      2000
weighted avg       0.52      0.54      0.51      2000
```

---

### 3. ⚙️ Support Vector Machine (SVM)
```
Accuracy: 55.65%

Classification Report:
              precision    recall  f1-score   support
           0       0.47      0.11      0.17       876
           1       0.57      0.91      0.70      1124
    accuracy                           0.56      2000
   macro avg       0.52      0.51      0.43      2000
weighted avg       0.52      0.56      0.47      2000
```

### 📊 Model Comparison Histogram
A visual bar chart was generated to compare model accuracies:
- Logistic Regression: **55.2%**
- Random Forest: **53.55%**
- SVM: **55.65%**

The SVM model performed slightly better overall, but all models show potential for improvement through tuning and feature engineering.

---

## 📈 Business Impact

This system demonstrates the **tangible benefits of intelligent personalization in e-commerce**:

| Impact Area | Business Benefit |
|-------------|------------------|
| 🎯 Targeted Marketing | Improve product discovery and user engagement through personalized recommendations |
| 📈 Higher Conversion | Likely-to-recommend products improve chances of purchase |
| 🛍️ Average Order Value | Recommending complementary or highly rated products boosts cart size |
| 🔁 Customer Retention | Users feel understood and are more likely to return to a personalized experience |
| 📉 Reduced Churn | Identifying non-engaged segments allows for intervention campaigns |

---


