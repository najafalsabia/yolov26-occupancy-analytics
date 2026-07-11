# AETHER VISION v5.0 – Real-Time People Counting, Occupancy Analytics, and Dwell Time Monitoring

## Overview

AETHER VISION v5.0 is a modular real-time computer vision system designed for people counting and occupancy monitoring. The system detects, tracks, and counts individuals crossing a configurable counting line while providing live occupancy statistics and telemetry output.

The project is built using **YOLO**, **ByteTrack**, **OpenCV**, and **PyTorch**, making it suitable for CCTV-based monitoring applications such as retail stores, offices, shopping malls, and public facilities.

---

## Features

Persistent multi-object tracking.
Entry / Exit counting.
Real-time occupancy monitoring.
Dwell Time calculation.
Average customer time inside.
Employee visualization support.
Automatic stream recovery.
Live telemetry export.
GPU acceleration.
Dynamic JSON configuration.

---

## System Architecture

```
Video Stream
        │
        ▼
YOLO Detection
        │
        ▼
ByteTrack Tracking
        │
        ▼
State Management
        │
        ├── IN
        ├── OUT
        ├── Dwell Time
        └── Occupancy
```

---

## Technologies

* Python
* PyTorch
* Ultralytics YOLO
* ByteTrack
* OpenCV
* NumPy
* Flask
* Flask-CORS
* Pillow

---

## Installation

Clone the repository:

```bash
 execute the installation notebook cell if using Jupyter Notebook.
---

## Running the Project

1. Start the video stream.
2. Load the YOLO model.
3. Run the notebook cells in sequence.
4. Press **Q** inside the OpenCV window to stop the application safely.

---

## Project Workflow

1. Receive video frames.
2. Detect people using YOLO.
3. Assign persistent IDs using ByteTrack.
4. Detect line-crossing events.
5. Update IN and OUT counters.
6. Compute current occupancy.
7. Export telemetry.
8. Display live analytics.

---

## Output Metrics

The application continuously displays:

IN
OUT
Current Occupancy
Average Time Inside
FPS

---

## Configuration

Runtime settings are loaded from `config.json`, allowing dynamic updates without restarting the application.

Available configuration options include:

* Counting line position
* Polygon ROI coordinates
* Detection parameters

---

## Telemetry

Runtime statistics are exported to `telemetry.json`, making the data available for dashboards or external monitoring services.

---

## Hardware Support

* NVIDIA GPU (CUDA)
* CPU fallback mode

The application automatically detects available hardware and selects the optimal execution device.

---



