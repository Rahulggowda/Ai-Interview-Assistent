# 🎤 AI-Powered Conversational Interview Assistant

An AI-powered mock interview platform that simulates real technical interviews using conversational AI, voice interaction, speech-to-text, and text-to-speech. The assistant asks adaptive questions, remembers previous responses, and provides detailed personalized feedback at the end of the interview.

---

## 🚀 Features

* 🎯 Multi-subject interview support

  * Python
  * HTML
  * CSS
  * English
  * Generative AI
  * Self Introduction

* 🤖 AI-powered interviewer using Google Gemini

* 🧠 Conversational memory using LangGraph

* 🎙️ Voice recording through the browser

* 📝 Speech-to-Text using AssemblyAI

* 🔊 Text-to-Speech streaming using Murf AI Falcon

* 💬 Context-aware follow-up questions

* 📊 Detailed interview feedback with scoring

* 🌐 Responsive web interface

---

## 🛠️ Tech Stack

### Frontend

* HTML
* CSS
* JavaScript

### Backend

* Python
* Flask
* Flask-CORS

### AI & APIs

* Google Gemini
* LangChain
* LangGraph
* AssemblyAI
* Murf AI Falcon

---

## 📂 Project Structure

```
InterviewAssistant/
│
├── backend/
│   ├── app.py
│   ├── .env
│   ├── requirements.txt
│   └── ...
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   ├── script.js
│   └── ...
│
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/interview-assistant.git

cd interview-assistant
```

---

### 2. Create Virtual Environment

Windows

```bash
python -m venv venv
venv\Scripts\activate
```

Mac/Linux

```bash
python3 -m venv venv

source venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

or

```bash
pip install flask flask-cors python-dotenv langchain langgraph langchain-google-genai assemblyai requests
```

---

## 🔑 Environment Variables

Create a `.env` file inside the backend folder.

```env
GOOGLE_API_KEY=your_google_gemini_api_key

ASSEMBLYAI_API_KEY=your_assemblyai_api_key

MURF_API_KEY=your_murf_api_key
```

---

## ▶️ Run the Application

Start the Flask backend

```bash
cd backend

python app.py
```

Open the frontend

```
frontend/index.html
```

or run it using VS Code Live Server.

---

## 🏗️ Application Workflow

### 1. Start Interview

* User selects a subject.
* Frontend sends the subject to `/start-interview`.
* Gemini greets the user.
* First interview question is generated.
* Murf AI converts the question into speech.
* Audio is streamed back to the browser.

---

### 2. Submit Answer

* User records an answer.
* Audio is uploaded to `/submit-answer`.
* AssemblyAI converts speech to text.
* Answer is stored in LangGraph memory.
* Gemini generates the next contextual question.
* Murf AI streams the next question as audio.

---

### 3. End Interview

* User clicks **End Interview**.
* Backend accesses the complete interview history.
* Gemini evaluates the conversation.
* Structured JSON feedback is generated.
* Frontend displays:

  * Interview score
  * Strengths
  * Areas for improvement

---

## 🧠 AI Memory

The application uses **LangGraph InMemorySaver** to preserve interview context.

Benefits include:

* Context-aware conversations
* Natural follow-up questions
* Better interview experience
* Personalized feedback

---

## 🔄 API Endpoints

### Start Interview

```
POST /start-interview
```

Request

```json
{
  "subject": "Python"
}
```

---

### Submit Answer

```
POST /submit-answer
```

Form Data

```
audio : answer.webm
```

Returns

* Next interview question
* Streaming audio
* Current question number

---

### Get Feedback

```
POST /get-feedback
```

Response

```json
{
  "subject": "Python",
  "candidate_score": 4,
  "feedback": "You explained Python concepts clearly and provided practical examples.",
  "areas_of_improvement": "Try explaining time complexity with more confidence and use more technical terminology."
}
```

---

## 📦 Major Libraries

| Library       | Purpose               |
| ------------- | --------------------- |
| Flask         | Backend API           |
| Flask-CORS    | Cross-Origin Requests |
| LangChain     | AI Agent              |
| LangGraph     | Conversation Memory   |
| Google Gemini | LLM                   |
| AssemblyAI    | Speech-to-Text        |
| Murf AI       | Text-to-Speech        |
| Requests      | HTTP Requests         |
| python-dotenv | Environment Variables |

---

## 🎯 Key Functionalities

* Interactive mock interviews
* AI remembers previous responses
* Dynamic follow-up questions
* Voice-based communication
* Real-time speech synthesis
* Automatic speech transcription
* Detailed interview evaluation
* JSON-based feedback generation

---

## 📸 Future Improvements

* User authentication
* Interview history
* Resume-based interview generation
* Video interview support
* Multiple interviewer personalities
* Difficulty levels
* Progress analytics dashboard
* Database integration
* Cloud deployment
* Real-time emotion analysis

---

## 📚 Learning Outcomes

This project demonstrates:

* Flask REST API development
* Prompt Engineering
* LangChain Agents
* LangGraph Memory
* Speech-to-Text integration
* Text-to-Speech streaming
* Conversational AI
* Browser audio recording
* AI-powered feedback generation
* End-to-end full-stack AI application development

---

## 👨‍💻 Author

**Rahul Gowda**

Full Stack Developer | AI Enthusiast

---

## ⭐ Acknowledgements

* Google Gemini
* LangChain
* LangGraph
* AssemblyAI
* Murf AI
* Flask
