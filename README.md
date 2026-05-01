# real-time-object-detection-tracking
real-time-object-detection-tracking A real-time object detection and tracking system I built using YOLOv8 and OpenCV. It runs on live webcam feed or video files and draws bounding boxes around detected objects with unique tracking IDs.

Why I built this I wanted to get hands-on with computer vision and understand how detection and tracking actually work together in real time. This project helped me go from zero to a working system that can detect and follow multiple objects simultaneously.

Demo

Run it yourself and see — webcam fires up instantly and starts tracking. 
 
What it does Detects objects in real time using YOLOv8 Assigns a unique tracking ID to each object across frames Draws bounding boxes with class labels and confidence scores Works on webcam feed or any video file

Tech used Python 3.12 YOLOv8 (Ultralytics) PyTorch OpenCV

How to run it

Clone the repo
git clone https://github.com/sidharth-1005/real-time-object-detection-tracking.git
cd real-time-object-detection-tracking
Install dependencies
pip install -r requirements.txt
Run on webcam
python yolo/v8/detect/detect_and_trk.py model=yolov8s.pt source=0 show=True
Run on a video file
python yolo/v8/detect/detect_and_trk.py model=yolov8s.pt source="your_video.mp4" show=True
Press Q to quit the window.

Setup notes Tested on Python 3.12.4 and PyTorch 2.2.0 (CPU) yolov8s.pt weights download automatically on first run (~22MB) If you hit a pkg_resources error, run: pip install setuptools==69.5.1

Project structure

real-time-object-detection-tracking/
├── yolo/
│   └── v8/
│       └── detect/
│           └── detect_and_trk.py   ← main script
├── assets/
│   └── demo.gif                    ← demo recording
├── requirements.txt
└── README.md
What I learned How YOLOv8 handles detection under the hood How SORT tracking assigns and maintains object IDs across frames Debugging Python version and dependency conflicts (the fun part 😅) How to wire OpenCV video I/O with a live detection pipeline

Possible improvements [ ] Switch to ByteTrack for better tracking accuracy [ ] Add object counting per class [ ] GPU support for higher FPS [ ] Export tracked output as video file

Real-time multi-object detection and tracking powered by YOLOv8 and OpenCV. 
 
📸 Demo 
  Detecting and tracking multiple objects live — each assigned a unique track ID with a bounding box and confidence score.

🚀 Features ⚡ Real-time detection — runs at high FPS on CPU and GPU 🔁 Multi-object tracking — persistent track IDs across frames using ByteTrack 🟩 Bounding boxes — labeled with class name and confidence score 🎬 Video demo — test on any .mp4 or webcam feed out of the box

🛠️ Tech Stack Tool Purpose Python 3.10+ Core language PyTorch Deep learning backend YOLOv8 (Ultralytics) Object detection model OpenCV Video I/O and rendering

📁 Project Structure

real-time-object-detection-tracking/
├── assets/
│   └── demo.gif              # Demo animation for README
├── videos/
│   └── sample.mp4            # Sample input video
├── weights/
│   └── yolov8n.pt            # YOLOv8 model weights (auto-downloaded)
├── detect_
