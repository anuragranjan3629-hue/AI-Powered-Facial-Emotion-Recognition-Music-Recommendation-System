# MoodSync AI — Complete Project & Viva Preparation Guide

**Tagline**: "Your Mood. Your Music."  
**Domain**: Computer Vision, Deep Learning, Affective Computing, Full-Stack Web Development  
**Academic Target**: Final-Year Computer Science / AI & Data Science Engineering Project Defense  

---

## 1. Quick Start Guide

### 1.1 Running the Web Application (Vite + Express Full-Stack)
```bash
# Install dependencies
npm install

# Run the development server (Binds to 0.0.0.0:3000)
npm run dev
```
Open your browser at `http://localhost:3000`.

### 1.2 Running the Python FastAPI Backend (Optional AI Service)
```bash
# Navigate and create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install Python requirements
pip install -r backend/requirements.txt

# Run FastAPI backend with Uvicorn
uvicorn backend.app:app --host 0.0.0.0 --port 8000 --reload
```

---

## 2. Core Functional Modules

| Module | Location | Purpose |
|---|---|---|
| **Camera & Hardware Controller** | `src/hooks/useCamera.ts`, `src/components/WebcamSection.tsx` | Streams user video, handles camera switching, and takes snapshots |
| **Inference & Fallback Pipeline** | `src/services/api.ts`, `backend/services/emotion_service.py` | OpenCV face detection, 48×48 preprocessing, and 7-class Softmax classification |
| **Music Recommendation Engine** | `src/services/recommendationEngine.ts` | Valence/Arousal Euclidean distance matching with feedback adaptation |
| **Academic Viva Hub** | `src/components/AcademicVivaSection.tsx` | 30 comprehensive viva questions with examiner tips and code snippets |
| **ML CNN Architecture Visualizer** | `src/components/ArchitectureModal.tsx` | Visual topology breakdown, layer-by-layer parameter counts, and dataflow |
| **Mood Analytics Dashboard** | `src/components/MoodStats.tsx` | Pie chart, valence trends, session counts, and temporal distribution |

---

## 3. Key Scientific & Viva Defense Tips

1. **Why 48×48 Grayscale?**
   - Facial expressions are conveyed by structural landmarks (mouth corners, eyebrow furrows, eyelid shape). Single-channel reduces computational complexity by 67% without losing topological discriminative power.

2. **How does the Bounding Box work on Mirrored Video?**
   - Webcams are horizontally mirrored for natural user interaction. The face overlay calculates CSS `left: (1 - x - width) * 100%` so the box aligns accurately over the user's face in real-time.

3. **Privacy Compliance:**
   - MoodSync AI operates on in-memory volatile frames. No user images or biometric face templates are written to disk or sent to persistent external stores.
