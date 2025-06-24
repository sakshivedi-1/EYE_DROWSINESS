#  EYE_DROWSINESS_DETECTION

Real-time driver drowsiness detection using facial landmarks and Eye Aspect Ratio (EAR). Powered by OpenCV, dlib, and Python.

This project tracks a user's eyes via webcam feed and triggers an alert if drowsiness is detected—enhancing safety in real-time applications like automotive systems.

---

##  How It Works

1. Captures video using OpenCV
2. Detects facial landmarks using `dlib`
3. Computes the Eye Aspect Ratio (EAR)
4. Triggers alert if eyes stay closed beyond a threshold

---

##  Tech Stack

- **Python**
- **OpenCV**
- **dlib** (facial landmark detection)
- **scipy** / **imutils**
- **pygame** (for playing alert sounds)

---

##  Run It Locally

### 1. Clone the Repository

```bash
git clone https://github.com/sakshivedi-1/EYE_DROWSINESS.git
cd EYE_DROWSINESS
2. Install Requirements
bash
Copy
Edit
pip install -r requirements.txt
⚠ Note: Installing dlib may require CMake or pre-built binaries depending on your OS.

3. Run the App
bash
Copy
Edit
python drowsiness_detection.py
Make sure your webcam is connected and accessible.

 Directory Structure
bash
Copy
Edit
EYE_DROWSINESS/
│
├── drowsiness_detection.py   # Main detection script
├── shape_predictor_68_face_landmarks.dat  # Pre-trained dlib model
├── alarm.wav                 # Alert sound file
├── requirements.txt
└── README.md
Key Features
Real-time facial landmark detection

EAR-based drowsiness metric

Custom audio alert when user is sleepy

Works with any standard webcam

🔧 Troubleshooting
dlib installation error?

Install CMake first: pip install cmake

Use precompiled wheels from: https://www.lfd.uci.edu/~gohlke/pythonlibs/#dlib

No sound on alert?

Check if alarm.wav is in the root directory

Ensure pygame is installed and functional

