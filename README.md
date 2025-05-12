# 👁️‍🗨️ Person Tracking Across Multiple Videos – Computer Vision Assignment

## 🎯 Objective

This project tackles the challenge of **detecting and consistently tracking people across four surveillance-style videos**, even when the same person appears in multiple videos. Each individual is assigned a **unique global ID**, ensuring consistency across all inputs.

---

## 🚀 Approach

### 🔍 Person Detection
- Used **YOLOv8** to detect people in all video frames.
- Filtered detections to keep only the `'person'` class.

### 🧠 Tracking
- Applied **Deep SORT** (Simple Online and Realtime Tracking with a deep appearance descriptor) to track people frame-to-frame within each video.

### 🔁 Cross-Video Re-identification
- Used **cosine similarity** on appearance embeddings to match identities across different videos.
- Ensured consistent global IDs using a mapping strategy.

---

## 📁 Deliverables

| File | Description |
|------|-------------|
| `notebook.ipynb` | Full implementation for detection, tracking, and ID mapping |
| `results.csv` | Final tracking results in required format |
| `requirements.txt` | Python packages used in this project |
| `annotated_videos.zip` | 📦 Annotated videos with bounding boxes and IDs |
| `README.md` | This file |

📦 **Download Annotated Videos**: [Link to Google Drive](https://drive.google.com/your_link_here)

---

## 📝 Output Format (`results.csv`)

This CSV contains one row per person per frame:

