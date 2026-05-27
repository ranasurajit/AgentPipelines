# 🤖 AgentPipelines

A modular collection of AI agents built as workflow-driven pipelines using n8n and tool-based reasoning.

This project demonstrates how to design reliable, scalable AI agents that interact with external tools (APIs, data sources) while enforcing strict prompt rules to minimize hallucinations.

---

## 🚀 Overview

Modern AI systems are not just models — they are pipelines.

**AgentPipelines** treats each AI agent as a structured workflow:
- Input → Reasoning → Tool Selection → Execution → Response

Each agent is designed to:
- Use tools deterministically when required
- Avoid hallucinated responses
- Provide concise, structured outputs

---

## 🧠 Key Concepts

- **Agentic Workflows** using n8n  
- **Tool-Augmented Reasoning** (LangChain-style agents)  
- **Prompt Guardrails** to enforce correct behavior  
- **Memory-Enabled Conversations**  
- **Secure API Handling** via environment variables  

---

## 📂 Project Structure

```
AgentPipelines/
│
├── agents/
│ ├── news-weather-agent/
│ │ ├── workflow.json
│ │ └── README.md
│
├── shared/
│ ├── prompts/
│ └── configs/
│
├── docs/
│
├── .env.example
├── .gitignore
|__ .env
└── README.md
```

---

## 🌦️ Included Agents

### 1. News & Weather Agent
- Fetches real-time weather data via API  
- Retrieves latest news using RSS feeds  
- Uses strict tool-calling rules  
- Summarizes outputs concisely  

📁 Path: `agents/news-weather-agent/`

---

## ⚙️ Tech Stack

- **n8n** — workflow orchestration  
- **LangChain Agent Nodes** — tool-based reasoning  
- **OpenRouter** — LLM provider  
- **Weather API** — real-time data  
- **RSS Feeds** — news ingestion  

---

## 🏗️ How It Works

1. User sends a query  
2. AI agent interprets intent  
3. համապատասխան tool is selected:
   - Weather → Weather API  
   - News → RSS Feed  
4. Tool executes  
5. Agent summarizes response  

---

## 🔐 Environment Setup

Create a `.env` file:

```
WEATHER_API_KEY=your_api_key
OPENROUTER_API_KEY=your_api_key
```


Start n8n with environment variables loaded.

---

## 🛠️ Usage

1. Import workflow into n8n  
2. Configure credentials / environment variables  
3. Activate the workflow  
4. Interact via chat/webhook  

---

## 💡 Sample Queries

- "What's the weather in Bangalore?"
- "Give me latest tech news"
- "Will it rain today in Delhi?"

---

## 📌 Design Highlights

- Enforces **tool usage over guessing**
- Prevents hallucinated outputs
- Modular and extensible architecture
- Clean separation of logic, prompts, and configuration

---

## 🔮 Future Enhancements

- Multi-agent coordination  
- Additional domain agents (finance, travel, coding)  
- Central orchestration layer  
- Structured JSON responses  

---

## 👨‍💻 Author

Surajit Rana
