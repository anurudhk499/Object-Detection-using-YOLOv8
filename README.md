#  Real-Time Object Detection using YOLOv8
## 📌 Overview

This project demonstrates real-time object detection using the powerful **YOLOv8 (You Only Look Once)** model from Ultralytics. It supports both **image-based detection** and **live webcam detection** using OpenCV.
The system detects multiple objects in real-time and displays bounding boxes with labels.


## Technologies Used

* Python 🐍
* OpenCV 📷
* YOLOv8 (Ultralytics)
* Deep Learning / Computer Vision



## Features

✔️ Object detection on images<br>
✔️ Real-time detection using webcam<br>
✔️ Pre-trained YOLOv8 model (no training required)<br>
✔️ Fast and efficient detection<br>
✔️ Easy to run and modify<br>



## ▶️ How It Works

### 1. Load YOLOv8 Model

The model is automatically downloaded:

```python
from ultralytics import YOLO
model = YOLO("yolov8n.pt")
```

### 2. Image Detection

```python
img = cv2.imread("image.jpg")
results = model(img)
```

### 3. Real-Time Webcam Detection

```python
cap = cv2.VideoCapture(0)

while True:
    ret, frame = cap.read()
    results = model(frame)
    output = results[0].plot()

    cv2.imshow("Detection", output)

    if cv2.waitKey(1) == ord('q'):
        break
```

---

## 🖥️ Installation

### Step 1: Clone Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### Step 2: Install Dependencies

```bash
pip install ultralytics opencv-python
```

---

## ▶️ Run the Project

```bash
python your_script.py
```

OR open the notebook:

```bash
jupyter notebook YOLO.ipynb
```

---

## 📸 Output

* Detects objects like **person, car, bottle, etc.**
* Displays bounding boxes with labels
* Works in real-time via webcam


