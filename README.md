
# 🚀 Multi-Model YOLO Object Detection & Performance Benchmark

This project compares multiple YOLO models (**YOLOv8, YOLOv9, YOLOv10, YOLOv11, YOLOv12**) on a real-world traffic surveillance video.  
It runs all models in parallel, generates **side-by-side visual outputs**, and computes **performance statistics** (FPS, people count, car count) to help you choose the best-performing model.

---

## 📌 Features

✅ Loads and runs **multiple YOLO models** on GPU (if available)  
✅ Processes a **video frame-by-frame** and annotates detections  
✅ Displays **people & car counts** for each model  
✅ Measures **FPS (frames per second)** for speed benchmarking  
✅ Generates a **3x2 grid video output** showing all models side by side  
✅ Prints a **performance summary** with average FPS and counts  

---

## 🛠️ Installation & Requirements

Install dependencies if not already installed in your environment:

```bash
pip install ultralytics opencv-python
````

**Tested On:**

* **Python:** 3.10+
* **Ultralytics YOLO:** v8+
* **OpenCV:** 4.11+
* **Torch:** CUDA-enabled GPU recommended for speed

---

## 📂 Project Structure

```
├── notebook.ipynb             # Kaggle Notebook (or .py file)
├── /kaggle/input/lari-adda/   # Input folder containing `adda.mp4`
├── /kaggle/input/yolo11/      # Pretrained YOLOv11 model weights
├── /kaggle/input/yolov12m/    # Pretrained YOLOv12 model weights
└── output2.mp4                # Generated comparison video (saved after processing)
```

---

## ▶️ How to Run

1. Place your input video in `/kaggle/input/lari-adda/adda.mp4`
2. Run the notebook (or Python script)
3. The code will:

   * Load all YOLO models
   * Process each frame through each model
   * Write a 3x2 comparison grid video as `output2.mp4`
   * Print a **performance summary**

---

## 📊 Sample Output (Performance Summary)

After running, you will see a performance report like this:

```
📊 Model Performance Summary:

🔹 YOLOv8n  → Avg FPS: 56.4 | Avg People: 3.8 | Avg Cars: 2.1
🔹 YOLOv9c  → Avg FPS: 49.2 | Avg People: 4.0 | Avg Cars: 2.2
🔹 YOLOv10n → Avg FPS: 61.5 | Avg People: 3.7 | Avg Cars: 2.0
🔹 YOLOv11m → Avg FPS: 44.3 | Avg People: 4.1 | Avg Cars: 2.3
🔹 YOLOv12m → Avg FPS: 42.8 | Avg People: 4.3 | Avg Cars: 2.5
```

* **Avg FPS** → Higher = faster inference
* **Avg People / Cars** → Higher = better detection recall

---

## 📹 Output Video

The final video shows all models’ detections **side-by-side** in a 3x2 grid format, with each frame annotated like this:

```
YOLOv8n | People: 3 Cars: 2 | FPS: 58.2
```

This allows you to **visually inspect** detection quality and compare models.

---

## 🏆 How to Choose the Best Model

* If **speed** matters (real-time processing) → Choose the model with **highest FPS**
* If **accuracy** matters (maximum detections) → Choose the model with **highest people/car counts**
* For **balanced performance** → Choose a model with a good trade-off between FPS & detection count

---

## 📌 Future Improvements

* Add **precision/recall/mAP** evaluation using labeled ground truth data
* Support for **batch inference** for faster processing
* Integrate **model weights auto-download** from Ultralytics Hub
* Deploy as a **web dashboard** to visualize results interactively

---

## 👨‍💻 Author

Developed by **Zuhaib Hussain Butt**
💼 Lecturer in Data Science | Generative AI Enthusiast
📍 Pakistan | 🔗 [LinkedIn]([https://linkedin.com](https://www.linkedin.com/in/zuhaib-hussain-butt-6628141a4/))

```
