# 🔥 Early Fire Detection using YOLOv8

A real-time fire and smoke detection system using a custom-trained YOLOv8 model. It processes video feeds and sends email alerts based on three conditions: constant detection, large fire area, and increasing fire size. Ideal for early intervention and disaster prevention.

---

## 📹 Demo

https://user-images.githubusercontent.com/your-video-link.mp4  
> 🔁 Replace this with your actual video URL or embed.

---

## 🧠 Model Details

- **Model**: YOLOv8 (custom-trained)
- **Framework**: Ultralytics
- **Classes**: `fire`, `smoke`
- **Input**: Video file or webcam
- **Device**: CPU (can switch to GPU)

---

## ⚙️ Setup Instructions

1. **Clone this repository**
```bash
git clone https://github.com/yourusername/fire-detection-yolov8.git
cd fire-detection-yolov8
```

2. **Create virtual environment (optional)**
```bash
python -m venv venv
venv\Scripts\activate          # for Windows
# source venv/bin/activate    # for Linux/macOS
```

3. **Install dependencies**
```bash
pip install ultralytics opencv-python
```

---

## 🚀 Run the System

1. **Edit email credentials in `fire_detection.py`:**
```python
sender_email = "your_email@gmail.com"
password = "your_app_password"
receiver_email = "receiver_email@gmail.com"
```

2. **Run the script**
```bash
python fire_detection.py
```

> Press `q` to quit the video window.

---

## 🔔 Alert Conditions

| Condition                     | Trigger Description                                 |
|------------------------------|------------------------------------------------------|
| ✅ Constant Detection         | Fire is detected continuously over time             |
| 🔲 Large Bounding Box         | Fire area exceeds defined size threshold            |
| 📈 Increasing Fire Area       | Fire box area increases continuously                |

Each alert captures the frame and sends an email with the attached image.

---

## 🧪 Test Video

Replace this path in the code with your own:
```python
cap = cv2.VideoCapture(r'E:\Fire_Detection\your_video.mp4')
```

Or switch to webcam:
```python
cap = cv2.VideoCapture(0)
```

---

## 📦 Project Structure

```
fire-detection-yolov8/
├── fire_detection.py           # Main script
├── Model/
│   └── train3/
│       └── weights/
│           └── best.pt        # YOLOv8 trained weights
├── test_videos/
│   └── fire_example.mp4       # Sample video
└── README.md
```

---

## 📽️ Future Work

- SMS/WhatsApp/Push alerts
- RTSP/Streaming support
- Deploy to Raspberry Pi / Jetson
- Log alert history

---

## 📝 License

MIT License

---

## 🙏 Acknowledgements

- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- [OpenCV](https://opencv.org/)

