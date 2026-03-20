# 💬 BlenderBot Chatbot Web Application

A ChatGPT-like web application powered by Facebook's BlenderBot model.
Built with a Flask backend and a custom HTML/CSS/JavaScript frontend.

## 🌐 Live Demo
👉 [Try it on Hugging Face Spaces](https://huggingface.co/spaces/Mae-Mae/blenderbot-chatbot)

## 📖 About
This project demonstrates how to build a full-stack AI chatbot web 
application from scratch. The Flask backend hosts the BlenderBot model 
and exposes a REST API endpoint. The custom frontend communicates with 
the backend to create a seamless chat experience similar to ChatGPT.

## ⚠️ Important Note on Running This App
This app runs on a **temporary IBM Skills Network lab environment**.
The URL is only active while the lab session is open and Flask is running.

To run this app permanently you can deploy it to a cloud service like:
- **Hugging Face Spaces** ✅ [Live here](https://huggingface.co/spaces/Mae-Mae/blenderbot-chatbot)
- **Render.com** (free Flask hosting)
- **Railway.app** (free Flask hosting)

## 🔧 Run Locally or in IBM Lab
```bash
# Clone the repo
git clone https://github.com/soriamaegan-dev/blenderbot-chatbot
cd blenderbot-chatbot

# Create virtual environment
pip3 install virtualenv
virtualenv my_env
source my_env/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the server
flask run
```

Then open your browser at `http://127.0.0.1:5000`

## 🔁 How to Restore After Lab Session Ends
Every time you open a new IBM lab session the environment is wiped.
To restore your chatbot:

1. Open a new lab session
2. Clone your repo:
```bash
git clone https://github.com/soriamaegan-dev/blenderbot-chatbot
```
3. Install dependencies:
```bash
cd blenderbot-chatbot
pip install -r requirements.txt
```
4. Run the server:
```bash
flask run
```

## 🚀 Features
- Real-time chat interface with message bubbles
- Multi-turn conversation with memory of chat history
- Powered by Facebook BlenderBot-400M-distill
- Custom HTML/CSS/JavaScript frontend
- Flask REST API backend
- CORS enabled for cross-origin requests
- Responsive and clean chat UI

## 🛠️ Tech Stack
- **Model**: facebook/blenderbot-400M-distill
- **Backend**: Python, Flask, Flask-CORS
- **Frontend**: HTML, CSS, JavaScript
- **Libraries**: Hugging Face Transformers, PyTorch

## 📂 Project Structure
```
blenderbot-chatbot/
├── app.py                 # Flask backend server
├── requirements.txt       # Project dependencies
├── static/
│   ├── script.js         # Frontend JavaScript
│   └── css/
│       └── style.css     # Frontend styles
└── templates/
    └── index.html        # Chat interface webpage
```

## 🔌 API Endpoint
```
POST /chatbot
Content-Type: application/json

{
    "prompt": "Hello, how are you today?"
}
```

Response:
```
I am doing well today. How are you?
```

## 💬 How It Works
1. User types a message in the chat interface
2. JavaScript sends a POST request to `/chatbot`
3. Flask receives the request and passes it to BlenderBot
4. BlenderBot generates a response using conversation history
5. Response is returned and displayed in the chat interface

## 💾 Why GitHub?
GitHub permanently saves your code so it's never lost when the lab 
session ends. Think of it as:

| | Description |
|--|--|
| **GitHub** | 📦 Saves your code permanently |
| **IBM Lab** | 🖥️ Temporary workspace — wiped when session ends |
| **HF Spaces** | 🌐 Runs your code with a permanent URL |

## 🧠 Model Used
| Model | Description |
|-------|-------------|
| `facebook/blenderbot-400M-distill` | Open source conversational AI by Facebook |

## 📚 What I Learned
- How to build a Flask REST API backend
- How to integrate LLMs into a web application
- How to build a custom chat UI with HTML/CSS/JS
- How to handle CORS in Flask
- How to maintain conversation history in a chatbot
- How to save and restore projects using GitHub

## 🎓 Built As Part Of
IBM AI Developer Professional Certificate — Coursera
Lab: Integrating Your Chatbot into a Web Application
