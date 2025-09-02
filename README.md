# AI Exercise Trainer 🏋️‍♂️

[![Python](https://img.shields.io/badge/python-3.x-blue)](https://www.python.org/) [![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

An AI-powered personal trainer that tracks and counts repetitions for exercises in real-time using **MediaPipe** for pose detection and a **custom LSTM model** for exercise classification.  

---

## Features ✨

- **Real-time Pose Detection:** Tracks 33 body landmarks.  
- **Exercise Classification:** Recognizes `bicep_curl`, `push_up`, `squat`, `shoulder_press`.  
- **Repetition Counter:** Counts reps automatically using joint angles.  
- **Performance Metrics:** Displays FPS for monitoring.  

---

## Quick Start 🚀

### Prerequisites

- Python 3.x  
- Webcam  

### Installation & Running the Application

1. Clone the repository:

```bash
git clone https://github.com/DevPatel1106/Repo_github.git
cd Repo_github
```
2. Install dependencies and Run:

```bash
pip install -r requirements.txt
python main.py
```

### How It Works ⚙️

- Capture Video: Webcam feed processed in a loop.
- Pose Detection: Extracts 33 (x, y) landmark coordinates.
- Sliding Window: Last 30 frames fed into the LSTM model.
- Exercise Prediction: Model predicts the exercise class.
- Repetition Counting: Detects “up” & “down” stages using joint angles.

---

### Visual Example 🖼️
Real-Time Pose Detection
<img width="777" height="428" alt="image" src="https://github.com/user-attachments/assets/a87266aa-4b8b-48b3-bff4-a01f55e1a273" />
- Tracks 33 key body landmarks using MediaPipe.
- Displays predicted exercise class, rep count, and FPS.
### Tip: For best accuracy, ensure proper lighting and full-body visibility in the webcam frame.

---

### Project Structure 📁

|- main.py – Runs video capture & integrates modules.

|- ExerciseAiTrainer.py – Core logic for classification & rep counting.

|- PoseModule2.py – Pose detection & angle calculations.

|- AiTrainer_utils.py – Utilities (image resizing, FPS display).

|- ML.ipynb – Notebook for model training.

|- requirements.txt – Python dependencies.

|_ lstm_model.keras, scaler.joblib, label_encoder.joblib – Pre-trained model & encoders.

---

