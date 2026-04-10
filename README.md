# 🤟 Finnish Sign Language Recognition System (FinSL)

This project presents a **baseline Finnish Sign Language (FinSL) recognition system** using hand landmark extraction and deep learning. The system takes a video as input and predicts the corresponding sign using a trained LSTM model.

---

## 📌 Overview

Finnish Sign Language recognition is a challenging task due to the **lack of large, diverse datasets**. This project aims to demonstrate a **working end-to-end pipeline** under low-resource conditions.

The system includes:
- 🎥 Video input (offline upload)
- ✋ Hand landmark extraction using MediaPipe
- 📊 Feature preprocessing and normalization
- 🧠 Temporal modeling using LSTM
- 🌐 Web-based interface (frontend + backend)

---

## 🏗️ System Architecture
User Video Upload
↓
Backend (FastAPI)
↓
MediaPipe Hand Landmark Extraction
↓
Normalization + Sequence Processing
↓
LSTM Model Prediction
↓
Output Label (or UNKNOWN)


---

## ⚙️ Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- MediaPipe
- FastAPI (Backend)
- React (Frontend)

---

## 📁 Project Structure
├── model/
│  training_code.py
│  sign_model.h5
│  label_encoder.pkl


├── backend/
│  main.py


├── frontend/
│  React app files


---

## 🚀 How to Run the Project

### Backend Setup

cd backend
pip install -r requirements.txt
uvicorn main:app --reload

cd frontend
npm install
npm run dev

Upload Video
Open the frontend in your browser
Upload a sign video
The system will predict the sign label

🔮 Future Improvements
Collect larger multi-signer dataset
Expand vocabulary
Improve signer-independent recognition
Add real-time detection
Explore Transformer-based models

🔮 Future Improvements
Collect larger multi-signer dataset
Expand vocabulary
Improve signer-independent recognition
Add real-time detection
Explore Transformer-based models
