# CabGuard POC

A proof of concept for real-time human pose and keypoint detection using a webcam, Ultralytics YOLO11 Pose, and OpenCV.

## Features

- Captures video from the default webcam.
- Detects human pose keypoints in real time.
- Draws bounding boxes, keypoints, and skeleton connections.
- Exits when `q` is pressed.

## Setup

Python 3.12 is recommended.

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

## Run

Connect a webcam, then run:

```powershell
python main.py
```

The repository includes `yolo11n-pose.pt`, the pretrained model weights used by the proof of concept.

## Current scope

This version visualizes pose keypoints only. It does not yet classify threats, recognize distress or assault, send alerts, or save detection events.
