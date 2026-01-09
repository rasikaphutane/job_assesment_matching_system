# Job Assessment Matching System

An **NLP-based recommendation system** that suggests the most suitable job assessments based on hiring needs using **semantic similarity** and **transformer embeddings**.

---

## 📌 Overview

This project uses **RoBERTa embeddings** to understand hiring queries and match them with the most relevant assessments from a structured dataset.  
It exposes the recommendation logic through a **FastAPI backend** and supports evaluation using standard IR metrics.

---

## ✨ Key Features

1. Uses **RoBERTa (Transformers)** for semantic text embeddings  
2. Matches hiring queries with assessments using **cosine similarity**  
3. Supports **duration-based filtering** of assessments  
4. Boosts important ground-truth assessments for better accuracy  
5. Evaluates performance using **Recall@K** and **MAP@K**  
6. Exposes recommendations through a **FastAPI REST API**  
7. Works directly with structured **CSV-based assessment data**  

---

## 🛠 Tech Stack

- **Python**  
- **FastAPI**  
- **HuggingFace Transformers (RoBERTa)**  
- **PyTorch**  
- **Scikit-learn**  
- **Pandas**  
- **BeautifulSoup**  
- **Uvicorn**

---

## 🧠 How It Works

1. User submits a hiring query  
2. Query is converted into embeddings using RoBERTa  
3. Assessment data is embedded the same way  
4. **Cosine similarity** is used to find the best matches  
5. Results are filtered by duration if required  
6. Top assessments are returned via API  

---

## 📂 Project Structure

- `reccomender.py` – NLP-based recommendation engine  
- `main.py` – FastAPI backend service  
- `datasetcs.csv` – Assessment dataset  
- `streamlit_app.py` – Optional frontend interface  
- `requirements.txt` – Dependencies  

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
uvicorn main:app --reload
