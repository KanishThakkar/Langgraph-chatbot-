# 🤖 LangGraph Chatbot with Multi-Thread Memory

A conversational AI chatbot built using **LangGraph**, **LangChain**, **Groq LLM (Llama 3.3 70B)**, and **Streamlit**.

The chatbot supports:

- 💬 Real-time AI conversations
- 🧠 Conversation memory using LangGraph Checkpointer
- 🔄 Multiple chat sessions (thread-based conversations)
- ⚡ Streaming AI responses
- 🎨 Clean Streamlit user interface
- 🚀 Fast inference through Groq API

---

## 🏗️ Architecture

```text
User
 │
 ▼
Streamlit Frontend
 │
 ▼
LangGraph Workflow
 │
 ▼
Chat Node
 │
 ▼
Groq Llama 3.3 70B
 │
 ▼
Response
```

### Workflow

```text
START
  │
  ▼
Chat Node
  │
  ▼
 END
```

The chatbot uses a simple LangGraph state machine where:

- User messages are stored in the graph state
- Previous messages are maintained through thread IDs
- The LLM receives the entire conversation context
- Responses are streamed back to the UI

---

## 🚀 Features

### 💬 Multi-Conversation Support

Create multiple chat sessions and switch between them from the sidebar.

### 🧠 Conversation Memory

Each conversation is assigned a unique thread ID, allowing the chatbot to remember previous messages within that conversation.

### ⚡ Streaming Responses

Responses are streamed token-by-token for a more natural user experience.

### 🔄 Thread-Based State Management

LangGraph maintains conversation state independently for every chat session.

### 🎨 Interactive Streamlit Interface

- Clean and responsive UI
- Sidebar conversation history
- New Chat functionality
- Real-time AI responses

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|----------|
| LangGraph | Workflow orchestration |
| LangChain | LLM integration |
| Groq API | LLM inference |
| Llama 3.3 70B | Language model |
| Streamlit | Frontend UI |
| Python | Backend development |

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/langgraph-chatbot.git
cd langgraph-chatbot
```

### 2️⃣ Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows**

```bash
venv\Scripts\activate
```

**Linux / Mac**

```bash
source venv/bin/activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key
```

Get your API key from:

https://console.groq.com/

---

## ▶️ Run the Application

```bash
streamlit run app.py
```

## 💡 Example Usage

<img width="1450" height="697" alt="image" src="https://github.com/user-attachments/assets/bd7e64b3-280f-4382-a7ec-283b3579a33a" />


## 📈 Future Improvements

- PostgreSQL Checkpointer
- Long-Term Memory
- Retrieval-Augmented Generation (RAG)
- Tool Calling
- MCP Server Integration
- User Authentication
- Chat Export Functionality
- Vector Database Support
- Docker Deployment
- AWS/GCP/Azure Deployment

---

## 🎯 Learning Outcomes

This project demonstrates:

- LangGraph Fundamentals
- Stateful AI Applications
- Conversation Memory Management
- LLM Streaming
- Multi-Session Chat Architecture
- Streamlit Application Development
- LangChain Integration
- Production-Oriented AI Workflow Design

---

