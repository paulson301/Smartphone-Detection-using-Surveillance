# Smartphone Detection using Surveillance

This project is a browser-based surveillance demo that detects a mobile phone in a person's view and raises an alert when it appears that the phone is being used in a risky or prohibited way.

## Overview

The system uses a combination of:
- TensorFlow.js
- COCO-SSD for object detection
- PoseNet for pose estimation

It monitors:
- whether a cell phone is visible in the frame
- whether the phone is near the user's face or within their visual zone
- whether the phone is near the ear while a hand is close, suggesting a call
- whether the phone was recently seen and should remain in memory for a short period before clearing

A live webcam feed is displayed, along with a status HUD and a flashing alarm when a violation is detected.

## Features

- Real-time webcam access
- Detection of `cell phone` objects
- Face and hand landmark tracking
- Visual vision-zone overlay around the face
- Memory-based logic to reduce false alarms and flicker
- Audio alarm for suspicious activity
- Minimal browser-based control panel

## Project Structure

- `final_guard.html` — main HTML, CSS, and JavaScript file containing the surveillance logic

## How to Run

1. Clone or download the project.
2. Open the project folder in a browser, or serve it locally with a web server.
3. Allow camera permissions when prompted.
4. Click the `ACTIVATE` button to begin monitoring.

### Local Server Example

```bash
cd Smartphone-Detection-using-Surveillance
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/final_guard.html
```

## Technologies Used

- HTML5
- CSS3
- JavaScript
- TensorFlow.js
- COCO-SSD
- PoseNet

## Notes

- This is a prototype/demonstration project.
- It requires webcam access and a modern browser.
- The detection logic is intended for educational and experimental use, not for production-grade security or surveillance deployment.

## License

This project is provided as-is for educational and experimental use.
