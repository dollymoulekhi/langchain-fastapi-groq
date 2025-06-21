# langchain-fastapi-groq


# 🌐 LLM Translation API with FastAPI & LangChain

This project builds a **REST API for text translation** using LangChain, FastAPI, and Groq’s Gemma2-9b-It LLM. It uses LangChain’s Expression Language (`|`) for chaining components and exposes the model as a simple HTTP endpoint via FastAPI.

---

## 🚀 What This Project Does

- Accepts user input: a **text** and **target language**
- Uses a Groq-hosted **LLM (Gemma2-9b-It)** to translate the text
- Returns the translated string via a `/chain` API endpoint
- Hosted locally with **FastAPI + Uvicorn**
- Includes `.env`-based API key management

---

## 🧱 Tech Stack

- 🧠 **LangChain** – for prompt and LLM chaining
- 🤖 **Groq / Gemma2-9b-It** – the model backend
- ⚡ **FastAPI** – lightweight web API framework
- 🌀 **Uvicorn** – ASGI server to run the app
- 🔐 **python-dotenv** – for environment variables

---

## 🛠️ How to Run

1. **Install dependencies**:
    ```bash
    pip install fastapi uvicorn langchain langserve python-dotenv langchain-groq
    ```

2. **Set your API key** in a `.env` file:
    ```
    GROW_API_KEY=your_groq_api_key_here
    ```

3. **Start the server**:
    ```bash
    python serve.py
    ```

4. **Test the API** at:
    ```
    http://127.0.0.1:8000/docs
    ```

---

## 📦 Example Request

**POST** `/chain`  
Body:
```json
{
  "language": "Spanish",
  "text": "Where is the nearest station?"
}
