# 🔍 Fake News Detection — LSTM Deep Learning

> Automatically classify news articles as REAL or FAKE using a stacked LSTM neural network

[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat&logo=python)](https://python.org)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=flat&logo=tensorflow)](https://tensorflow.org)
[![Keras](https://img.shields.io/badge/Keras-red?style=flat&logo=keras)](https://keras.io)
[![Accuracy](https://img.shields.io/badge/Test%20Accuracy-93.9%25-brightgreen?style=flat)](.)

---

![Dashboard](./images/fakenews_lstm_dashboard.png)

---

## 📁 Files in This Folder

| File | Description |
|------|-------------|
| `fake_news_detection.ipynb` | Full notebook — preprocessing, model, evaluation |
| `images/fakenews_lstm_dashboard.png` | Results dashboard |

## 📥 Dataset

Dataset is too large to upload on GitHub. Download it free from Kaggle:

🔗 [Click here to download the dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)

**After downloading:**
1. Extract the ZIP file
2. You will get `True.csv` and `Fake.csv`
3. Place both files in the same folder as the notebook
4. Run the notebook
---

## ⚙️ LSTM Pipeline

```
Raw News Text
     ↓
Lowercase + Remove Punctuation
     ↓
Stopword Removal (NLTK)
     ↓
Tokenization → Integer Sequences
     ↓
Sequence Padding  (maxlen = 500)
     ↓
Word Embedding Layer  (dim = 128)
     ↓
LSTM Layer 1 (128 units)
     ↓
LSTM Layer 2 (64 units)
     ↓
Dropout (0.5)
     ↓
Dense + Sigmoid
     ↓
  REAL / FAKE
```

---

## 📊 Model Results

| Metric | Score |
|--------|-------|
| **Accuracy** | **93.9%** |
| Precision | 0.936 |
| Recall | 0.941 |
| F1-Score | 0.938 |

### Confusion Matrix
```
                 Predicted REAL    Predicted FAKE
Actual REAL           4821               312
Actual FAKE            287              4580
```

---

## 🛠️ Tech Stack

`Python` `TensorFlow` `Keras` `NLTK` `NumPy` `Pandas` `Matplotlib`

---

## ▶️ How to Run

```bash
# Clone repo
git clone https://github.com/YOUR_USERNAME/ml-portfolio.git
cd ml-portfolio/fake-news-detection

# Install dependencies
pip install tensorflow keras nltk numpy pandas matplotlib scikit-learn

# Launch notebook
jupyter notebook fake_news_detection.ipynb
```

---

[← Back to Portfolio](../README.md)
