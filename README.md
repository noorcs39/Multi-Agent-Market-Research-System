# 🧠 Multi-Agent Market Research System

This project implements a **multi-agent system** for conducting automated market research using [CrewAI](https://docs.crewai.com/), [LangChain with Ollama](https://python.langchain.com/docs/integrations/llms/ollama/), and the [Serper.dev](https://serper.dev/) search tool.

## 🛠 Overview

The system is composed of three specialized AI agents working in a **sequential pipeline**:

1. **Market Data Gatherer**
   Gathers the latest trends, pricing, competitors, and customer demographics in a given product domain (e.g., wearable tech).

2. **Market Analyst**
   Analyzes the gathered data to identify opportunities, threats, and competitive advantages.

3. **Report Generator**
   Summarizes the insights into a concise, business-ready market research report.

---

## 🚀 How It Works

```python
from crewai import Agent, Task, Crew, Process
from crewai_tools import SerperDevTool
from langchain_ollama import OllamaLLM
```

* **OllamaLLM** is used to power the agents using a local LLaMA 3 model.
* **SerperDevTool** enables real-time web search for up-to-date market data.

The process flow:

* Agent 1 gathers real-world data using search tools.
* Agent 2 processes the raw data into strategic insights.
* Agent 3 converts those insights into a formatted market research report.

---

## 📦 Requirements

Make sure the following are installed and running:

* Python 3.10+
* Ollama installed and running locally with the `llama3` model pulled
  (`ollama run llama3`)
* `crewai`, `langchain`, `crewai-tools`, and `serper-dev` Python packages

Install dependencies:

```bash
pip install crewai langchain crewai-tools langchain-ollama
```

---

## 🔑 Serper API Key

You must set your Serper.dev API key as an environment variable:

```bash
export SERPER_API_KEY=your_api_key_here
```

---

## ▶️ Run the Script

```bash
python market_research.py
```

The final market research report will be printed in the terminal.

---

## 🧩 Customization

You can easily adapt this system to other domains like:

* Automotive
* Fintech
* Real Estate
* Healthcare

Just change the task description in `task_gather`.

---

## 📄 Output Example

```
📊 Final Market Research Report:
The wearable tech market is experiencing...
```

---

## 📬 Contact

For improvements or collaboration, feel free to reach out!

**Author:** Noor Uddin
**Email:** [noor.cs2@yahoo.com](mailto:noor.cs2@yahoo.com)

---
