# Question-Answering-Assistant

A Retrieval-Augmented Generation (RAG) pipeline that answers questions using both **local PDFs** and **web scraping**. Powered by **LLMs**, **FAISS**, and **multi-agent orchestration** with CrewAI.

---

## 🚀 Features

- 📄 Load and vectorize PDF documents
- 🔍 Smart routing: decides whether to use local or web data
- 🌐 Web search and scraping with agents
- 🧠 Uses LLMs like `llama-3.3-70b-specdec` and `Gemini 1.5 Flash`
- 🛠️ Modular design using Langchain and CrewAI

---

## 🛠️ Tech Stack

| Tool / Library            | Purpose                                 |
|--------------------------|-----------------------------------------|
| `LangChain`              | Document loading, chaining, and agents  |
| `FAISS`                  | Vector similarity search                |
| `HuggingFace Embeddings` | Sentence embeddings                     |
| `ChatGroq`               | LLM for QA                              |
| `CrewAI`                 | Task-based agent orchestration          |
| `Serper.dev`             | Google Search API                       |
| `ScrapeWebsiteTool`      | Web content extraction                  |
| `dotenv`                 | Environment variable management         |

---
