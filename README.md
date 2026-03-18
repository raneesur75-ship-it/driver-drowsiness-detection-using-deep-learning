🚗 Driver Drowsiness Detection System

Python | TensorFlow | OpenCV | MediaPipe

🚨 A real-time AI system that detects driver fatigue using Computer Vision and Deep Learning
⚡ 96.5% Accuracy | 👁️ Eye + Mouth Analysis | 🔊 Smart Alarm System

📸 Demo

👉 (Add screenshots / GIF here — THIS IS CRITICAL)

Live detection interface

Fatigue score + graphs

Alarm triggering

🎯 Why This Project Matters

Drowsy driving is a major cause of road accidents worldwide.
This system helps prevent accidents by:

Detecting early signs of fatigue

Alerting drivers in real-time

Providing a low-cost, deployable safety solution

🔥 Key Features

🎥 Real-time Detection
Webcam-based monitoring using MediaPipe Face Mesh (468 landmarks)

🧠 Hybrid Intelligence System
Combines:

Eye Aspect Ratio (EAR)

Mouth Aspect Ratio (MAR)

CNN (MobileNetV2)

🤖 Deep Learning Model

MobileNetV2 (Transfer Learning)

96.5% test accuracy

🎨 Smart Data Augmentation

Stable Diffusion (AI-generated images)

Improved dataset diversity

📊 Professional UI

Live fatigue score (0–100%)

Real-time graphs (EAR/MAR trends)

Status indicators (AWAKE / WARNING / ALARM)

🔔 Multi-Trigger Alarm System

Eye closure

Yawning

Head nodding

📊 Performance Metrics
Class	Accuracy	Notes
Closed_Eyes	~99%	Very strong detection
Open_Eyes	~99%	Highly reliable
No_Yawn	~95%	Minor confusion cases
Yawn	95.8%	High recall (safety-critical)

👉 Overall Accuracy: 96.50% (572 test images)

📚 Dataset

Total Images: 2,845

Split: 80% training / 20% testing

Classes: 4 (Balanced dataset)

Sources:

Kaggle datasets

Self-collected images/videos

Stable Diffusion augmentation

📁 Full dataset not included (size), sample available in data/sample/



🏗️ System Architecture

```
Webcam → Face Mesh → EAR/MAR → CNN → Fatigue Score → Alarm
```
💡 Why This Works

Lightweight → runs on laptop

Hybrid approach → reduces false alarms

Real-time processing → practical deployment

The system uses a **hybrid approach** (fast rule-based + deep learning) for reliable real-time drowsiness detection.

### Flow:
1. **Webcam Input** → Live video frames  
2. **MediaPipe Face Mesh** → 468 facial landmarks  
3. **EAR + MAR Calculation** → Quick eye/yawn detection  
4. **MobileNetV2 CNN** → Classifies eyes & mouth (96.5% accurate)  
5. **Decision Fusion** → Combines everything into Fatigue Score  
6. **Alert System** → Alarm + UI graphs if drowsy  

**Why it works**: Lightweight (MobileNetV2 runs on laptop/mobile), very accurate, and almost no false alarms.

(Architecture diagram coming soon — we will add screenshot here next!)

## 💻 Installation & How to Run

### 1. Clone the repo
```
git clone https://github.com/raneesur75-ship-it/driver-drowsiness-detection-using-deep-learning.git
cd driver-drowsiness-detection-using-deep-learning
```
### 2. Install packages

```
pip install -r requirements.txt

```
### 3. Run the real-time demo

```
python src/realtime_detector.py

```


## Note: 
Your🎥 Webcam will start with live detection + fatigue score + alarm system will open instantly.


🚀 Key Innovations

✅ Hybrid CNN + EAR + MAR system

✅ AI-based data augmentation using Stable Diffusion

✅ Real-time fatigue scoring (not just classification)

✅ Multi-condition alarm logic

🔮 Future Improvements

Night vision (infrared camera)

Mobile app (Android/iOS)

Cloud-based monitoring system

Voice-based alerts
