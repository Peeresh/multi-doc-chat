#  Multi-Document RAG Chat System

A production-ready **Conversational AI system** that allows users to upload multiple documents and interact with them using **Retrieval-Augmented Generation (RAG)**.

---
##  Demo

### Upload & Chat Interface

![Upload](assets/upload_and_chat.png.png)

### Example Response
![Upload](assets/response_example.png.png)

---
##  Features

*  Upload and process multiple documents (PDF, DOCX)
*  Semantic search using **FAISS vector database**
*  Context-aware responses using **Conversational RAG**
*  Session-based chat memory
*  FastAPI backend for scalable APIs
*  Fully tested with **unit + integration tests**

---

##  Architecture

```
User → FastAPI → Document Ingestion → Chunking → Embeddings → FAISS
                                              ↓
                                      Conversational RAG
                                              ↓
                                           Response
```

---

##  Tech Stack

* **Backend:** FastAPI
* **LLM Framework:** LangChain
* **Vector Store:** FAISS
* **Embeddings:** HuggingFace / OpenAI
* **Testing:** Pytest
* **Package Manager:** uv

---
##  Project Structure

```
multi-doc-chat/
│
├── multi_doc_chat/
│   ├── config/              # Configuration (YAML, settings)
│   ├── exception/           # Custom exception handling
│   ├── logger/              # Logging utilities
│   ├── model/               # Data models
│   ├── prompts/             # Prompt templates
│   ├── src/
│   │   ├── document_ingestion/   # Document loading & processing
│   │   ├── document_chat/        # RAG retrieval logic
│   ├── utils/               # Helper utilities (config, file ops, models)
│
├── templates/               # HTML frontend
├── static/                  # CSS / assets
├── test/                    # Unit + integration tests
├── notebook/                # Experiments & research notebooks
│
├── main.py                  # FastAPI entry point
├── pyproject.toml           # Project configuration
├── README.md
```

##  Setup & Run

```bash
git clone https://github.com/Peeresh/multi-doc-chat.git
cd multi-doc-chat
uv sync
uv pip install -e .
uv run uvicorn multi_doc_chat.src.api.main:app --reload
```

Open: http://127.0.0.1:8000

---

##  Run Tests

```bash
uv run pytest
```

---

## 📌 API

* `POST /upload` → Upload documents
* `POST /chat` → Ask questions

---
##  Key Concepts

* Retrieval-Augmented Generation (RAG)
* Vector similarity search (FAISS)
* Chunking & embeddings pipeline
* Conversational memory
* Modular and testable architecture

---

##  Future Improvements

* Streaming responses
* Frontend UI (React / Next.js)
* Persistent vector database (Pinecone/Chroma)
* Authentication & multi-user support

---

##  Author

**Peeresh Kethavath**
B.Tech @ IIT Hyderabad
AI Engineer | Generative AI | RAG Systems

---
