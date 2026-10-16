# ♻️ EcoSort AI — Dry vs. Wet Waste Classifier

An end-to-end intelligent waste segregation system powered by **Ultralytics YOLO11** classification, featuring Apple Silicon (MPS) acceleration and ready for **Streamlit Community Cloud** deployment.

---

## 🌟 Features

- **Real-Time Classification:** Distinguishes between **Dry / Recyclable Waste** (🟦 Blue Bin) and **Wet / Organic Waste** (🟩 Green Bin).
- **High Accuracy:** Fine-tuned on the Kaggle Waste Classification dataset achieving **>92% validation accuracy**.
- **Hardware Adaptive:** Automatically utilizes **Apple Silicon MPS (GPU)** locally on macOS, and effortlessly falls back to **CPU mode** on Streamlit Community Cloud.
- **Multiple Input Modes:**
  - 📁 **File Upload:** Upload any image (JPG, PNG, WEBP).
  - 📸 **Live Webcam:** Real-time capture directly from your browser.
  - ✨ **Sample Gallery:** One-click preloaded test samples.
- **Actionable Guidance:** Provides confidence percentage metrics and proper recycling bin recommendations.

---

## 🛠️ Tech Stack

- **Framework:** Streamlit
- **Model:** Ultralytics YOLO11 Nano Classifier (`best.pt`)
- **Backend:** PyTorch (MPS / CPU)
- **Computer Vision:** OpenCV Headless & Pillow

---

## 🚀 Running Locally

```bash
# 1. Clone repository
git clone https://github.com/kaknayirp/CV_code_clash.git
cd CV_code_clash

# 2. Set up virtual environment
python3 -m venv venv
source venv/bin/activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch Streamlit
streamlit run app.py
```

---

## ☁️ Streamlit Community Cloud Deployment

This repository is pre-configured with:
- `requirements.txt`: Lightweight CPU PyTorch wheels to prevent out-of-memory container crashes.
- `packages.txt`: Linux dependencies (`libgl1`, `libglib2.0-0`) for headless OpenCV execution.
- `best.pt`: Fine-tuned weights included directly in the root directory.
