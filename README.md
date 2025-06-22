# -LLM-Fine-Tuning-Mini-Project-Hinglish-Voice-AI
building a Voice-AI that handles code-switched (Hinglish) dialogue. Your task is to design and prototype a small fine-tuning workflow that adapts a base LLM to Hinglish patterns.
LLM-Fine-Tuning-Mini-Project-Hinglish-Voice-AI/
# 🧠 LLM-Fine-Tuning-Mini-Project-Hinglish-Voice-AI

A mini AI voice assistant that understands and responds in **Hinglish** (Hindi + English). This project demonstrates **LLM fine-tuning**, **speech-to-text**, **text generation**, and **text-to-speech** pipelines — deployed via **FastAPI** and **Docker**.
---
## 🚀 Overview
This project combines three AI domains:
- 🎤 **STT (Speech to Text)** using OpenAI Whisper
- 🧠 **LLM Text Generation** using a fine-tuned Hugging Face model
- 🔊 **TTS (Text to Speech)** using Coqui TTS or gTTS
You speak in Hinglish → it transcribes → generates an intelligent response → and speaks it back.
- 🎤 Converts Hinglish speech to text using **OpenAI Whisper**
- 🧠 Processes and replies using a **fine-tuned LLM**
- 🔊 Speaks back the response using **Text-to-Speech (TTS)**
- 🧪 Deployed via **FastAPI**, **Docker**, and ready for cloud
---
## 🎯 Use Cases
- Voice-based Hinglish assistant for mobile/web apps  
- Educational, smart Q&A agents in regional languages  
- LLM testing/fine-tuning for multilingual low-resource NLP
---
# 🧠 LLM-Fine-Tuning-Mini-Project-Hinglish-Voice-AI

An end-to-end **Hinglish Voice Assistant** that listens, thinks, and speaks. This project showcases **LLM fine-tuning**, **speech recognition**, **text generation**, and **text-to-speech** — all wrapped in a deployable FastAPI application.

---
This assistant can understand questions like:
> **"Kal Hyderabad ka weather kaisa hai?"**  
And respond with:
> **"Kal Hyderabad ka weather dhup bhara rahega, 35°C tak ja sakta hai."**

---

## ✅ Skills Applied

| Category | Skills |
|---------|--------|
| 🧠 AI/ML | LLM fine-tuning, Tokenization, Prompt Engineering |
| 🧬 NLP | Hinglish language modeling, Text generation |
| 🎤 Voice | Speech-to-Text (STT), Text-to-Speech (TTS), audio I/O |
| 🧰 MLOps | Model management, LoRA (PEFT), Hugging Face, ML pipeline |
| 💻 Backend | API creation (FastAPI), Python multiprocessing |
| 🐳 Deployment | Docker, RESTful endpoints, service containerization |
---
## 🔄 Process Breakdown

### 1. 📊 Dataset Creation
- Collected Hinglish question-answer pairs
- Format: `prompt → response`

### 2. 🔧 LLM Fine-Tuning
- Base model: `flan-t5-small` or `falcon-rw-1b`
- Technique: Lightweight **LoRA** fine-tuning using `PEFT`
- Tools: Hugging Face `transformers`, `datasets`, `accelerate`, `wandb`

### 3. 🎤 Voice Integration
- STT: Whisper model (`base.en`) or Google Speech API
- TTS: Coqui TTS / gTTS for generating natural Hinglish voice

### 4. 🧠 LLM Inference
- Clean + tokenize input text
- Generate response using fine-tuned model

### 5. 🌐 API Deployment
- FastAPI backend serves endpoints for:
  - `/stt` → Audio → Text
  - `/generate` → Text → Response
  - `/tts` → Response → Audio

### 6. 🐳 Containerization
- Dockerized app for production-ready deployment
- Easily deployable on Render, Railway, Hugging Face Spaces

---
## 🗂️ Project Structure
├── app/
│   ├── main.py                # FastAPI app
│   ├── llm_core.py            # Fine-tuned LLM interaction
│   ├── stt.py                 # Speech-to-text (e.g., Whisper)
│   ├── tts.py                 # Text-to-speech
│   └── utils.py               # Preprocessing, cleaning
├── data/
│   └── hinglish_dataset.csv   # Custom fine-tuning dataset
├── model/
│   └── fine_tuned_model/      # Saved model checkpoint
├── requirements.txt
├── Dockerfile
├── .gitignore
└── README.md


---

## 📦 Technologies Used

| Layer | Tools |
|------|-------|
| LLM | Hugging Face Transformers, LoRA (PEFT), Datasets |
| STT | Whisper (OpenAI), Google Speech Recognition |
| TTS | Coqui TTS, gTTS |
| Backend | FastAPI, Uvicorn |
| Deployment | Docker, GitHub |
| Dev Tools | Python, PyTorch, VS Code, WandB |

---

## 💻 How to Run

### 1️⃣ Install dependencies
```bash
pip install -r requirements.txt
uvicorn app.main:app --reload
docker build -t hinglish-voice-ai .
docker run -p 8000:8000 hinglish-voice-ai

---

Would you like me to now:
- Generate the code files like `main.py`, `llm_core.py`, `tts.py`?
###
- Provide the sample Hinglish dataset for fine-tuning?
- Help you deploy it live on Render or Hugging Face Spaces?

Let me know, and I’ll walk you through the full setup, end-to-end.


