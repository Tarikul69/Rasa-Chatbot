<h1 align="center">🤖 Intelligent RASA Chatbot with LLM, RAG & Memory</h1>
<p align="center"><b>A context-aware conversational assistant using RASA, Local LLM, Retrieval-Augmented Generation (RAG), and Vector Database.</b></p>

---

## 🧠 Project Overview

This is a smart chatbot system powered by:
- ✅ **RASA** – NLU and dialogue management framework
- 🔗 **LLM (Mistral or any local model)** – Generates intelligent responses
- 📚 **RAG (Retrieval-Augmented Generation)** – Retrieves relevant document chunks before generation
- 🗂️ **Vector Database (FAISS/Chroma)** – Stores embedded textbook data for long-term memory
- 🧾 **Memory Support**
  - **Short-term memory** – Tracks recent conversation history
  - **Long-term memory** – Retrieves from stored document vectors

---

## Key Features

- Conversational chatbot with intent recognition (English + Bangla)
- Retrieval-Augmented Generation for domain-grounded responses
- Dual memory system:
  - Short-term: recent user messages
  - Long-term: embedded document knowledge base
- Integrated LLM using REST API with context injection
- Supports HSC Textbooks or any custom PDF source

---

## Tech Stack

- **RASA** for bot flow and NLU
- **Mistral (or any LLM)** for intelligent response generation
- ** Chroma** for vector-based long-term memory
- **LangChain for document embedding
- **Flask backend for LLM-RAG server
- **Python** as core language

---

## 📁 Folder Structure

```bash
rasa_llm_rag_chatbot/
├── data/                  ← RASA training data (intents/entities)
├── domain.yml             ← RASA domain definitions
├── config.yml             ← NLU pipeline config
├── endpoints.yml          ← Webhook + action configs
├── actions/               
│   └── llm_rag.py         ← Custom RASA actions calling LLM API
├── backend/               ← RAG + LLM service
│   ├── ingest.py          ← Chunk, embed & store documents in vector DB
│   └── rag_server.py      ← API that connects LLM, RAG, memory
├── vectorstore/           ← FAISS/Chroma DB files
└── models/                ← RASA trained models
