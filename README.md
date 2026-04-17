# ROO'YA (رؤية) - Smart Visual Assistance System 👁️

**ROO'YA** is an AI-powered assistive technology designed to help visually impaired individuals navigate urban environments safely. The system identifies obstacles in real-time and provides immediate directional audio feedback.

---

## 🎥 System Demonstration & Explanation

Below is a demonstration of the system processing a complex urban environment at night.

![Project Demo](رابط_الفيديو_هنا)

### 🔍 What’s happening in this video?
1. **Dynamic Environment Handling:** The system successfully identifies multiple "Persons" and "Cars" even under low-light conditions (Night-time).
2. **Directional Awareness:** The model doesn't just detect objects; it analyzes their position to provide accurate spatial alerts (e.g., "Person on your Left").
3. **Obstacle Prioritization:** The system is fine-tuned to focus on immediate paths, ensuring the user is warned about the most relevant obstacles first.

---

## ⚠️ IMPORTANT: Local Deployment
> [!IMPORTANT]
> **Privacy & Speed:** This system runs **ENTIRELY LOCAL**. It does not require an internet connection to process the camera feed or generate voice alerts. This ensures:
> - **Zero Latency:** Immediate response essential for safety.
> - **Privacy:** No data or video feed is ever uploaded to the cloud.

---

## 🚀 Key Features

* **Real-time Object Detection:** Powered by a custom-trained **YOLO** model.
* **Intelligent Audio Feedback:** Features a "Cooldown Mechanism" to prevent overlapping voice alerts (no more "Per-Per-Person" stuttering).
* **High Sensitivity:** Adjusted confidence thresholds (`conf=0.3`) to detect smaller objects like street poles and barriers.
* **Multi-Class Support:** Specifically trained to recognize Pedestrians, Vehicles, and common Urban Obstacles.

---

## 🛠️ Technical Overview

### Model Training
* **Dataset:** 1,754 curated images of diverse street scenes.
* **Performance:** High precision verified via `Confusion Matrix` and `F1-Score` curves (available in the `results/` folder).

### Tech Stack
* **Language:** Python 3.x
* **AI Engine:** Ultralytics YOLO
* **Audio:** pyttsx3 (Offline Text-to-Speech)
* **Backend:** Flask (for local stream handling)

---

## ⚙️ Installation (Local Run)

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/Rooya_Project.git](https://github.com/yourusername/Rooya_Project.git)
