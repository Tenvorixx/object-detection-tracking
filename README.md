# 🚀 Object Detection & Tracking System

A real-time **Object Detection and Multi-Object Tracking** application built with **YOLOv8, SORT Tracker, OpenCV, and Streamlit**.

The application can detect objects in images and videos, assign unique tracking IDs, and track detected objects across video frames through an interactive Streamlit interface.

---

## 📌 Project Overview

This project combines **YOLOv8** for accurate object detection with the **SORT (Simple Online and Realtime Tracking)** algorithm for object tracking.

The system provides an easy-to-use web interface where users can:

* Upload a video for object detection and tracking
* Upload an image for object detection
* Use a local webcam for real-time detection and tracking
* Configure detection confidence and IoU thresholds
* Configure SORT tracking parameters

---

## ✨ Key Features

* 🎯 **YOLOv8 Object Detection**
* 🔄 **Multi-Object Tracking using SORT**
* 🆔 Unique tracking IDs for detected objects
* 🎥 Video-based object detection and tracking
* 🖼️ Image-based object detection
* 📷 Local webcam support
* ⚙️ Adjustable detection and tracking parameters
* 🖥️ Interactive Streamlit interface
* 🚀 OpenCV-based video processing

---

## 🛠️ Tech Stack

| Technology    | Purpose                                   |
| ------------- | ----------------------------------------- |
| **Python**    | Core programming language                 |
| **YOLOv8**    | Object detection                          |
| **SORT**      | Multi-object tracking                     |
| **OpenCV**    | Image and video processing                |
| **Streamlit** | Interactive web interface                 |
| **NumPy**     | Numerical and array operations            |
| **FilterPy**  | Kalman filter implementation used by SORT |

---

## 📂 Project Structure

```text
Object-Detection-Tracking/
│
├── objectDetection.py    # Main Streamlit application
├── sort.py               # SORT tracking implementation
├── yolov8n.pt            # YOLOv8n pretrained model
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation
```

---

## 🔍 How It Works

The system follows this pipeline:

```text
Input
  │
  ├── Image
  ├── Video
  └── Webcam
       │
       ▼
   YOLOv8 Detection
       │
       ▼
Detected Bounding Boxes
       │
       ▼
    SORT Tracker
       │
       ▼
Tracking IDs
       │
       ▼
Streamlit Visualization
```

### Detection & Tracking Process

1. The **YOLOv8n** model detects objects in each frame.
2. Bounding boxes and confidence scores are obtained from the detection results.
3. The detected objects are passed to the **SORT tracker**.
4. SORT uses tracking information to maintain object identities between frames.
5. Each tracked object receives a unique ID.
6. The processed results are displayed through the Streamlit interface.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Replace `YOUR-USERNAME` and `YOUR-REPOSITORY` with your GitHub username and repository name.

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Application

```bash
streamlit run objectDetection.py
```

The Streamlit application will open in your browser.

---

## 🎥 Input Modes

### Upload Video

Upload a video file to perform object detection and tracking frame-by-frame.

### Upload Image

Upload an image to detect objects using YOLOv8.

### Webcam

Use your computer's local webcam for real-time object detection and tracking.

> **Note:** Webcam mode is intended for local deployment because it requires access to the computer's webcam.

---

## ⚙️ Configuration

The application provides controls for important detection and tracking parameters, including:

* **Confidence Threshold** — Controls the minimum confidence required for detections.
* **IoU Threshold** — Controls the overlap threshold used during detection/tracking.
* **Maximum Age** — Controls how long the SORT tracker keeps an object without a matching detection.
* **Minimum Hits** — Controls the number of successful detections required by the tracker.

These settings allow users to experiment with detection accuracy and tracking behavior.

---

## 🤖 Model

The project uses the **YOLOv8n** pretrained model:

```text
yolov8n.pt
```

The model is loaded directly by the application and used for object detection.

---

## 💡 Skills Demonstrated

This project demonstrates practical experience with:

* Computer Vision
* Object Detection
* Multi-Object Tracking
* YOLOv8
* SORT Tracking
* OpenCV
* Python
* Streamlit
* Real-time video processing
* Machine Learning model integration

---

## 👨‍💻 Author

**Pravesh Verma**

Computer Science & Engineering Student

---

## ⭐ Acknowledgement

This project uses **YOLOv8** for object detection and the **SORT (Simple Online and Realtime Tracking)** approach for object tracking.

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---
