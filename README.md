# MoodSync AI — AI-Powered Facial Emotion Recognition & Music Recommendation System

> **"Your Mood. Your Music."**  
> A complete, production-ready, and viva-ready engineering application bridging Computer Vision, Convolutional Neural Networks, and Affective Music Recommendations.

---

## 🌟 Key Highlights

- 🎭 **Real-Time Facial Expression Recognition**: 7-class emotion classification (Happy, Sad, Angry, Neutral, Surprise, Fear, Disgust) with OpenCV face localization and confidence scoring.
- 🎵 **Affective Music Recommendation Engine**: Continuous 2D Valence-Arousal space matching based on Russell's Circumplex Model with language (English, Hindi, Spanish, Instrumental) and genre filtering.
- 🎓 **Comprehensive Academic Viva Hub**: 30 technical defense questions with examiner tips, mathematical proofs, and code snippets designed for university project evaluation.
- 📊 **Interactive Mood Analytics**: Session metrics, emotional trends, distribution pie charts, and mood transition analysis.
- 🔒 **Privacy-First Architecture**: Ephemeral in-memory stream processing; zero facial image persistence or storage.
- ⚡ **Offline-Resilient Fallback Mode**: Ensures 100% demo uptime under any network or GPU hardware conditions.

---

## 🚀 Getting Started

### Quick Start (Web App)
```bash
# 1. Install dependencies
npm install

# 2. Run the development server (port 3000)
npm run dev

# 3. Build for production
npm run build
```

### Quick Start (Python AI Service)
```bash
# 1. Install dependencies
pip install -r backend/requirements.txt

# 2. Start FastAPI server
uvicorn backend.app:app --host 0.0.0.0 --port 8000 --reload
```

---

## 📁 Repository Structure

```text
├── src/
│   ├── components/      # React UI components (Webcam, EmotionCard, MusicList, Viva Hub, etc.)
│   ├── data/            # Music catalog & 30 Academic viva questions
│   ├── hooks/           # Hardware camera & state management hooks
│   ├── services/        # Recommendation engine & API service layer
│   ├── types.ts         # TypeScript interfaces
│   ├── App.tsx          # Main entry component
│   └── main.tsx         # React root initialization
├── backend/
│   ├── services/        # CNN, DeepFace & Fallback inference engines
│   ├── utils/           # Face detection, preprocessing, validation & logging
│   ├── tests/           # Pytest test suite for health, predict & recommendations
│   └── app.py           # FastAPI application
├── ml/
│   ├── src/             # CNN model architecture, data loader, train, evaluate & predict
│   ├── notebooks/       # 4 Jupyter notebooks (exploration, preprocessing, training, evaluation)
│   └── dataset/         # Directory for FER-2013 CSV
├── docs/                # Academic documentation (Architecture, API, Model, Viva, Presentation)
├── server.ts            # Full-stack Node/Express server for web deployment
├── Dockerfile           # Production container build
└── docker-compose.yml   # Multi-service container orchestration
```

---

## 📜 Scientific Disclaimer
MoodSync AI estimates facial expressions from visual cues. It does not determine a person's actual emotional or mental state.

---

## 📄 License
This project is licensed under the Apache 2.0 License.
