# Cross-Platform Review Sentiment & Fake Review Detection  
### MSc Data Science – University of Hertfordshire  

## 📌 Project Overview  
This project performs sentiment classification and fake review detection using customer reviews from **Amazon** and **Flipkart**.  
The goal is to identify whether a review expresses **Negative, Neutral, or Positive** sentiment using machine learning models trained on TF-IDF text features.

This work was completed as part of the MSc Data Science Final Project.

---

## 🎯 Research Questions  
1. Which e-commerce platform (Amazon or Flipkart) receives more positive or negative reviews?  
2. Can machine learning accurately classify the sentiment of customer reviews?  
3. Which model performs best for text-classification: Logistic Regression or SVM?  
4. How does class imbalance (Positive vs Negative vs Neutral) affect model accuracy?

---

## 🗂 Dataset  
Two publicly available datasets from Kaggle were used:

### **Amazon Product Reviews Dataset**  
Source: *Kaggle (2024)*  
🔗 https://www.kaggle.com  
Contains: review text, rating, helpfulness, summary, timestamp.

### **Flipkart Product Reviews Dataset**  
Source: *Kaggle (2024)*  
🔗 https://www.kaggle.com  
Contains: product name, price, rating, summary, review text, sentiment label.

### ⚠ Ethical Notes  
- All datasets used are **public**.  
- No personal identifiable information (PII) is included.  
- All reviews are **anonymized**.  
- License allows academic use.  
- Data stored securely during the project.

---

## 🧹 Data Cleaning & Preprocessing  
### Steps performed:
- Removed duplicates  
- Removed missing values  
- Cleaned text (lowercase, punctuation removal, stopwords removal)  
- Normalized Amazon ratings into sentiment labels  
- TF-IDF vectorization (1–2 gram features)

---

## 📊 Exploratory Data Analysis  
EDA includes:
- Rating distribution by platform  
- Sentiment label distribution  
- Review length distribution  
- WordClouds for Amazon & Flipkart  
- Platform comparison visualizations

Plots are available in the `plots/` folder.

---

## 🤖 Machine Learning Models  
Two models were implemented:

### **1️⃣ Logistic Regression (Baseline)**  
- Fast to train  
- Good baseline for text classification  
- Accuracy: **87.0%**

---

### **2️⃣ Support Vector Machine (SVM)**  
- Best performing model  
- Tuned using GridSearchCV  
- Best Parameter: `C = 1`  
- Accuracy: **86.4%**  
- Strong performance on Positive class  
- Struggles with Neutral due to class imbalance  

Confusion matrix and classification reports included in the `plots/` folder.

---

## 🔧 Hyperparameter Tuning  
Performed using **GridSearchCV**:  
- Explored different C values  
- Improved macro F1 score  
- Helped reduce overfitting

---

## 📈 Model Comparison  
| Model | Accuracy |
|-------|----------|
| Logistic Regression | 0.870 |
| Tuned SVM | 0.864 |

Logistic Regression slightly outperformed SVM due to handling class imbalance better.

---

## 🧾 Conclusion  
- TF-IDF + ML models can effectively classify e-commerce reviews.  
- Logistic Regression performed slightly better overall.  
- SVM provided stronger decision boundaries but suffered from data imbalance.  
- Amazon had more reviews and more positive sentiment compared to Flipkart.

---

## 🚀 Future Work  
- Train advanced models (Random Forest, XGBoost, BERT)  
- Use SMOTE or re-sampling to balance Neutral class  
- Expand dataset for more categories  
- Build an API for real-time sentiment prediction  

---

## 🙏 Acknowledgements  
I would like to thank my project supervisor **Mr. Darshan** for his guidance and support throughout this project.

