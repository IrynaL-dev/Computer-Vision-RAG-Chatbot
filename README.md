# Computer Vision RAG Chatbot

An intelligent **chatbot** powered by **Retrieval-Augmented Generation (RAG)** that answers questions about **Computer Vision** using custom `.txt` documents, semantic search, and an LLM hosted via **ChatGroq (LLaMA3-8B-8192)**.

---

## 🧠 Overview

This project creates a **domain-specific Q\&A assistant** for **Computer Vision** topics. It uses RAG to retrieve semantically relevant information from a local document collection and generate accurate, context-aware answers.

### What it does:

* Loads `.txt` files with Computer Vision knowledge
* Uses **HuggingFace sentence-transformers/all-MiniLM-L6-v2** to embed and index documents in **ChromaDB**
* Accepts user questions via CLI or notebook
* Uses **ChatGroq API** with **LLaMA3-8B-8192** to generate grounded answers

---

## 🎯 Target Audience

This assistant is designed for:

* ML engineers & researchers learning Computer Vision
* Students preparing for CV-related interviews or exams
* Educators or AI trainers creating visual AI learning resources
* Teams managing internal documentation or educational CV material

---

## 🛠 Prerequisites

* Python 3.9+
* Basic knowledge of Python
* API key for **Groq** to access LLaMA3
* Local `.txt` documents related to Computer Vision

---

## ⚙️ Installation

```bash
git clone https://github.com/your-username/computer-vision-rag-chatbot.git
cd computer-vision-rag-chatbot
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

---

## 🌱 Environment Setup

Create a `.env` file and add:

```env
GROQ_API_KEY=your_groq_api_key
```

Dependencies are in `requirements.txt`, including:

* `langchain`
* `chromadb`
* `sentence-transformers`
* `groq` (for LLM access)

---

## 📁 Data Requirements

Place your **`.txt` documents** inside the folder:

```
/data/documents/
```

The assistant automatically ingests and chunks them for semantic retrieval.

---

## 🚀 Usage

### Notebook Demo

Run this notebook to test the chatbot:

```bash
notebooks/computer_vision_chatbot.ipynb
```

### CLI Version

```bash
python src/chatbot.py
```

Then enter a question like:

```
What is the role of convolution in CNNs?
```

---

## 🧪 Testing

To run tests:

```bash
pytest tests/
```

Tests cover embedding, vector store setup, and response quality.

---

## 🧩 Configuration

Modify `config.yaml` to change:

```yaml
embedding_model: sentence-transformers/all-MiniLM-L6-v2
vector_store: chroma
llm_provider: groq
llm_model: llama3-8b-8192
chunk_size: 500
```

---

## 💡 Features

* 🧠 Domain-specific responses (Computer Vision)
* 📚 Local document storage with `.txt` support
* 🔍 Fast retrieval via **ChromaDB**
* 🧬 Compact embeddings with HuggingFace models
* 💬 Natural language responses from LLaMA3 via **Groq**

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🤝 Contributing

1. Fork this repo
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Make your changes
4. Run tests
5. Open a PR!

We welcome improvements such as:

* New UX interfaces (e.g., Streamlit)
* Support for PDF ingestion
* Adding memory or ReAct-style reasoning chains

---

## 📬 Contact

Maintained by \[Your Name].
Feel free to reach out via Issues or Pull Requests.

---

