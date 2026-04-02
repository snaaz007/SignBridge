# SignBridge
SignBridge is an web application which allows seamless conversation between people who know sign language and who doesnt know it without requirement of third person
# 🚀 SignBridge – AI Powered Sign Language Communication System

## 📌 Overview

SignBridge is an AI-powered system that converts hand gestures into meaningful speech and text in real-time. It integrates:

* ✋ Hand Gesture Recognition (ML Model)
* 🧠 AI Sentence Generation (Google Gemini API)
* 🔊 Text-to-Speech (pyttsx3 / ElevenLabs optional)
* 🌐 Backend API (FastAPI)
* 📷 Live Camera Streaming

This project aims to bridge the communication gap for people using sign language.

---

## 🎯 Features

* ✅ Real-time hand gesture detection using webcam
* ✅ Converts gestures → meaningful sentences
* ✅ Multilingual sentence generation using Gemini
* ✅ Emergency alert system (FIST gesture 🚨)
* ✅ Live video streaming via backend
* ✅ Speech output for detected gestures
* ✅ REST API for frontend integration

---

## 🏗️ Project Structure

```
SignBridge_ML_improved/
│
├── data/                     # Gesture dataset (.npy files)
├── model.pkl                # Trained ML model
├── label_encoder.pkl        # Label encoder
├── alarm.wav                # Emergency alarm sound
│
├── train_model.py           # Model training script
├── collect_data.py          # Data collection script
├── test_model.py            # ML testing (webcam)
├── backend.py               # FastAPI backend
├── ml_logic.py              # Prediction logic
│
├── .env                     # API keys (DO NOT SHARE)
├── requirements.txt
└── README.md
```

---

## ⚙️ Setup Instructions

### 1️⃣ Create Environment

```bash
conda create -n signbridge python=3.10
conda activate signbridge
```

---

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

If missing:

```bash
pip install fastapi uvicorn mediapipe opencv-python pyttsx3 python-dotenv google-generativeai
```

---

### 3️⃣ Add API Key

Create `.env` file:

```
GEMINI_API_KEY=your_api_key_here
```

---

### 4️⃣ Run Backend

```bash
python backend.py
```

---

## 🌐 API Endpoints

### 🔹 Health Check

```
GET /health
```

---

### 🔹 Video Feed (Webcam)

```
GET /video_feed
```

👉 Open in browser:

```
http://localhost:8000/video_feed
```

---

### 🔹 Predict Gesture

```
POST /predict
```

Example body:

```json
{
  "language": "English"
}
```

---

## 🧠 How It Works

1. Webcam captures hand gestures
2. Mediapipe extracts landmarks
3. ML model predicts gesture label
4. Backend converts label → intent
5. Gemini converts intent → natural sentence
6. System speaks output

---

## 🚨 Emergency Feature

Gesture: **FIST**

* Triggers alert message
* Plays alarm sound
* Speaks emergency sentence

---

## 🌍 Multilingual Support

* Uses Gemini API
* Converts gestures into different languages

Example:

```
HELLO → "Hello, how are you?"
HELLO (Hindi) → "नमस्ते, आप कैसे हैं?"
```

---

## ⚠️ Important Notes

* Do NOT share `.env` file
* Do NOT expose API keys
* Ensure good lighting for gesture detection
* Use distinct gestures for better accuracy

---

## 🚀 Future Improvements

* 📱 Mobile app integration
* 🧠 Better gesture dataset (ISL standard)
* 🔊 Full ElevenLabs voice integration
* 🌐 Frontend UI dashboard
* 📡 Real-time communication system

---

## 🏆 Hackathon Value

This project demonstrates:

* AI + ML integration
* Real-world impact (accessibility)
* Multimodal system (vision + speech)
* Scalable architecture

---

## 👩‍💻 Author
Mariya Anjum
Sushma Kumari
Syeda Naazima Unnisa

---

## ⭐ Final Note

This is not just a project — it's a step toward inclusive communication using AI.

---
