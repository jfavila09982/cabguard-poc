
<div align="center">

<img src="assets/cabguard-logo.png" alt="CabGuard Logo" width="260" />

# CabGuard POC

### AI-Assisted In-Vehicle Safety Monitoring

**Exploring Computer Vision and Human Behavioral Analysis**

![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?logo=opencv&logoColor=white)
![YOLO11](https://img.shields.io/badge/YOLO11-Pose%20Estimation-00AABB)
![Status](https://img.shields.io/badge/Status-Early%20POC-orange)

</div>

---

## Overview

**CabGuard** is a personal computer vision proof-of-concept exploring AI-assisted safety monitoring inside vehicles.

The project aims to investigate how human movement and behavioral patterns can be analyzed to help identify potentially threatening or distress-related situations involving drivers and passengers.

Currently, CabGuard focuses on **real-time human pose estimation**, using Ultralytics YOLO11 Pose and OpenCV to detect and visualize body keypoints from a live webcam feed.

This initial implementation establishes the foundation for future behavioral analysis, movement pattern recognition, and potential threat detection.

> **Development Status:** Early-stage proof of concept. Human pose detection is implemented; behavioral classification and threat recognition remain future development goals.

---

## Project Objectives

CabGuard explores the potential of computer vision for improving in-vehicle safety through:

- Real-time human pose estimation.
- Observation of body movement and skeletal positioning.
- Exploration of temporal behavioral patterns.
- Research into potentially aggressive or distress-related movements.
- Development of a foundation for AI-assisted safety monitoring.

The long-term objective is to investigate whether movement patterns can contribute to identifying potentially unsafe situations inside vehicles.

---

## Current Features

The current proof of concept supports:

- **Real-Time Video Capture** — Captures video frames through the default webcam.
- **Human Pose Detection** — Uses YOLO11 Pose to estimate body keypoints.
- **Skeleton Visualization** — Displays body landmarks and skeletal connections.
- **Person Detection** — Draws bounding boxes around detected people.
- **Live Video Preview** — Displays annotated video frames using OpenCV.
- **Keyboard Control** — Press `q` to exit the application.

---

## How It Works

The current implementation follows a basic computer vision pipeline:

```text
       Webcam Input
            |
            v
     Frame Capture
         OpenCV
            |
            v
     YOLO11 Pose Model
            |
            v
   Human Pose Estimation
            |
            v
   Keypoint & Skeleton
      Visualization
            |
            v
     Live Video Output
```

Each captured frame is processed by the pretrained YOLO11 Pose model.

The model estimates human body landmarks, allowing the application to visualize skeletal positioning and movement in real time.

At this stage, the system does not interpret these movements as specific behaviors or threats.

---

## Technology Stack

| Technology | Purpose |
|------------|---------|
| Python | Core application development |
| OpenCV | Video capture and frame visualization |
| Ultralytics YOLO11 Pose | Human pose and keypoint estimation |
| Pretrained YOLO11n Pose Weights | Pose estimation model |

---

## Getting Started

### Prerequisites

Before running CabGuard, make sure you have:

- Python 3.12 (recommended)
- A working webcam
- Git
- pip

### 1. Clone the Repository

```bash
git clone https://github.com/jfavila09982/cabguard-poc.git
cd cabguard-poc
```

### 2. Create a Virtual Environment

**Windows PowerShell**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**macOS / Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Run CabGuard

Connect your webcam and execute:

```bash
python main.py
```

The application will open a live video preview displaying detected human poses and skeletal landmarks.

Press `q` to terminate the application.

---

## Model Information

CabGuard currently uses:

**YOLO11n Pose (`yolo11n-pose.pt`)**

The pretrained model estimates human body keypoints from image frames.

The model weights are included in this repository.

The current implementation uses pretrained inference without custom behavioral classification training.

---

## Development Status

### Phase 1 — Human Pose Estimation

**Current Implementation**

- [x] Webcam video capture
- [x] YOLO11 Pose model integration
- [x] Human keypoint detection
- [x] Skeleton and bounding box visualization
- [x] Real-time annotated video output

### Phase 2 — Behavioral Analysis

**Planned / Research Stage**

- [ ] Temporal keypoint tracking
- [ ] Movement pattern analysis across frames
- [ ] Body posture and gesture interpretation
- [ ] Behavioral feature extraction
- [ ] Preliminary action classification experiments

### Phase 3 — Potential Threat Recognition

**Future Exploration**

- [ ] Identification of potentially aggressive movements
- [ ] Distress-related behavioral pattern research
- [ ] Context-aware movement classification
- [ ] Reduction of false-positive detections
- [ ] Evaluation using representative behavioral datasets

### Phase 4 — Safety Monitoring

**Long-Term Goals**

- [ ] Event-based monitoring
- [ ] Potential incident recording
- [ ] Configurable safety alerts
- [ ] In-vehicle camera integration
- [ ] Performance and reliability evaluation

---

## Current Limitations

CabGuard remains an experimental proof of concept.

The current implementation:

- Does not classify human behavior.
- Does not detect or confirm physical assault.
- Does not recognize distress or emergency situations.
- Does not generate automated safety alerts.
- Does not record or persist detection events.
- Has not been validated as a production-ready vehicle safety system.

Human pose estimation alone cannot reliably determine a person's intentions or confirm threatening behavior.

Further research, temporal analysis, representative datasets, and extensive validation would be necessary before introducing behavioral classification capabilities.

---

## Future Direction

CabGuard aims to explore the relationship between human movement patterns and in-vehicle safety.

Future development will focus on transforming individual pose estimations into meaningful temporal movement features that can support experiments in behavioral analysis.

The goal is to research how computer vision may contribute to identifying potentially unsafe situations while considering reliability, privacy, and limitations in interpreting human behavior.

---

## Project Information

**Project:** CabGuard POC

**Category:** Artificial Intelligence / Computer Vision

**Development Type:** Personal Research & Development Project

**Current Focus:** Human Pose Estimation

**Next Phase:** Behavioral Analysis

**Status:** Early-stage Proof of Concept

---

## Author

**Jun Marco C. Favila**

Software Developer exploring backend engineering, artificial intelligence, and computer vision.

GitHub: [@jfavila09982](https://github.com/jfavila09982)

---

<div align="center">

**CabGuard — Exploring Intelligent In-Vehicle Safety Through Computer Vision**

*Personal project • Research & Development • Proof of Concept*

</div>
