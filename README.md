# ESP32-CAM VR Stream

This project enables a real-time object detection system using an ESP32-CAM, a Raspberry Pi for processing via MediaPipe, and VR headset visualization via a WebXR interface.

## 🌐 Overview

1. **ESP32-CAM** streams MJPEG over HTTP.
2. **Raspberry Pi** receives the stream, analyzes it using [MediaPipe](https://google.github.io/mediapipe/), and optionally overlays detection results.
3. **VR Headset** accesses a local WebXR page to view the processed stream in immersive mode.

## 📁 Project Structure

esp32-cam-vr-stream/
├── esp32/ # ESP32 camera streaming firmware
├── raspberry/ # MediaPipe-based analysis (Python)
├── vr-interface/ # VR WebXR viewer (HTML/JS)
├── docs/ # Diagrams and technical drawings
├── README.md
└── LICENSE

shell
Kopieren
Bearbeiten

## 🚀 Getting Started

### 1. Flash the ESP32-CAM
- Upload `esp32/camera_webserver.ino` using Arduino IDE
- Configure Wi-Fi SSID and password

### 2. Run analysis on Raspberry Pi
```bash
cd raspberry
pip install -r requirements.txt
python main.py
3. Open the VR interface
Use a VR-ready browser (e.g. Oculus Browser)

Visit the local IP of your Raspberry Pi hosting vr-interface/public/index.html

🧰 Requirements
ESP32-CAM (e.g., AI Thinker)

Raspberry Pi 4 or newer

Python 3.7+

MediaPipe, OpenCV

Local Wi-Fi network

WebXR-compatible VR headset (e.g., Meta Quest)

📖 License
MIT License – feel free to use, modify, and share.