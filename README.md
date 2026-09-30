# FinAssist AI – Intelligent Payment Support Agent

An AI-powered payment support agent built using LLM, RAG, database tools, and deterministic business logic to automate common payment-support tasks.

##  Overview

**FinAssist AI** is an intelligent payment-support application that allows users to interact with an AI agent through a web interface.

The system combines **Large Language Models (LLMs), Retrieval-Augmented Generation (RAG), database integration, and agentic tools** to provide accurate and context-aware responses for payment-related queries.

### Key Capabilities

* 💬 Natural-language payment support
* 🔎 Transaction status lookup
* 👤 Customer information retrieval
* 💰 Refund eligibility verification
* 🎫 Support ticket creation
* 📚 RAG-based knowledge retrieval
* 🔐 User authentication
* ⚡ Streaming AI responses
* 🖥️ Responsive React-based interface

## 🏗️ Architecture

```text
User
 │
 ▼
React Frontend
 │
 ▼
FastAPI Backend
 │
 ▼
AI Agent
 ├── LLM (Ollama)
 ├── RAG / Vector Store
 ├── Database Tools
 │    ├── Transaction Status
 │    ├── Customer Details
 │    ├── Refund Eligibility
 │    └── Support Tickets
 │
 ▼
Context-Aware Response
 │
 ▼
React UI
```

## 🛠️ Tech Stack

**Frontend**

* React
* Vite
* JavaScript
* Tailwind CSS
* React Markdown
* Lucide React

**Backend**

* Python
* FastAPI
* Pydantic
* Uvicorn

**AI / ML**

* LLM with Ollama
* Qwen3
* Retrieval-Augmented Generation (RAG)
* Vector Store
* Prompt-based Agentic Workflow

**Database & Tools**

* SQLite
* Python database integration
* Tool-based transaction and customer operations

**Authentication**

* JWT-based authentication

## 🤖 AI Agent Workflow

1. User submits a payment-related query.
2. FastAPI receives and processes the request.
3. The AI agent identifies the required action.
4. Relevant knowledge is retrieved through **RAG** when required.
5. Database tools are called for transactional information.
6. Deterministic business logic handles operations such as refund eligibility.
7. The LLM generates a concise response.
8. The response is streamed back to the React frontend.


## 📸 Demo

### AI Payment Support Interface

![FinAssist AI Demo](screenshots/finassist-demo.png)

> The screenshot demonstrates the application's chat interface and AI-powered payment-support workflow.


## ⚙️ Setup

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd FinAssist-AI
```

### 2. Backend

```bash
cd backend

python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt

uvicorn main:app --reload
```

### 3. Start Ollama

Install and run Ollama, then pull the required model:

```bash
ollama pull qwen3:4b
```

Make sure Ollama is running before starting the application.

### 4. Frontend

```bash
cd frontend

npm install
npm run dev
```

Open the local URL displayed by Vite in your browser.

## 🔑 Environment Variables

Create a `.env` file and configure the required application settings:

```env
OLLAMA_MODEL=qwen3:4b
OLLAMA_HOST=http://localhost:11434
```


## 🎯 Project Highlights

* Integrated **LLM + RAG + Agentic AI** into a real-world payment-support use case.
* Implemented **tool calling** for transaction, customer, refund, and ticket operations.
* Used **deterministic business logic** for critical payment decisions.
* Implemented **streaming responses** for a responsive user experience.
* Built a separate **React frontend and FastAPI backend**.
* Added authentication and structured API models.

