# Real-Time Object Tracker

Overview
This project implements a **real-time object tracker** using **OpenCV** in Python. The system allows a user to select an object in the first frame from a live webcam feed and then tracks the selected object as it moves, displaying the tracking results in a live video feed.

---

## Implementation Details

### 1 **Key Features:**
- **Live webcam feed capture** using `cv2.VideoCapture()`.
- **User-defined object selection** via `cv2.selectROI()` for the initial bounding box.
- **Real-time object tracking** using OpenCV's `cv2.TrackerCSRT_create()` tracker.
- **Dynamic bounding box visualization** updated in real-time with tracking status.
- **Smooth live video display** using `cv2.imshow()` with minimal latency.

### 2 **Technologies Used:**
- **Python 3.x**
- **OpenCV (cv2)**

### 3 **Tracking Algorithm:**
- The **CSRT (Discriminative Correlation Filter with Channel and Spatial Reliability)** tracker is used due to its balance between speed and accuracy, making it ideal for real-time applications.

### 4 **How It Works:**
1. The webcam feed is initialized, capturing live video frames.
2. The user selects the object to be tracked by drawing a bounding box on the first frame.
3. The CSRT tracker is initialized with the selected region.
4. For every new frame from the webcam, the tracker updates the bounding box position based on the object's movement.
5. The tracking results are displayed in real-time, with the bounding box following the object as it moves.

### 5 **Exiting the Application:**
- The live tracking window can be closed by pressing the **`q`** key.

---

##  Prerequisites
- Python 3.x
- OpenCV (`opencv-python`)

###  **Install Dependencies:**
```bash
pip install opencv-python
```

---

##  Running the Tracker

###  **Run the Script:**
```bash
python real_time_tracker.py
```

### **Usage Steps:**
1. When the webcam feed opens, **select the object** you want to track by drawing a bounding box with the mouse.
2. The tracking will start automatically and display the results in **real time**.
3. To **stop the tracking**, press **`q`**.

---

##  Key Points
- The **tracking quality** depends on lighting conditions and object movement speed.
- **CSRT tracker** provides higher accuracy but might be slower on low-end devices. For faster but less accurate tracking, try **KCF** or **MOSSE**.

---




