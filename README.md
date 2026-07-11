# AETHER VISION v5.0
### AI-Powered Real-Time Occupancy Analytics using YOLO and ByteTrack

<p align="center">
  <img src="demo.gif" alt="System Demo" width="900">
</p>

---

## Overview

AETHER VISION v5.0 is a modular real-time computer vision system for people counting and occupancy analytics.

Built with **YOLO**, **ByteTrack**, **OpenCV**, and **PyTorch**, the system detects, tracks, and counts people while providing live occupancy statistics, dwell time analytics, and telemetry.

Before running the model, users can preview the video and accurately configure the counting line or custom polygon zones, making the system easy to adapt to different camera views without modifying the source code.

---

## Features

- Real-time person detection
- Persistent multi-object tracking
- Entry & Exit counting
- Live occupancy monitoring
- Dwell time analytics
- Average time inside
- Employee visualization support
- Pre-run video preview
- Interactive counting line selection
- Custom polygon detection zones
- Automatic stream recovery
- Live telemetry export
- GPU acceleration
- Dynamic JSON configuration

---

## System Architecture

```text
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
      ├── Entry Count
      ├── Exit Count
      ├── Occupancy
      ├── Dwell Time
      └── Telemetry
```

---

## Technologies

- Python
- PyTorch
- Ultralytics YOLO
- ByteTrack
- OpenCV
- Streamlit
- Flask
- Flask-CORS
- NumPy
- Pillow

---

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/yolov26-occupancy-analytics.git

cd yolov26-occupancy-analytics
```

If you're using Jupyter Notebook, simply open the notebook and run the installation cell.

---

## Running the Project

1. Open the notebook.
2. Run the installation cell.
3. Select the input video.
4. Preview the video.
5. Configure the counting line or polygon.
6. Run the detection pipeline.
7. Press **Q** to safely stop the application.

---

## Project Workflow

1. Receive video frames
2. Detect people using YOLO
3. Track people using ByteTrack
4. Detect line-crossing events
5. Update IN and OUT counters
6. Calculate occupancy
7. Compute dwell time
8. Export telemetry
9. Display live analytics

---

## Live Analytics

The application continuously displays:

- IN Count
- OUT Count
- Current Occupancy
- Average Dwell Time
- FPS

---

## Configuration

Runtime settings are loaded from `config.json`, allowing configuration updates without restarting the application.

Available settings include:

- Counting line position
- Polygon ROI coordinates
- Detection parameters

---

## Telemetry

Runtime statistics are exported to `telemetry.json`, allowing integration with dashboards or external monitoring systems.

---

## Hardware Support

- NVIDIA GPU (CUDA)
- CPU fallback mode

The application automatically selects the best available execution device.

---

## Applications

- Retail Stores
- Offices
- Shopping Malls
- Universities
- Smart Buildings
- Public Facilities

---

## License

This project was developed as part of our CO-OP training program for educational and demonstration purposes.
