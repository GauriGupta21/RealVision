#  RealVision: Smart Object Detection & Notification System

**RealVision** is a powerful desktop-based object detection system built with **YOLOv8**, **Tkinter**, and **OpenCV**, designed to track, log, notify, and count objects in real time from:
- Live camera input
- Uploaded videos
- Uploaded images

It not only detects objects but also:
- **Sends desktop notifications** when specific objects (like person, car, bicycle) appear
- **Logs data** into Excel sheets
- **Counts unique object instances intelligently** (no double-counting)
- **Saves annotated frames**
- Runs entirely offline on your laptop

---

## Features

| Feature                             | Description                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------|
|  YOLOv8 Object Detection          | Real-time detection with bounding boxes and confidence scores              |
|  Smart Desktop Notifications      | Sends alerts for selected objects (e.g., person, bicycle, car)             |
|  Excel Logging                    | Logs every detection with timestamp and unique ID                          |
|  Intelligent Object Tracking      | Detects when object leaves & reappears — no duplicate counting             |
|  Save Frame Button                | Saves the current annotated frame manually                                 |
|  Video & Image Support            | Works with webcam or uploaded MP4 files                                    |
|  GUI Built with Tkinter           | Easy-to-use graphical interface                                            |

---

##  Technologies Used

- Python 3.x
- OpenCV
- Tkinter (GUI)
- YOLOv8n (Ultralytics)
- Pillow (image rendering)
- Plyer (desktop notifications)
- openpyxl (Excel logging)

---

##  Installation Instructions

###  Prerequisites

- Python 3.7+
- pip

---

###  Step-by-Step Setup

```bash
# Step 1: Clone the repository
git clone https://github.com/yourusername/RealVision.git
cd RealVision

# Step 2: Install dependencies
pip install opencv-python ultralytics pillow openpyxl plyer

# Step 3: How to Run
python realvision_app.py
```
The GUI will launch. You can:

Click Start Camera to detect from your webcam

Click Select Video to upload a video

Click Save Frame to save the current frame

Click Stop to close detection

All detected objects are saved in:

detected_objects.xlsx

object_count.xlsx

## How It Works
Loads YOLOv8n model.

Captures frames from camera/video.

Detects objects and labels them with class and confidence.

Sends notification if any object in the alert list (person, car, bicycle) is found.

Logs detections with timestamps and unique IDs.

Updates Excel-based object counts.

Avoids recounting objects unless it fully disappears and reappears (intelligent memory).

##  Output Files

| File Name                  | Purpose                                 |
|---------------------------|------------------------------------------|
| `detected_objects.xlsx`   | Stores timestamp, object type, and ID    |
| `object_count.xlsx`       | Stores total object counts per class     |
| `frame_YYYYMMDD_HHMM.jpg` | Saved frames manually by the user        |

## Advantages Over Basic Detection Scripts

| Feature             | Others                        | RealVision                        |
|---------------------|-------------------------------|------------------------------------|
|  Notification Alerts |  No                         |  Yes                             |
|  Excel Logging      |  Manual                     |  Automatic                       |
|  Object Memory       | Duplicates on re-entry     |  Tracks & avoids duplicates      |
|  GUI Interface       |  None (only terminal)        |  Tkinter-based live GUI          |
|  Frame Saving       |  Manual only                |  Button-based frame saving       |

## License
This project is licensed under the MIT License.





