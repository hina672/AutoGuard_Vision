# Real-Time-Object-Detection-And-Counter


This project uses the YOLOv8 object detection model to detect specific objects (like people, cars, buses, etc.) within 6 feet (approx. 1828.8 mm) in real-time video or video streams. If an object is within this distance, a snapshot is saved with the timestamp and object counts.

---

## 🔧 Features

- 📸 Detects objects using [YOLOv8](https://github.com/ultralytics/ultralytics)
- 🎯 Calculates real-world distance from the camera using known object width
- ✅ Only saves snapshots if object is **within 6 feet**
- 🧠 Avoids redundant saves using **image hashing** and **cooldown timers**
- ⏰ Adds timestamps and detected object summaries to saved images
- 📹 Works with **webcams** and **video URLs**
- 📁 Saves detected images with bounding boxes, distance, and summary overlays

---

## 💡 Use Cases

- Social distancing monitoring  
- Security & surveillance systems  
- Distance-based object tracking  
- Smart retail analytics  

---

## 🛠️ Tech Stack

**Languages:**  
Python

**Computer Vision & AI:**  
- YOLOv8 (`ultralytics`)
- OpenCV
- EasyOCR  
- ImageHash  
- PIL (Pillow)

**Utilities:**  
- NumPy  
- Time, Datetime  
- os, defaultdict (collections)

---



**Required Packages:**

* ultralytics
* opencv-python
* imagehash
* pillow
* numpy

You can install them via:

```bash
pip install ultralytics opencv-python imagehash pillow numpy
```

---

## ▶️ How It Works

1. Loads YOLOv8 pretrained model (`yolov8n.pt`)
2. Uses known object width and bounding box width to estimate distance
3. If an object is within 6 feet:

   * Adds bounding boxes + distance labels
   * Saves snapshots with time + object count
   * Skips saving if same object was recently saved
4. Displays live video with timestamp + summary overlays

---

## 📽️ Example Video Source

This sample uses a demo video URL:

```python
video_url = "http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ForBiggerEscapes.mp4"
```

To use your webcam instead, comment out the video line and uncomment:

```python
cap = cv2.VideoCapture(0)  # Webcam
```



## 📷 Sample Snapshot

![example](./v1%20saved_images/sample_snapshot.jpg)

🔐 Note: This is a public demo overview. Preview images are intentionally excluded from this public demo to respect privacy and data sensitivity. The full source code is available upon request. Contact me via LinkedIn https://www.linkedin.com/in/hinaasad-/ or email at hinaasad672@gmail.com.


