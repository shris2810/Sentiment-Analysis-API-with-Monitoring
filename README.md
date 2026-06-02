# 🚀 Sentiment Analysis API with Monitoring

Deployed NLP sentiment analysis service that classifies text as positive/negative in real-time, with full experiment tracking and model monitoring.

---

## What the Project Does

Fine-tuned a **DistilBERT** model on IMDB/Twitter sentiment data and exposed it as a production-style REST API. The service accepts raw text and returns a sentiment label with a confidence score. Model experiments, metrics, and versions are tracked via MLflow, and live API performance is monitored to ensure reliability in a simulated production environment.

---

## 🛠 Tech Stack

- **FastAPI** — REST API framework
- **HuggingFace Transformers** — DistilBERT fine-tuning and inference
- **Docker** — containerization
- **MLflow** — experiment tracking, model registry, and monitoring UI
- **AWS EC2** — cloud deployment

---

## 🏗 Architecture Plan

```
User Request
     │
     ▼
FastAPI (REST API)
     │
     ▼
DistilBERT Model (HuggingFace)
     │
     ├──► Prediction + Confidence Score
     │
     ▼
MLflow Logging
     │
     ├──► Metrics (Accuracy, F1)
     ├──► Model Versions & Registry
     └──► Live Prediction Monitoring UI

Infrastructure: Docker Container → AWS EC2
```
---
 
## 📂 Datasets
 
| Dataset | Size | Source |
|---------|------|--------|
| IMDB Movie Reviews | ~50,000 reviews | HuggingFace `datasets` |
 
Both datasets are binary sentiment classification (positive/negative) and loaded directly via `datasets.load_dataset()`.
 
---
 
## 📊 Results
 
> **In progress** — expected benchmarks for fine-tuned DistilBERT:
 
| Metric | Expected Score |
|--------|---------------|
| Accuracy | ~92–93% |
| F1 Score | ~0.91–0.93 |
 
---
 
## ▶️ How to Run
 
> **Coming soon**
