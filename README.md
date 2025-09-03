Face Detection Attendance System (Google Colab + Mediapipe)
📌 Project Overview

This project is a real-time face detection attendance system built using Mediapipe and OpenCV.
It captures faces from a webcam (via Google Colab integration), draws bounding boxes around them, and logs detections into a CSV file as attendance records.

👉 Ideal for learning computer vision, experimenting with real-time detection, or showcasing a practical project on your CV.

✨ Features

Real-time face detection using Mediapipe

Bounding boxes drawn around detected faces

Attendance logging into attendance.csv (Name/ID, Date, Time)

Runs on Google Colab (no local setup nightmares)

Supports both webcam streaming and video file processing

🛠️ Tech Stack

Python 3.10+

Google Colab

Mediapipe

OpenCV

NumPy, Matplotlib, CSV

🚀 Setup & Usage
1. Open in Google Colab

Clone or download the notebook, or create a new one in Colab.

2. Install dependencies
!pip install mediapipe opencv-python

3. Run webcam demo

Enable webcam access inside Colab using the provided JavaScript cell, then process frames with Mediapipe to detect faces in real time.

4. Attendance logging

Each detection logs an entry into attendance.csv with:

Name/ID, Date, Time


You can download the CSV file from Colab for further use.

📂 Project Structure
├── face_attendance_mediapipe.py   # Main script (if running locally)
├── Face_Attendance_Colab.ipynb    # Notebook for Google Colab
├── attendance.csv                 # Output attendance log
├── README.md                      # Project documentation

📸 Demo

Faces are detected in real-time via webcam.

A green bounding box highlights detected faces.

Attendance entries are logged automatically.

🔮 Future Improvements

Add face recognition (identify specific people, not just "Person").

Build a Streamlit web app for easier use.

Store attendance in a database (SQLite/PostgreSQL) instead of CSV.

Integrate with Google Sheets for live logging.

👨‍💻 Author

Developed by Mahad

💼 LinkedIn

🐙 GitHub
