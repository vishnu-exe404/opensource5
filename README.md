# opensource5# 🎨 Air Canvas

A high-precision, real-time Computer Vision virtual canvas that lets you draw in mid-air using hand gestures via your webcam. Powered by **MediaPipe Tasks API**, **OpenCV**, and local multimodal AI via **Ollama (LLaVA)** to analyze and solve drawn math problems or describe sketches.

---

## ✨ Features

- **Gesture-Driven Controls**:
  - 🤏 **Pinch (Thumb + Index)**: Draw or erase smooth lines in real-time.
  - ✌️ **Two Fingers Up (Index + Middle)**: Select brush color or eraser from the top navigation bar.
  - ✊ **Closed Fist (Hold 1.2s)**: Clear the entire canvas.
  - 🖐️ **Open Palm (Hold 1.2s)**: Trigger local multimodal vision analysis on your drawing.
- **High Accuracy & Smoothness**:
  - **Exponential Moving Average (EMA) Smoothing**: Eliminates hand jitter and produces clean strokes.
  - **Scale-Invariant Gesture Recognition**: Adapts pinch and gesture detection relative to hand distance from the camera.
  - **Hysteresis Filtering**: Prevents accidental gesture triggers or mode switching.
- **Multimodal AI Vision Integration**:
  - Automatically crops and prepares drawn sketches for evaluation using local Ollama vision models (e.g., `llava`).
  - Solves mathematical equations step-by-step or provides detailed descriptions of drawn objects.
- **Auto-Config & Standalone Execution**:
  - Automatically downloads required MediaPipe task models on first launch.
  - Automatically creates and manages runtime configurations and saved canvas directories.

---

## 🛠️ Prerequisites

Ensure you have Python 3.8+ installed on your system.

### Required Python Packages
```bash
pip install opencv-python mediapipe numpy requests
