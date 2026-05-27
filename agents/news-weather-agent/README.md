# 🌦️ News & Weather AI Agent

An AI-powered assistant built using n8n that provides real-time weather updates and latest news using tool-based reasoning and strict prompt control.

This agent ensures accurate responses by enforcing API usage instead of relying on model-generated guesses.

---

## 🚀 Overview

This workflow implements an intelligent AI agent that:

- Answers weather-related queries using a live Weather API  
- Fetches latest news via RSS feeds  
- Uses tool-based reasoning to avoid hallucinations  
- Maintains short-term conversational memory  

---

## 🧠 How It Works

1. User sends a message via chat/webhook  
2. AI Agent analyzes intent  
3. Based on query:
   - 🌦️ Weather → Calls Weather API  
   - 📰 News → Fetches RSS feed  
4. Tool executes and returns data  
5. Agent summarizes response concisely  

---

## 🔧 Workflow Components

### 1. Chat Trigger
- Entry point for user queries

### 2. AI Agent (LangChain आधारित)
- Handles reasoning and tool selection  
- Enforces strict prompt rules  

### 3. Memory Buffer
- Maintains short conversation context  

### 4. OpenRouter Chat Model
- LLM provider for agent reasoning  

### 5. Weather API Tool
- Fetches real-time weather data  
- Uses environment variables for API key  

### 6. News API Tool
- Reads RSS feed for latest news  

---

## ⚙️ Environment Variables

Create a `.env` file in the project root:

```env
WEATHER_API_URL=http://api.weatherapi.com/v1
WEATHER_API_KEY=your_api_key_here
```

---

## 🔐 Credentials Setup

- OpenRouter API key is configured via n8n Credentials
- It is NOT stored in the workflow JSON for security reasons

---

## 🛠️ Setup Instructions

1. Start n8n with environment variables:

```bash
npx dotenv -e .env -- n8n start
```

2. Open n8n UI:
```bash
http://localhost:5678
```

3. Import workflow:
- Go to Workflows
- Click Import from File
- Select workflow.json

4. Configure credentials:
- Add OpenRouter API key in Credentials

5. Activate workflow

---

## 💬 Sample Queries

- "What's the weather in Bangalore?"
- "Give me latest tech news"
- "Will it rain in Delhi today?"
- "Top headlines today"

---

## 📌 Design Highlights

- Enforces tool usage over model guessing
- Prevents hallucinated responses
- Clean separation of logic and configuration
- Uses environment variables for secure API handling
- Modular and extensible workflow design

---

## 🔮 Future Improvements

- Add support for multiple news sources
- Extend to multi-agent architecture
- Add structured JSON responses
- Integrate additional APIs (stocks, travel, etc.)

---

## 👨‍💻 Author

- Surajit Rana
