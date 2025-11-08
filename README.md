# 🎵 ZYNO: Music Recommendation System Based on Facial Emotion Recognition

Zyno is a music recommendation system that uses **facial emotion recognition (FER)** to suggest songs matching the user’s current mood.  
It integrates **machine learning**, **computer vision**, and **DevOps automation** to create an interactive, intelligent, and scalable system.

---

## 🚀 Project Overview

Zyno combines three main components:

- **Frontend (React.js)** — The user interface for emotion detection and music display.  
- **Backend (Flask/Python)** — Handles emotion classification, API logic, and communication between models and frontend.  
- **Models (CNN + Emotion Recognition + Recommendation Engine)** — Detects facial emotions in real-time and maps them to suitable playlists or music categories.

---

## 🎯 Features

- Real-time emotion detection using webcam input  
- CNN-based emotion classification (Happy, Sad, Angry, Neutral, etc.)  
- Dynamic song recommendations based on detected emotion  
- Configurable model and playlist parameters  
- Integrated CI/CD pipelines using GitHub Actions for linting, testing, and containerization  

---

## 🧠 How It Works

1. **Camera Input** — The webcam captures live facial expressions.  
2. **Emotion Detection** — `realtimedetection.py` processes frames and classifies emotions using the CNN model.  
3. **Music Recommendation** — Detected emotions are sent to the Flask backend, which queries the recommendation model to return songs or playlists corresponding to the mood.  
4. **Frontend Display** — The React frontend receives and displays the music recommendations instantly.  

**Example Flow:**  
😄 → “Happy” emotion detected → fetches upbeat playlist → plays songs in UI  

---

## ⚙️ Project Structure
```
ScrumProject/
├── FER/
│ └── Zyno/
│ ├── Music-Recommendation-App/ # React frontend
│ │ ├── src/ # React source files
│ │ ├── public/ # Public assets (songs, images, etc.)
│ │ ├── package.json # NPM package configuration
│ │ ├── package-lock.json
│ │ ├── tailwind.config.js
│ │ ├── postcss.config.js
│ │ ├── next.config.js
│ │ ├── README.md
│ │ └── ... # Other frontend files
│ │
│ └── face_emotion_detection/ # Flask backend
│ ├── backend.py # Main Flask app
│ ├── realtimedetection.py # Real-time detection script
│ ├── models/ # ML models directory
│ ├── requirements.txt # Python dependencies
│ └── ... # Other backend files
│
└── ...
```
Copy code




---

## 🖥️ How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/suvi-running-as-root/YOUR_REPOSITORY.git
cd ScrumProject/FER/Zyno/
2. Run the Frontend
bash
Copy code
cd Music-Recommendation-App
npm install
npm run dev
The React app will start on a local development server (typically http://localhost:5173).

3. Run the Backend
Open a new terminal window:

bash
Copy code
cd face_emotion_detection
pip install -r requirements.txt
python backend.py
This starts the Flask backend, usually on http://127.0.0.1:5000.

4. Configure Model Settings
In realtimedetection.py, you can modify which model is used for detection and how it behaves.

python
Copy code
# Example inside realtimedetection.py

# Choose between available models
(example)
model_1 = 'models/emotion_cnn.h5'
model_2 = 'models/emotion_vgg.h5'
model_3 = 'models/emotion_mobilenet.h5'

# Select active model
active_model = model_2
You can switch between the three models or adjust parameters such as frame rate or detection confidence.

🧩 Tech Stack
Frontend: React.js, Vite, Tailwind CSS

Backend: Flask (Python)

ML Models: CNN-based Emotion Detection

DevOps: GitHub Actions (Testing, Linting, Docker Build)

Testing: pytest, ESLint, Pylint

Containerization: Docker-ready setup

🔄 CI/CD Pipeline Overview
The project uses GitHub Actions workflows for automation:

Unit Testing Workflow — Runs backend and model tests on every push.

Lint Check Workflow — Enforces code standards for Python and JavaScript.

Container Build Workflow — Builds and pushes Docker images for deployment.

Comprehensive Test Workflow — Validates endpoints and model outputs.

🧑‍💻 Contributors
Manish M G
Shreya M G
Spoorthi S
Suviksha V B

Under the guidance of Harikumar Santhibhavan,
Assistant Professor, School of Computer Science and Engineering, RV University



Assistant Professor, School of Computer Science and Engineering, RV University
