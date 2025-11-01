# Face Recognition Attendance System

A real-time face detection and attendance logging system built with Mediapipe and OpenCV. This project can run in Google Colab or locally, detecting faces from webcam streams or images and automatically logging attendance records to a CSV file.

## 📋 Features

- **Real-time Face Detection**: Uses Mediapipe for accurate face detection
- **Visual Feedback**: Draws bounding boxes around detected faces
- **Automatic Attendance Logging**: Logs detections with timestamps to CSV
- **Flexible Deployment**: Works in Google Colab or locally
- **Multiple Input Sources**: Supports webcam streaming and image file processing

## 🛠️ Tech Stack

- **Python** 3.10+
- **Mediapipe** - Face detection engine
- **OpenCV** - Image processing and visualization
- **NumPy** - Numerical operations
- **Matplotlib** - Image display
- **CSV** - Attendance logging

## 📦 Installation

### For Local Development

1. Clone the repository:
```bash
git clone https://github.com/yourusername/Face-Recognition.git
cd Face-Recognition
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install mediapipe opencv-python matplotlib numpy
```

### For Google Colab

1. Upload the `code.ipynb` notebook to Google Colab
2. Install dependencies in the first cell:
```python
!pip install mediapipe opencv-python
```

## 🚀 Usage

### Google Colab

1. Open `code.ipynb` in Google Colab
2. Run all cells in sequence
3. Upload images when prompted (the notebook handles file upload)
4. View detected faces with bounding boxes
5. Download the generated `attendance.csv` file

### Local Usage

Run the notebook locally or create a Python script based on the notebook code:

```python
import cv2
import mediapipe as mp
import matplotlib.pyplot as plt

# Initialize Mediapipe Face Detection
mp_face = mp.solutions.face_detection
mp_draw = mp.solutions.drawing_utils
face_detection = mp_face.FaceDetection(min_detection_confidence=0.6)

# Load image
img = cv2.imread('path/to/image.jpg')
rgb_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Process with Mediapipe
results = face_detection.process(rgb_img)

# Draw detections
if results.detections:
    for detection in results.detections:
        mp_draw.draw_detection(img, detection)

# Display result
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```

## 📂 Project Structure

```
Face-Recognition/
├── code.ipynb              # Main Jupyter notebook
├── README.md               # Project documentation
├── .gitignore             # Git ignore rules
├── attendance.csv          # Output attendance log (generated)
└── images/                # Input images (optional)
```

## 📊 Attendance Log Format

The system generates `attendance.csv` with the following format:

| Name/ID | Date       | Time     |
|---------|------------|----------|
| Person  | 2025-02-20 | 03:08:37 |

## 🎯 Future Enhancements

- [ ] Face recognition to identify specific individuals (beyond generic "Person")
- [ ] Database integration (SQLite/PostgreSQL) for persistent storage
- [ ] Streamlit web application for easy interface
- [ ] Google Sheets integration for real-time collaboration
- [ ] Real-time webcam streaming for continuous monitoring
- [ ] Email notifications for attendance events
- [ ] Multi-face detection with individual identification

## 👨‍💻 Author

**Mahad**

- 💼 [LinkedIn](https://linkedin.com/in/yourprofile)
- 🐙 [GitHub](https://github.com/yourusername)

## 📄 License

This project is open source and available for educational purposes.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

---

**Note**: This project is designed for educational purposes. For production use, consider implementing additional security measures and user authentication.
