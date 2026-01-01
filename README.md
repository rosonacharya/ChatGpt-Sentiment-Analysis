# 📊 ChatGPT Sentiment Analysis using NLP & Machine Learning

This project focuses on **sentiment classification of tweets and reviews** using Natural Language Processing (NLP) and Machine Learning techniques. The goal is to classify text into **positive, negative, or neutral sentiments**.

---

## 📁 Dataset

- **Source:** Public tweet sentiment dataset  
- **Link:** https://www.kaggle.com/datasets/charunisa/chatgpt-sentiment-analysis*  

---

## 🧠 Project Pipeline (End-to-End NLP Workflow)

### 1️⃣ Data Loading
- Load dataset using pandas
- Inspect shape, columns, and data types
---

### 2️⃣ Data Cleaning
Performed to reduce noise and improve model performance:

- Lowercasing text
- Removing:
  - URLs
  - Mentions (@user)
  - Hashtags
  - Punctuation
  - Numbers
- Handling missing values (`NaN`)
- Removing emojis
- Normalizing repeated characters (e.g., `goooood → good`)
- Stopword removal

---

### 3️⃣ Text Preprocessing
Applied standard NLP preprocessing steps:

- Tokenization
- Lemmatization
- Removal of extra whitespaces
- Validation to ensure no empty or null texts remain

---

### 4️⃣ Feature Extraction
Converted text into numeric features:

#### ✔ Bag of Words (BoW)
- Represents text as word frequency vectors

#### ✔ TF-IDF (Term Frequency–Inverse Document Frequency)
- Gives higher importance to informative words
- Reduces impact of very frequent words

---

### 5️⃣ Train–Test Split
- Split ratio: **80% training / 20% testing**
- Stratified sampling used to preserve class distribution

---

### 6️⃣ Model Building
Three supervised ML models were trained:

- Naive Bayes
- Logistic Regression
- Support Vector Machine (SVM)

All models were trained using **TF-IDF features**.

---

### 7️⃣ Model Evaluation
Evaluation metrics used:

- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix

#### 🔍 Model Performance

| Model | Accuracy |
|-----|---------|
| Naive Bayes | 67.79% |
| Logistic Regression | **82.46%** |
| SVM | 81.83% |

---

### 🏆 Final Model Selection
**Logistic Regression** was selected as the best-performing model based on accuracy and stability.

---

## 📊 Confusion Matrix
Confusion matrices were plotted to analyze:
- True Positives
- False Positives
- False Negatives
- True Negatives

This helps understand **class-wise prediction performance**.

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/chatgpt-sentiment-analysis.git
cd chatgpt-sentiment-analysis
2️⃣ Install Dependencies
bash
Copy code
pip install -r requirements.txt
3️⃣ Run the Notebook
bash
Copy code
jupyter notebook
