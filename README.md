<p align="center">
  <img src="banner.png" alt="Project Banner" width="100%">
</p>

# 🏝️ Airbnb Price Prediction & Sentiment Analysis – Honolulu, Hawaii

This project analyzes Airbnb listings and guest reviews in Honolulu to build a predictive pricing model and extract sentiment-driven insights from customer feedback. Combining structured data with advanced NLP techniques, the model supports hosts in dynamic pricing and experience optimization.

---

## 🔍 Overview

Honolulu, a global tourist hotspot, presents unique Airbnb pricing challenges due to its seasonal demand, luxury listings, and location-sensitive bookings. This project uses over 35,000 listings and 27,000 guest reviews to:

- Predict nightly prices using regression models 🧮
- Extract key guest sentiment themes using NLP 🧠
- Identify the most influential features in pricing and guest satisfaction

The project integrates data preprocessing, sentiment scoring, topic modeling, and predictive analytics into a unified pipeline to assist hosts and platforms in making data-driven decisions.

---

## 🧾 Prerequisites

Ensure you have the following libraries installed:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `transformers` (Hugging Face)
- `nltk`
- `gensim` (for LDA topic modeling)

Install using:
pip install pandas numpy matplotlib seaborn scikit-learn transformers nltk gensim

## 🧠 Methodology

### 🔹 Data Cleaning & Preprocessing
- Filtered Honolulu listings from the Inside Airbnb dataset  
- Removed columns with 40%+ missing data  
- Imputed missing values (median/mode)  
- Converted price field to float  
- Engineered `price_per_guest` and composite review score  

### 🔹 Natural Language Processing (NLP)
- Cleaned review texts (lemmatization, stopword removal)  
- Used zero-shot classification to tag sentiment themes  
- Applied Latent Dirichlet Allocation (LDA) for topic modeling  

### 🔹 Feature Engineering
- Combined review and listing data  
- Merged sentiment and topic scores with numeric features  

---

## 📈 Model Evaluation

We used 3 supervised models for price prediction:

| Model               | R² Score | RMSE      | MAE     |
|---------------------|----------|-----------|---------|
| Linear Regression   | 0.34     | $111.47   | $70.21  |
| K-Nearest Neighbors | 0.39     | $128.88   | $58.96  |
| Random Forest       | 0.52     | $114.45   | $53.39  |

- ✅ **Random Forest** performed best on test data but showed some overfitting  
- 🔄 **KNN** had relatively stable MAE and explained more variance than linear regression  

---

## 📊 Key Insights

- Listings in premium areas command a **23% price premium**  
- Positive sentiment reviews → **9.3% increase in price**  
- Most appreciated themes: **cleanliness**, **location**, and **host communication**  
- Listings with “instant book” enabled and strong review activity → **higher demand**  
- Availability drops by ~**12.6%** for instant-bookable listings with high review volumes  

---

## 📁 Repository Contents

| File                    | Description                                             |
|-------------------------|---------------------------------------------------------|
| `Project AIML.ipynb`    | Full end-to-end analysis notebook                       |
| `docs/Airbnb_Report.pdf`| Final written report with methodology and findings      |
| `reviews.csv` *(optional)* | Dataset of Airbnb guest reviews                    |
| `README.md`             | This file — project overview and guide                  |

---

## 📄 Report

📥 [Download Final PDF Report](docs/Airbnb_Report.pdf)

**Includes**:
- Data pipeline and transformations  
- NLP pipeline (zero-shot classification & LDA)  
- Model tuning and evaluation  
- Business impact and strategy suggestions  

---
