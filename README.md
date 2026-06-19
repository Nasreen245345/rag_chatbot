
# Context-Aware RAG Chatbot

A production-ready Retrieval-Augmented Generation (RAG) chatbot built using **LangChain, FAISS, Groq (Llama 3.1), HuggingFace embeddings, and Streamlit**.  
It retrieves relevant context from a knowledge base and generates accurate, grounded responses using an LLM.

---

## Features

-  Multi-source document ingestion (PDF, TXT, Wikipedia)
-  Semantic search using FAISS vector database
-  Retrieval-Augmented Generation (RAG)
-  Multi-turn conversation memory
-  Fast LLM responses using Groq (Llama 3.1)
-  Intelligent document chunking
-  Interactive Streamlit web UI
-  Reduced hallucinations with grounded responses

---

##  Architecture

User Query  
→ Embedding (HuggingFace MiniLM)  
→ FAISS Vector Search  
→ Top-K Relevant Chunks  
→ LLM (Groq / Llama 3.1)  
→ Final Answer + Conversation Memory  

---

##  Tech Stack

- Python
- LangChain
- FAISS (Vector Database)
- HuggingFace Transformers (MiniLM Embeddings)
- Groq API (Llama 3.1)
- Streamlit (Frontend UI)

---

##  Project Structure

```

├── streamlit_app.py        # Main Streamlit chatbot app
├── knowledge_base.txt      # Custom knowledge base
├── faiss_vectorstore/      # Saved vector database
├── rag_kb_stats.png        # Visualization output
├── embedding_space.png     # Embedding visualization
└── README.md               # Project documentation

````

---

##  Installation

### 1. Clone repository
```bash
git clone https://github.com/your-username/rag-chatbot.git
cd rag-chatbot
````

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install langchain langchain-community langchain-core
pip install langchain-groq langchain-huggingface
pip install faiss-cpu sentence-transformers
pip install streamlit wikipedia python-dotenv
```

---

##  API Key Setup

Get free Groq API key:
 [https://console.groq.com](https://console.groq.com)

Set environment variable:

```bash
export GROQ_API_KEY="your_api_key"
```

Or inside Python:

```python
import os
os.environ["GROQ_API_KEY"] = "your_api_key"
```

---

##  Run Project

```bash
streamlit run streamlit_app.py
```

Then open:

```
http://localhost:8501
```

---

##  How It Works

1. Load documents from multiple sources
2. Split text into chunks
3. Convert chunks into embeddings
4. Store embeddings in FAISS index
5. Convert user query into vector
6. Retrieve similar chunks from FAISS
7. Send context + query to LLM (Groq)
8. Generate final response
9. Store chat history in memory

---

##  Key Concepts

* Retrieval-Augmented Generation (RAG)
* Vector similarity search
* Embeddings (semantic understanding)
* Conversational memory
* Prompt engineering
* Document chunking

---

##  Use Cases

* AI chatbot assistant
* Document Q/A system
* Customer support bot
* Internship project demo
* Knowledge base assistant

---

##  Future Improvements

* Add re-ranking for better accuracy
* Use Pinecone / Weaviate instead of FAISS
* Add streaming responses
* Add citations in answers
* Deploy on cloud (AWS / Streamlit Cloud)

---

##  Outcome

This project demonstrates:

* End-to-end RAG pipeline
* Real-world LLM application
* Vector database usage
* Full-stack AI chatbot development

---

##  Author

Nasreen Fatima
Computer Science Student | AI/ML Enthusiast



---


