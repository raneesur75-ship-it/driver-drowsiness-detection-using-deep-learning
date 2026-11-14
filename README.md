# Driver Drowsiness Detection System

A real-time driver-monitoring prototype combining a MobileNetV2-based deep-learning model with facial-landmark measurements to identify visual indicators of driver fatigue and trigger alerts.

<p align="center">
  <img src="driver-drowsiness-detection-demo.gif" alt="Animated demonstration of the driver drowsiness detection system" width="760">
</p>

<p align="center"><strong>Reported test accuracy: 96.68%</strong> · 4 visual classes · Real-time webcam prototype</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/TensorFlow-Keras-FF6F00?logo=tensorflow&logoColor=white" alt="TensorFlow">
  <img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?logo=opencv&logoColor=white" alt="OpenCV">
  <img src="https://img.shields.io/badge/Model-MobileNetV2-2E8B57" alt="MobileNetV2">
</p>

## Overview

Driver fatigue can reduce attention and reaction time. This project explores a computer-vision approach for detecting visual indicators of drowsiness through a webcam. The prototype combines image classification and facial-landmark measurements, then presents a live status and alert.

**Academic project result:** 175/200 (87.5%).

## Features

- **Webcam-based monitoring** with a live visual interface.
- **CNN image classification** using a MobileNetV2-based model.
- **Four visual classes:** `Closed_Eyes`, `Open_Eyes`, `No_Yawn`, and `Yawn`.
- **Facial-landmark measurements:** Eye Aspect Ratio (EAR) and Mouth Aspect Ratio (MAR).
- **Combined decision logic** to estimate fatigue indicators.
- **Visual and audio alerts** when configured detection conditions are met.
- **Evaluation scripts** and a data-augmentation workflow.

## Demo and screenshots

The animation above shows the application in operation. Additional screenshots are available in the [screenshots](screenshots/) directory.

## Model evaluation

The repository reports **96.68% overall accuracy** on a held-out test set of 572 images. The class-level figures recorded for that evaluation are:

| Class | Reported accuracy | Correct predictions |
|---|---:|---:|
| Closed_Eyes | 100.00% | 143/143 |
| Open_Eyes | 98.60% | 141/143 |
| No_Yawn | 93.01% | 133/143 |
| Yawn | 95.10% | 136/143 |
| **Overall** | **96.68%** | **553/572** |

These are the project's reported evaluation results, not a guarantee of performance in real driving conditions. Lighting, camera position, individual differences, and environmental conditions can affect predictions.

## Technology

- Python
- TensorFlow / Keras
- MobileNetV2
- OpenCV
- MediaPipe
- NumPy and scikit-learn
- PyTorch and Hugging Face Diffusers for the documented augmentation workflow

See [requirements.txt](requirements.txt) for the current dependency list.

## Repository structure

```text
.
├── data/             # Dataset notes and sample-data information
├── docs/             # Project documentation and thesis (when added)
├── models/           # Model files, if included
├── notebooks/        # Experiment notebooks, if included
├── results/          # Evaluation outputs, if included
├── screenshots/      # Application screenshots
├── src/
│   ├── data_augmentation.py
│   ├── evaluate.py
│   ├── realtime_detector.py
│   └── train.py
├── requirements.txt
└── README.md
```

## Getting started

### 1. Clone the repository

```bash
git clone https://github.com/raneesur75-ship-it/driver-drowsiness-detection-using-deep-learning.git
cd driver-drowsiness-detection-using-deep-learning
```

### 2. Create and activate a virtual environment

**Windows (PowerShell):**

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS / Linux:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Some deep-learning and computer-vision packages have Python-version and operating-system compatibility requirements. If installation fails, use a Python version supported by the packages in your environment and consult their official installation guides.

### 4. Run the webcam application

```bash
python src/realtime_detector.py
```

A working webcam and the model/assets expected by the application are required. Check the source code and available model files before running if your local setup differs from the original development environment.

## Dataset

The complete dataset is not stored in this repository. Dataset sources, class information, and sample-data notes are described in [data/README.md](data/README.md). Respect the licences and usage conditions of the original datasets and third-party material.

## Limitations and responsible use

This repository is an academic prototype. It is **not a certified vehicle-safety system** and must not be used as the sole means of deciding whether a person is fit to drive. Do not interact with the application while driving. Real-world deployment would require broader testing, validation across diverse conditions, privacy review, and safety engineering.

## Academic documentation

The final approved thesis PDF will be added to the `docs/` directory after it has been checked for correctness and permission to publish. No thesis file is included yet.

## Author

**Anees Ur Rehman**

Computer Science graduate interested in applied AI, deep learning, and computer vision.

---

If you find this project useful, you can star the repository or open an issue with a question or suggestion.
