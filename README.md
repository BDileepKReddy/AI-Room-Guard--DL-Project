🛡️ AI Room Guard – Intelligent Multi-Modal Surveillance System








🔍 Overview

AI Room Guard is an intelligent surveillance assistant that combines:

🎤 Voice activation (ASR)

👤 Face recognition (DeepFace – Facenet)

🧠 Large Language Model (Gemini)

🔊 Text-to-Speech feedback

📧 Email alert system

🎥 Video processing & annotation

It functions as a virtual AI security guard capable of detecting intruders, issuing warnings, escalating intelligently, and notifying the owner automatically.

🏗️ System Architecture
🧩 Milestone 1 – Voice Activation

Upload audio command

Speech-to-text conversion using Google Web Speech API

Detect activation phrase:
"Guard my room"

Activate Guard Mode

👤 Milestone 2 – Face Enrollment & Recognition
🔹 Enrollment

Upload image of trusted person

Extract DeepFace (Facenet) embeddings

Store embeddings in .pkl file

🔹 Recognition

Process uploaded video

Detect faces frame-by-frame

Compare embeddings using cosine similarity

Mark:

🟩 Known person

🟥 Unknown person

🚨 Milestone 3 – Intelligent Escalation System

If an unknown person persists:

🟡 Level 1 (0s)

Polite warning

Generated using Google Gemini LLM

Spoken via TTS

🟠 Level 2 (5s)

Stronger warning

🔴 Level 3 (10s)

Final warning

Email alert sent to owner

Video saved with annotations

⚙️ Technologies Used

Python

OpenCV

DeepFace (Facenet)

MediaPipe

Google Speech Recognition

Google Gemini LLM

gTTS (Text-to-Speech)

SMTP Email Protocol

Scikit-learn (Cosine Similarity)

Google Colab

🧠 Key Features

Multi-modal AI integration

Real-time face recognition

LLM-generated human-like warnings

Timed escalation logic

Automatic email alerts

Annotated video output

Trusted face enrollment system

Guard Mode voice activation

📁 Output Files

Annotated video:

/content/Files/guard_out.mp4


Face embeddings:

face_features.pkl

🚀 How to Run
1️⃣ Set Credentials (Colab userdata)
userdata.set('SENDER_EMAIL', 'your@gmail.com')
userdata.set('SENDER_PASSWORD', 'app_password')
userdata.set('OWNER_EMAIL', 'owner@gmail.com')
userdata.set('API_KEY', 'your_gemini_api_key')

2️⃣ Enroll Trusted Face
feat, name = enroll_face()
save_faces([feat], [name])

3️⃣ Activate Guard Mode

Upload voice command audio:

"Guard my room"

4️⃣ Upload Video for Monitoring

System will:

Detect faces

Escalate warnings

Send email if needed

Save annotated output video

🧠 AI Concepts Demonstrated

Multi-modal AI system design

Embedding-based recognition

Similarity metrics

LLM integration in CV pipeline

Escalation state machine

Real-time frame processing

Secure email automation

Human-AI interaction design

🎯 Future Improvements

Real-time webcam monitoring

WhatsApp alert integration

SMS notification system

Mobile app interface

Cloud deployment

Edge-device optimization

Database storage of intruder logs

👨‍💻 Author

B Dileep Kumar Reddy

