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

```
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
```

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

```
FinSL/
  ├── backend/
  └── frontend/
```

---

## 🚀 How to Run the Project

### Backend Setup

1. **Create the root and backend folders**
   ```bash
   mkdir FinSL
   cd FinSL
   mkdir backend
   cd backend
   ```

2. **Copy backend files**
   Copy the following files into the backend folder:
   - `requirements.txt`
   - `sign_model_tf213_new.h5`
   - `label_encoder_new.pkl`

3. **Install backend dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Copy and paste the main.py file**

5. **Run the Backend**
   ```bash
   uvicorn main:app --reload
   ```
   The backend will usually run at: `http://127.0.0.1:8000`

### Frontend Setup

1. **Return to the root folder**
   Place the frontend files inside the FinSL folder and extract them

2. **Go to the frontend folder after extracting**

3. **Install frontend dependencies**
   ```bash
   npm install
   ```

4. **Run the frontend**
   ```bash
   npm run dev
   ```
   The frontend will usually run at: `http://localhost:5173`

### How to Run the Full System

1. Start the backend server from the backend folder
2. Start the frontend server from the frontend folder
3. Open the frontend in your browser
4. Upload a sign video through the interface
5. The system will process the video and display the predicted Finnish sign label

---

## 🔮 Future Improvements

- Collect larger multi-signer dataset
- Expand vocabulary
- Improve signer-independent recognition
- Add real-time detection
- Explore Transformer-based models