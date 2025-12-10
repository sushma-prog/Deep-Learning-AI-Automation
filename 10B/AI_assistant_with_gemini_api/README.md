# 🌟 Mini AI Coding Assistant (Gemini 2.5 Flash)

A simple and beginner-friendly **AI coding assistant** built using **Google Gemini 2.5 Flash**.
This notebook can generate code, explain code, summarize datasets, write documentation, and answer general questions.

---

## 🚀 Features

* **Generate Python code** for any task
* **Explain code** line-by-line
* **Summarize datasets** in simple language
* **Create documentation/README files**
* **General AI Q&A support**
* **Interactive chat mode** (type `exit` to quit)

---

## 🧩 How It Works

The notebook includes:

1. Importing libraries and setting up environment variables
2. Listing all available Gemini models
3. Initializing `models/gemini-2.5-flash`
4. Core function `ask_gemini()`
5. Tools for:

   * Code generation
   * Dataset summarization
   * Documentation writing
   * Code explanation
   * General chat
6. A final chat loop for interactive conversations

---

## 🔑 API Key Setup (Colab)

```python
import os
api_key = input("Enter your Google Gemini API Key: ")
os.environ["GOOGLE_API_KEY"] = api_key
```

---

## 🛠 Model Initialization

```python
import google.generativeai as genai

api_key = os.getenv("GOOGLE_API_KEY")
genai.configure(api_key=api_key)

model = genai.GenerativeModel("models/gemini-2.5-flash")
```

---

## 💬 Start Chatting

```python
print("🤖 AI Assistant Ready! Type 'exit' to quit.")

while True:
    user_input = input("You: ")
    if user_input.lower() == "exit":
        break
    print("Assistant:", ask_gemini(user_input))
```

---

## 📂 Project Files

* `ai_assistant.ipynb` — Full notebook
* `README.md` — Documentation

---

## 👩‍💻 Author

Built by **Sushma** while learning AI, Python, and Gemini API.

---
