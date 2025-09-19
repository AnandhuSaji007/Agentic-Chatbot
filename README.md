# IntelliAgent-Graph

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
- `agentic.ipynb` → Jupyter notebook for running the agent.
- `requirements.txt` → Dependencies required for the project.

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/IntelliAgent-Graph.git
cd IntelliAgent-Graph
```

### 2️⃣ Create a Virtual Environment
```bash
python -m venv agent
```

Activate it:
- **Windows**: `agent\Scripts\activate`
- **Linux/Mac**: `source agent/bin/activate`

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Run the Agent
Open Jupyter Notebook and run:
```bash
jupyter notebook agentic.ipynb
```

---

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

## ✅ Next Steps
- Extend the agent with more tools.
- Connect to custom knowledge bases.
- Add memory for multi-turn conversations.

---

## 📌 Author
Developed by **Your Name**
