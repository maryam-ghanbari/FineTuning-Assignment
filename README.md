# FineTuning-Assignment

This repository contains my implementation for an **NLP course assignment** focused on **fine-tuning pre-trained Transformer models** on two text classification tasks.  
The goal is to explore how models such as **BERT**, **DistilBERT**, and **ALBERT** perform when fine-tuned on **Emotion** and **TweetEval (Irony)** datasets.

---

## 🎯 Objective
The main objectives of this project are:
- To understand and apply the fine-tuning process for pre-trained Transformer models.
- To evaluate model performance on different datasets.
- To compare BERT-family architectures in terms of effectiveness and efficiency.
- To analyze predictions qualitatively and generate confusion matrices for classification results.

---

## 📚 Datasets
Two publicly available Hugging Face datasets were used:
1. **Emotion dataset** – classifies emotions expressed in text (e.g., joy, sadness, anger, fear, etc.)
2. **TweetEval (Irony) dataset** – identifies irony and sarcasm in tweets.

Both datasets were split into **training**, **validation**, and **test** subsets for consistent evaluation.

---

## ⚙️ Models and Libraries
The following Transformer models were fine-tuned:
- **BERT** (`bert-base-uncased`)
- **DistilBERT** (`distilbert-base-uncased`)
- **ALBERT** (`albert-base-v2`)

### Core Libraries
- `transformers`  
- `datasets`  
- `scikit-learn`  
- `torch`  
- `numpy`  
- `ray` (for hyperparameter tuning)

---

## 🧩 Tasks Implemented
Each model follows the same pipeline structure:
1. **Dataset preprocessing** – tokenization, padding, truncation, and encoding.  
2. **Model training and evaluation** – using the Hugging Face `Trainer` API.  
3. **Fine-tuning** – hyperparameter optimization (learning rate, batch size, epochs, weight decay).  
4. **Confusion matrix generation** – to analyze classification errors.  
5. **Qualitative analysis** – comparing model predictions on sample texts.

---

## 📁 Repository Structure
FineTuning_Assignment/
│
├── emotion_bert.ipynb
├── emotion_distilbert.ipynb
├── emotion_albert.ipynb
├── irony_bert.ipynb
├── irony_distilbert.ipynb
├── irony_albert.ipynb
│
├── Assignment_Report.pdf
└── README.md

Each notebook focuses on one **model–dataset combination**, performing all assignment tasks for that specific setup.

---

## 🧪 Methodology Summary
- Pre-trained models were loaded from Hugging Face and adapted for sequence classification tasks.  
- The datasets were preprocessed using model-specific tokenizers.  
- Fine-tuning was done using the `Trainer` API with custom training arguments.  
- Hyperparameter search was automated using the **Ray Tune** library.  
- Confusion matrices and qualitative analyses were conducted to interpret model behavior.  

---
