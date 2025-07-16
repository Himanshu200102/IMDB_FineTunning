# IMDB Sentiment Analysis

This project builds a **privacy-friendly AI Agent** that classifies IMDb movie reviews as *positive* or *negative* sentiment.

✅ Runs **locally** for maximum data privacy  
✅ Uses an **open-source LLM** (DistilBERT)  
✅ Includes an **Inference Engine** with rule-based reasoning  
✅ Fine-tuned using **two different approaches** with real performance comparison  

---

## 🚀 Project Goals

- Build an AI Agent that can run locally, respecting user privacy
- Compare **two different fine-tuning approaches**
- Choose the better approach based on real metrics

---

## 📂 Dataset Used
- 50,000 labeled movie reviews
- Binary classification: 0 = negative, 1 = positive

---

## 🤗 Model Used

- **Base model**: [`distilbert-base-uncased`](https://huggingface.co/distilbert-base-uncased)
  - Lightweight, open-source Transformer
  - Easy to deploy on local devices

---

## 🧠 Inference Engine (Reasoning)

The agent includes a **rule-based Inference Engine** for post-processing and reasoning:

✅ **Confidence Threshold Rule**  
- If model confidence < 0.6 → return "Uncertain"

✅ **Negation Override Rule**  
- If input text contains negation words (e.g. "not", "never", "no"), flip the prediction

## Results Comparison
| Metric         | Standard Fine-Tuning  | LoRA                  |
| -------------- | --------------------- | --------------------- |
| Accuracy       | 89.0%                 | 87.4%                 |
| Inference Time | \~100.6 ms            | \~8.2 ms              |
| Model Size     | 262mb                 | 2.9mb                 |


