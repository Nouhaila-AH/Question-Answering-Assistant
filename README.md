# Question-Answering-Assistant
This project implements a Retrieval-Augmented Generation (RAG) system that answers questions using both local documents (PDFs) and real-time web content. It uses LLMs, vector databases, and scraping tools to provide accurate and context-rich answers.

🚀 Features
🧾 PDF Document Ingestion: Loads and processes PDFs into a searchable vector database.

🧠 Intelligent Routing: Determines whether the answer exists in local documents or should be searched online.

🌍 Web Search + Scraping: Uses tools like Serper and website scrapers to extract up-to-date web content.

💬 LLM-Powered Responses: Utilizes models like llama-3.3-70b-specdec and Gemini 1.5 Flash to generate coherent and accurate answers.

👥 Agentic Workflow: Implements task-based agents (CrewAI) to handle search and scraping separately and effectively.

🛠️ Tech Stack
Component	Description
🦜 Langchain	Document loading, text splitting, and LLM chaining
🤗 HuggingFaceEmbeddings	Embedding generation for document vectorization
🧠 ChatGroq	LLM inference using the Groq API
🧠 CrewAI	Multi-agent orchestration of search and scraping tasks
🔍 SerperDevTool	Google Search API for relevant web sources
🕸️ ScrapeWebsiteTool	Tool to scrape and extract website content
📄 FAISS	Vector search for document similarity
📚 dotenv	Environment variable management

📦 Setup Instructions
1. Clone the Repo
bash
Copier
Modifier
git clone https://github.com/your-username/intelligent-query-assistant.git
cd intelligent-query-assistant
2. Install Dependencies
bash
Copier
Modifier
pip install -r requirements.txt
Make sure to include in requirements.txt:

txt
Copier
Modifier
langchain
langchain_groq
langchain_huggingface
crewai
crewai-tools
faiss-cpu
python-dotenv
3. Environment Variables
Create a .env file in the root directory:

env
Copier
Modifier
GROQ_API_KEY=your_groq_api_key_here
4. Prepare the PDF
Place the PDF you want to use in your local knowledge base in the appropriate path. Adjust the pdf_path in main() accordingly.

▶️ How It Works
Load & Index: The PDF is loaded and chunked, then converted into a vector database using embeddings.

Query Processing:

First, the system checks whether it can answer the question from the local documents.

If Yes, it retrieves similar chunks from the vector database.

If No, it triggers a CrewAI-based web search and scraping workflow.

LLM Answering: Based on the chosen context, an LLM generates a final answer.

🧪 Example
bash
Copier
Modifier
python main.py
Example output:

yaml
Copier
Modifier
Processing query: What is Agentic RAG?
Can answer locally: no
Retrieved context from web scraping

Final Answer:
Agentic RAG refers to...
📁 Project Structure
bash
Copier
Modifier
📦 project-root
├── main.py
├── requirements.txt
├── .env
├── README.md
└── pdfs/
    └── genai-principles.pdf
📌 Notes
This is a demo-style hybrid RAG implementation.

You may replace models, agents, and tools as per your needs.

Web search requires a valid Serper.dev API key (or you can extend it with other search APIs).

