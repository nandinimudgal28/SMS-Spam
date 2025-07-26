#  SMS Spam Detection & Data Insights

##  Project Overview
This repository presents a full pipeline of a **Spam SMS Detection System**, coupled with **data visualizations** and **machine learning models**. The notebook focuses on both **business insights** and **spam classification**, providing actionable intelligence from the dataset.

---

## 📁 Dataset
The project uses a CSV file containing labeled SMS messages (`ham` or `spam`). The main columns used:

- `Category`: Label (`ham` or `spam`)
- `Message`: The SMS text
- Additional derived features (message length, punctuation count, etc.)

---

##  Key Actions Performed

###  1. Data Loading & Cleaning
- Imported the dataset using `pandas`.
- Removed null values.
- Renamed columns for clarity.
- Encoded the `Category` column as binary (1 = spam, 0 = ham).
- Created new features: `Message_Length`, `Punctuation_Count`.

###  2. Exploratory Data Analysis (EDA)
- **Distribution Plots:** Pie chart showing proportion of spam vs ham.
- **Histograms & Boxplots:** Message length and punctuation distribution across labels.
- **WordClouds:** Visual representation of frequently occurring words in spam and ham messages.
- **Most Common Words:** Bar charts of top keywords for spam and ham messages.

###  3. Text Preprocessing
- Lowercasing
- Removing punctuation
- Removing stopwords
- Lemmatization

###  4. Feature Extraction
- Converted text data into numerical vectors using:
  - **CountVectorizer**
  - **TF-IDF Vectorizer**

###  5. Model Training & Evaluation
Trained multiple classification models:
- **Multinomial Naive Bayes**
- **Logistic Regression**
- **Random Forest Classifier**

Evaluated using:
- Accuracy Score
- Classification Report (Precision, Recall, F1-score)
- Confusion Matrix
- ROC Curve Plot

###  6. Model Comparison
Compared models using accuracy scores and visualized ROC curves for interpretability.

---

## Visualizations
- **Spam vs Ham Distribution** (Pie chart)
- **WordClouds** for Spam and Ham
- **Top Words** in Spam/Ham messages
- **Message Length vs Category**
- **Punctuation Analysis**
- **Model Performance Metrics** (confusion matrix, ROC curve)

---

## Conclusions
- The dataset is heavily skewed toward "ham" messages.
- Spam messages tend to be longer and contain more punctuation.
- Naive Bayes and Logistic Regression performed very well with high precision and recall for spam detection.
- TF-IDF vectorization helped reduce noise and improve model accuracy.

---

## 📂 Project Structure
```
📁 Spam_sms_detection/
│
├── Spam_sms.ipynb        # Full notebook with code, visualizations, and model training
├── dataset.csv           # Dataset used for SMS classification
├── README.md             # This file
```

---

## Future Improvements
- Deploy as a web application using Streamlit or Flask.
- Add real-time SMS classification via user input.
- Explore deep learning models (RNNs, LSTM).

---

## Acknowledgments
Built entirely using Python, Pandas, Matplotlib, Seaborn, Scikit-learn, and NLP techniques.
