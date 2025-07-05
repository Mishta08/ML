# 🧠 Epileptic Seizure Detection using EEG data

This project focuses on classifying EEG (electroencephalogram) data to detect epileptic seizures using deep learning techniques. We explored different neural network architectures to identify seizure patterns in time-series EEG data.

---

## 📂 Project Includes

- `data` - EEG dataset (https://www.kaggle.com/datasets/harunshimanto/epileptic-seizure-recognition)
- `preprocessing` - Data cleaning, normalization, and oversampling
- `models`
  - `cnn_bigru_model.py` - CNN + BiGRU model
  - `lstm_gru_attention_model.py` - LSTM + GRU + Attention model
-  Training and evaluation script
- `requirementst` - Python dependencies
- `README` - Project documentation

---

## 📊 Dataset

We use the **UCI Epileptic Seizure Recognition Dataset**, which contains 500 EEG recordings segmented into 4097 time steps.

- **Classes**:
  - Class 1: Seizure
  - Classes 2–5: Non-seizure (eyes open, closed, normal activity, etc.)
- For binary classification: Classes 2–5 are grouped as non-seizure.

📎 [Dataset Link (UCI)](https://archive.ics.uci.edu/ml/datasets/Epileptic+Seizure+Recognition)

---

## 🧹 Preprocessing

- Normalization (z-score)
- Oversampling with **Random Over-sampler** to handle class imbalance
- Train-test split

---

## 🧠 Model Architectures

### 1️⃣ CNN + BiGRU

- **Convolutional layers** for local feature extraction
- **Bidirectional GRU** layers to capture temporal dependencies in both directions
-  Softmax output for binary classification

**Highlights:**
- Fast convergence
- Good spatial-temporal representation

---

### 2️⃣ LSTM + GRU with Attention Mechanism

- **Stacked LSTM and GRU** for richer sequence modeling
- **Custom Attention Layer** to focus on the most relevant time steps
- Improves interpretability and performance

**Highlights:**
- Attention helps model focus on critical EEG intervals
- Better performance in class-imbalanced settings

---



