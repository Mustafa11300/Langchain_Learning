
# 🧠 Document Similarity using LangChain + OpenAI

This project demonstrates how to use **OpenAI embeddings** (via LangChain) to measure **semantic similarity** between a query and a set of documents using **cosine similarity**.

---

## 📘 Overview

The script embeds multiple text documents and a user query using **`text-embedding-3-large`** from OpenAI, then computes their **cosine similarity** to find which document best matches the query.

---

## 🧩 Project Structure

```
GEN_AI(CAMPUS-X)/
│
├── ChatModels/
│   └── 1.Document_Similarity.py
│
├── venv/
├── .env
├── requirements.txt
└── test.py
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/Mustafa11300/Langchain_Learning.git
cd Langchain_Learning
```

### 2. Create and Activate a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate   # for macOS/Linux
# OR
venv\Scripts\activate      # for Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Add Your OpenAI API Key

Create a `.env` file in the root directory and add:

```
OPENAI_API_KEY=your_api_key_here
```

---

## 🧠 How It Works

```python
from langchain_openai import OpenAIEmbeddings
from sklearn.metrics.pairwise import cosine_similarity
```

1. **Embeddings** are generated for each document and the query using `OpenAIEmbeddings`.
2. **Cosine similarity** compares the query vector with each document vector.
3. The script returns the **most semantically similar document** to the query.

---

## 🚀 Example Output

```
Most similar document to the query 'tell me about virat kohli':
Document: Virat Kohli is an Indian cricketer known for his aggressive batting and leadership.
Similarity Score: 0.9351
```

---

## 📦 Requirements

* Python 3.8+
* `langchain-openai`
* `scikit-learn`
* `numpy`
* `python-dotenv`

---

## 🧾 License

This project is released under the **MIT License**.


