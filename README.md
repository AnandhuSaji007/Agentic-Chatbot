# Agentic AI Chatbot Using LangGraph

This project demonstrates how to build an **Agentic Workflow** using LangChain, LangGraph, and multiple external tools (Arxiv, Wikipedia, Tavily). 
The agent queries research papers, Wikipedia, Tavily Search, and generates responses using Groq-powered LLM.

---

## 🚀 Features
- Query **Arxiv** for research papers.
- Query **Wikipedia** for quick knowledge retrieval.
- Use **Tavily Search** for web-based search results.
- Orchestrate with **LangGraph** for agentic workflows.
- Generate responses with **ChatGroq** (Qwen3-32B model).

---

## 📂 Project Structure
- `Agent_chatbot.ipynb` → Jupyter notebook for running the agent.
- `requirements.txt` → Dependencies required for the project.
- `.env` → Store environment variables.
---

## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/AnandhuSaji007/Agentic-Chatbot
cd Agentic-Chatbot
```

### 2️⃣ Create a Virtual Environment
```bash
conda create -p venv python=3.12 -y
```

Activate it:
- **Windows**: `conda activate venv/`

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Run the Agent
Open Jupyter Notebook and run:
```bash
Agent_chatbot.ipynb
```

## 🛠️ Code Overview

The core logic:
- Wrap Arxiv & Wikipedia APIs with LangChain tools.
- Use **Tavily Search** for additional info.
- Define agent state using LangGraph `StateGraph`.
- Add nodes (`tool_calling_llm`, `tools`) and edges.
- Compile the graph and invoke the agent with a query.

---

## 📌 Example Query
```python
messages = graph.invoke({"messages": "give latest news in AI and then give about 'Attention is All You Need' research paper"})
for m in messages["messages"]:
    m.pretty_print()
```

---

## 📖 Output
- The agent fetches the latest AI news via Tavily.
- Retrieves summary of "Attention is All You Need" from Arxiv/Wikipedia.
- Combines responses and prints them neatly.

---


## 📌 Author
Developed by **Anandhu Saji**
