# 🤖 RAG Pipeline Demo

> A production-ready **Retrieval-Augmented Generation (RAG)** pipeline built with LangChain, FAISS, and OpenAI GPT-4. Upload any document and ask questions — powered by semantic search + LLM reasoning.

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square)
![OpenAI](https://img.shields.io/badge/GPT--4-412991?style=flat-square&logo=openai&logoColor=white)
![FAISS](https://img.shields.io/badge/FAISS-00A3E0?style=flat-square)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

---

## 📌 Overview

This project demonstrates a complete RAG pipeline that:

- **Ingests** PDF and text documents
- **Chunks & embeds** content using OpenAI Embeddings
- **Indexes** vectors using FAISS for fast similarity search
- **Retrieves** the most relevant chunks for any query
- **Generates** accurate, grounded answers using GPT-4
- **Serves** an interactive web UI via Streamlit

---

## 🏗️ Architecture

```
User Query
    │
    ▼
Query Embedding (OpenAI)
    │
    ▼
FAISS Vector Search ──── Document Chunks ◄── PDF/TXT Ingestion
    │
    ▼
Top-K Relevant Chunks
    │
    ▼
GPT-4 (with context)
    │
    ▼
Grounded Answer
```

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| Orchestration | LangChain |
| LLM | OpenAI GPT-4 |
| Embeddings | OpenAI text-embedding-ada-002 |
| Vector Store | FAISS (CPU) |
| Web UI | Streamlit |
| Document Loaders | PyPDFLoader, TextLoader |

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/SaiKiran-212/rag-pipeline-demo.git
cd rag-pipeline-demo
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Set your OpenAI API key
```bash
export OPENAI_API_KEY="your-api-key-here"
```

### 4. Run via Python (CLI)
```bash
python src/rag_pipeline.py
```

### 5. Run the Streamlit Web App
```bash
streamlit run app.py
```
Then open `http://localhost:8501` in your browser.

---

## 📁 Project Structure

```
rag-pipeline-demo/
├── src/
│   └── rag_pipeline.py       # Core RAG pipeline class
├── notebooks/
│   └── rag_exploration.ipynb # Jupyter notebook walkthrough
├── data/
│   └── sample.txt            # Sample document for testing
├── app.py                    # Streamlit web application
├── requirements.txt          # Python dependencies
└── README.md
```

---

## 💡 Key Features

- **Modular Design** — RAGPipeline class is reusable and extensible
- **Persistent Index** — Save and load FAISS index to/from disk
- **Custom Prompts** — Tailored prompt template for accurate, grounded answers
- **Source Attribution** — Every answer includes source document references
- **Multi-format Support** — Handles both PDF and plain text files
- **Interactive UI** — Streamlit app with chat history and source viewer

---

## 📊 How RAG Reduces Hallucinations

Traditional LLMs generate answers from training data alone — which can be outdated or wrong. RAG grounds every answer in your actual documents:

```
Without RAG: LLM guesses → hallucination risk
With RAG:    LLM + retrieved context → grounded, accurate answers
```

---

## 🔧 Customization

You can easily swap components:
- **Vector Store**: Replace FAISS with Pinecone or Chroma
- **LLM**: Switch GPT-4 to LLaMA 3, Mistral, or Claude
- **Embeddings**: Use HuggingFace sentence-transformers instead of OpenAI

---

## 👤 Author

**Sai Kiran Kummari** — Senior AI/ML Engineer  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sai-kiran-kummari-231250242)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/SaiKiran-212)

---

## 📄 License

MIT License — feel free to use and adapt this project.
