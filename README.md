# Eye Drowsiness Detection System
## Overview

The Eye Drowsiness Detection System is a real-time computer vision application that monitors a person’s eye state using a webcam feed and detects signs of drowsiness. When prolonged eye closure is detected, the system triggers an alert sound to warn the user. This solution is designed for driver safety and fatigue monitoring use cases.

The project uses OpenCV and facial landmark detection to compute Eye Aspect Ratio (EAR) and determine whether the eyes are open or closed.

## Problem Statement

Driver and operator fatigue is a major safety risk. Manual monitoring is not scalable. There is a need for an automated, low-latency system that can detect drowsiness in real time and generate alerts.

## Objective

Detect eyes from live video feed

Compute eye openness using Eye Aspect Ratio (EAR)

Identify continuous eye closure frames

Trigger an alarm when drowsiness threshold is crossed

## Features

Real-time webcam monitoring

Facial landmark detection

Eye Aspect Ratio (EAR) based logic

Frame-by-frame drowsiness scoring

Audio alert on drowsiness detection

Lightweight and runs on CPU

## Tech Stack

Python

OpenCV

dlib

NumPy

imutils

pygame (for alarm sound)

Project Architecture

Capture live video stream from webcam

Detect face in each frame

Extract facial landmarks

Isolate left and right eye coordinates

Compute Eye Aspect Ratio (EAR)

Compare EAR with threshold

Count consecutive closed-eye frames

Trigger alarm if limit exceeded

Eye Aspect Ratio (EAR)

EAR is computed using distances between eye landmarks.

EAR remains nearly constant when eye is open

EAR drops significantly when eye closes

Threshold + frame counter helps avoid false alarms

## Installation
```
Clone Repository
git clone https://github.com/your-username/eye-drowsiness-detection.git
cd eye-drowsiness-detection
```
```
Install Dependencies
pip install opencv-python dlib imutils numpy pygame scipy

```
Note: dlib may require CMake and a C++ build environment.

### Required Files

shape_predictor_68_face_landmarks.dat (dlib model file)
Download and place it in the project directory.

Run the Project
python drowsiness_detector.py

Press q to exit the window.
## Architecture
Eye_Drowsiness_Detection/
├── data/
│   ├── train/
│   │   ├── open_eyes/
│   │   └── closed_eyes/
│   ├── valid/
│   │   ├── open_eyes/
│   │   └── closed_eyes/
│   ├── test/
│   │   ├── open_eyes/
│   │   └── closed_eyes/
│   ├── data.yaml  # Data configuration for training
├── model/
│   ├── last.pt   # Trained model file
│   └── shape_predictor.dat  # Pre-trained dlib shape predictor
├── src/
│   ├── detection.py 
│   ├── prediction.py  # Real-time detection script for webcam
├── app.py  # Streamlit or Flask web app for deployment
├── requirements.txt  # List of dependencies for the project
└── README.md  # Project documentation
