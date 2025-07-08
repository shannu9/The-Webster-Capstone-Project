
# 🧠 Automating Fashion Tagging with GPT-4o: A Scalable AI Agent Solution

**Capstone Project | Stevens Institute of Technology – School of Business**  
**Industry Partner: The Webster (Luxury Fashion Retailer)**  
**Team Members:** Shanmukh Sri Surya Gopi, Shiva Kumar Midde, Abhiram Reddy Gunutula, Shriteja Salunkepatil  
**Instructor:** Prof. Alkiviadis Vazacopoulos

---

## 🚀 Overview

The Webster, a luxury fashion retailer, faced challenges with slow and inconsistent manual product tagging, leading to poor search accuracy and customer experience. Our team built a Python-based AI tagging system using **GPT-4o**, improving accuracy, reducing manual effort, and enabling scalable operations.

---

## 🎯 Objectives

- Eliminate manual product tagging bottlenecks
- Ensure consistency in category labeling
- Scale tagging pipeline for large catalogs and seasonal surges
- Integrate a user-friendly interface for merchandisers

---

## 🧰 Tech Stack

- **Language:** Python  
- **Libraries:** scikit-learn, pandas, NumPy, TensorFlow, torchvision, Flask  
- **Model:** GPT-4o (OpenAI API)  
- **Embedding:** ResNet-50 for images, TF-IDF for text  
- **Database:** PostgreSQL  
- **Infrastructure:** AWS EC2

---

## 🧪 Methodology

### 1. 🧹 Data Preparation
- Consolidated 94 noisy tags into 10 clean categories
- Removed duplicates and filled missing values
- Extracted metadata (brand, color, price) and vectorized text & images

### 2. 🤖 Model Experiments
- Tried traditional ML: XGBoost, CNN, Bi-LSTM → Poor accuracy (9–23%)
- Shifted to GPT-4o with 5-shot prompting (zero-shot generalization worked best)

### 3. ⚙️ Pipeline Architecture
```plaintext
Data Ingestion → Preprocessing → GPT-4o Inference → Confidence Thresholding → Flask UI for Review
