# ChatGPT

ChatGPT is an open-source **Agentic AI Chatbot** built with **Python, FastAPI, LangGraph, LangChain, Google Gemini, Tavily, ChromaDB, and SQLite**.

It supports real-time streaming chat, document uploads, Retrieval-Augmented Generation (RAG), web search, conversation memory, and a simple web interface.

---

## 🚀 Live Demo

**Try the application here:**

https://chatgpt-agent-f9v4.onrender.com

> **Note:** The application is hosted on Render's free tier. If the app has been inactive, the first request may take 30–60 seconds while the server wakes up.

---

## Features

- Chat with an AI agent powered by Google Gemini
- Stream responses in real time
- Upload PDF, DOCX, TXT, MD, PY, and CSV documents
- Retrieval-Augmented Generation (RAG) using uploaded documents
- Search the web using Tavily
- Store and recall conversation history
- Long-term memory support
- Multi-turn conversations with LangGraph
- Simple FastAPI web interface

---

## Project Overview

This project combines:

- **FastAPI** for backend APIs
- **Jinja2** for rendering the frontend
- **LangGraph** for agent orchestration
- **LangChain** for tools and RAG
- **Google Gemini** as the LLM
- **Tavily** for web search
- **ChromaDB** for vector storage
- **SQLite** for chat history, long-term memory, and checkpoints

---

## Tech Stack

- Python
- FastAPI
- LangGraph
- LangChain
- Google Gemini
- Tavily Search
- ChromaDB
- SQLite
- SQLAlchemy
- Jinja2

---

## Prerequisites

Make sure you have the following installed:

- Python 3.11+
- pip or conda
- Git
- Google Gemini API Key
- Tavily API Key

---

## Getting Started

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the project

```bash
cd ChatGPT
```

### 3. Create a virtual environment

Using conda:

```bash
conda create -n chatgpt python=3.11 -y
```

### 4. Activate the environment

```bash
conda activate chatgpt
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file in the project root.

```env
GOOGLE_API_KEY=your_google_api_key
GOOGLE_MODEL=gemini-2.5-flash

TAVILY_API_KEY=your_tavily_api_key

LANGSMITH_TRACING=false
LANGSMITH_ENDPOINT=https://api.smith.langchain.com
LANGSMITH_API_KEY=your_langsmith_api_key
LANGSMITH_PROJECT=chatgpt
```

---

## Run Locally

```bash
python app.py
```

Open:

```
http://127.0.0.1:8080
```

---

## Project Structure

```text
ChatGPT/
│
├── app.py                  # FastAPI app and streaming endpoints
├── agent.py                # LangGraph agent
├── database.py             # SQLite + SQLAlchemy logic
├── rag.py                  # RAG pipeline
├── tools.py                # Agent tools
├── requirements.txt
│
├── templates/
│   └── index.html
│
├── uploads/                # Uploaded files
├── data/                   # SQLite databases
└── chroma_db/              # Chroma vector database
```

---

## Example Questions

```text
Summarize the uploaded PDF.
```

```text
Search the web for the latest AI agent news.
```

```text
Based on my uploaded document, what are the key points?
```

```text
Calculate 125 * 48 / 6.
```

---

## Notes

- Do not commit your `.env` file.
- Keep your API keys private.
- For production, disable `reload=True`.
- Runtime-generated files inside `uploads/`, `data/`, and `chroma_db/` should use persistent storage when deploying to production.

---

## Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Open a Pull Request.

---

## License

This project is open source. Please refer to the repository license for usage details.