# LangGraph AI Chatbot

LangGraph AI Chatbot is a powerful chatbot application built using FastAPI, LangGraph, and LangChain. It leverages large language models (LLMs) like Llama3 and Mixtral, integrated with the Tavily search tool, to provide intelligent responses. The frontend is designed with Streamlit for an interactive and sleek user experience.

## 🚀 Features

- **FastAPI Backend**: Efficient API for handling chat requests.
- **LangGraph & LangChain**: Enables intelligent conversation processing.
- **Multiple LLM Models**: Supports `llama3-70b-8192` and `mixtral-8x7b-32768`.
- **Tavily Search Integration**: Fetches relevant search results.
- **Streamlit UI**: Interactive, customizable, and responsive frontend.
- **Docker Support**: Easily deploy the application with Docker.
- **Custom Themes**: Light & Dark mode for enhanced user experience.

## 🛠️ Installation & Setup

### 1️⃣ Clone the Repository

```sh
https://github.com/ToufiqQureshi/ai-agent-with-langraph.git
```

### 2️⃣ Create a Virtual Environment & Install Dependencies

```sh
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt
```

### 3️⃣ Set Environment Variables

Create a `.env` file and add your API keys:

```
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

Alternatively, set them in your terminal:

```sh
export GROQ_API_KEY=your_groq_api_key
export TAVILY_API_KEY=your_tavily_api_key
```

### 4️⃣ Run the Application

#### Start FastAPI Backend

```sh
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

#### Start Streamlit Frontend

```sh
streamlit run ui.py
```

## 🐳 Deploy with Docker

### 1️⃣ Build the Docker Image

```sh
docker build -t langgraph-chatbot .
```

### 2️⃣ Run the Docker Container

```sh
docker run -p 8000:8000 -p 8501:8501 langgraph-chatbot
```

## 🔧 API Usage

### Chat Endpoint

**URL:** `http://127.0.0.1:8000/chat`

**Request Body:**

```json
{
  "system_prompt": "Define your AI agent",
  "model_name": "llama3-70b-8192",
  "messages": ["Hello, how can you help me?"]
}
```

**Response:**

```json
{
  "messages": [
    { "type": "ai", "content": "Hello! How can I assist you today?" }
  ]
}
```

## 🖥️ UI Features

- **Send Messages**: Chat with AI.
- **Select Model**: Choose from `llama3-70b-8192` or `mixtral-8x7b-32768`.
- **Define AI Behavior**: Custom system prompts.
- **Dark & Light Themes**: Switch between modes for a better experience.

## 📜 Project Structure

```
langgraph-chatbot/
│── main.py          # FastAPI backend
│── ui.py            # Streamlit frontend
│── requirements.txt # Dependencies
│── Dockerfile       # Docker setup
│── .env             # Environment variables (ignored in Git)
```

## 📜 License

This project is licensed under the MIT License.

## 📩 Contact

For support or inquiries, contact: [toufiqqureshi651@gmail.com](mailto\:toufiqqureshi651@gmail.com)

Enjoy using LangGraph AI Chatbot! 🎉

