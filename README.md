# 🎓 Smart Attendance System — AI-Based Face Recognition for Online Classes

An AI/ML-powered attendance management system that automatically detects and recognizes students' faces during online classes and records their attendance in real time. Built entirely with **pure Python** and **core AI/ML concepts**, without relying on heavy third-party attendance frameworks.

---

## 📌 Overview

Traditional attendance methods (roll calls, manual entry, sign-in sheets) are time-consuming and prone to proxy attendance. This project solves that problem by using **computer vision and machine learning** to detect a student's face via webcam/video feed, recognize their identity against a trained dataset, and automatically log their attendance — with timestamp — into a structured record (CSV/database).

---

## ✨ Features

- 🎥 **Real-time face detection** from webcam or video stream
- 🧠 **Face recognition** using trained ML models on student face datasets
- 📝 **Automated attendance logging** with name, date, and time
- 🚫 **Duplicate-entry prevention** (marks each student only once per session)
- 📊 **Attendance reports** exportable as CSV/Excel
- 👤 **Student registration module** to add new faces to the dataset
- 🔒 Works offline — no cloud dependency required
- ⚙️ Lightweight, built with pure Python and open-source ML libraries

---

## 🏗️ How It Works

1. **Dataset Creation** – Capture and store multiple face images per student using the webcam.
2. **Face Encoding / Model Training** – Extract facial features (encodings) from the dataset and train/store the recognition model.
3. **Real-Time Detection & Recognition** – During a live class session, the system continuously scans the video feed, detects faces, and matches them against known encodings.
4. **Attendance Marking** – On successful recognition, the student's attendance is automatically recorded with a timestamp, avoiding duplicate entries for the same session.
5. **Report Generation** – Attendance data is saved and can be exported for review.

---

## 🛠️ Tech Stack

| Component            | Technology                          |
|-----------------------|--------------------------------------|
| Language              | Python 3.x                          |
| Face Detection        | OpenCV (Haar Cascades / DNN module) |
| Face Recognition      | `face_recognition` / LBPH / custom ML model |
| Data Handling         | Pandas, NumPy                       |
| Storage               | CSV / SQLite                        |
| GUI (optional)        | Tkinter / Streamlit                 |

*(Update this table to match the exact libraries used in your implementation.)*

---

## 📂 Project Structure

```
face-attendance-system/
│
├── dataset/                  # Stored face images of registered students
├── trainer/                  # Trained model / encodings
├── attendance/                # Generated attendance CSV/Excel files
├── src/
│   ├── register_faces.py     # Capture & register new student faces
│   ├── train_model.py        # Train/encode facial data
│   ├── recognize_attendance.py # Real-time detection & attendance marking
│   └── utils.py               # Helper functions
├── requirements.txt
└── README.md
```

*(Adjust folder/file names to match your actual repo layout.)*

---

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/face-attendance-system.git
   cd face-attendance-system
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

---

## ▶️ Usage

### 1. Register Students
```bash
python src/register_faces.py
```
Captures face images via webcam and saves them under the student's name in the `dataset/` folder.

### 2. Train the Model
```bash
python src/train_model.py
```
Processes the dataset and generates facial encodings/model used for recognition.

### 3. Start Attendance Session
```bash
python src/recognize_attendance.py
```
Opens the webcam feed, detects and recognizes faces in real time, and logs attendance automatically.

### 4. View Attendance Records
Check the `attendance/` folder for the generated CSV file with student name, date, and time of entry.

---

## 📋 Requirements

- Python 3.8+
- Webcam / camera device
- Libraries listed in `requirements.txt` (e.g., `opencv-python`, `face_recognition`, `numpy`, `pandas`)

---

## 🚀 Future Enhancements

- Integration with live video-conferencing platforms (Zoom/Google Meet) for direct attendance capture
- Web-based dashboard for teachers to monitor attendance analytics
- Liveness detection to prevent photo/video spoofing
- Cloud database integration for multi-class, multi-session support
- Email/SMS notifications for absentees

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repository, raise issues, or submit pull requests to improve detection accuracy, add features, or enhance the UI.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 🙋 Author

Developed as an AI/ML mini-project demonstrating real-time face recognition applied to automated classroom attendance systems.
