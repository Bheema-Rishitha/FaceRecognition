# Face Recognition Attendance System

An automated attendance tracking web application built with Python, Streamlit, DeepFace, and RetinaFace. The system replaces manual roll calls by detecting and recognizing student faces from uploaded classroom images and logging attendance records automatically.

🌐 **Live Demo:** [View App on Streamlit Cloud](https://facerecognition-dxalvvwkrpqneltbzhgbb2.streamlit.app/)

## Features

- **Role-Based Access Control:** Separate workflows for Admins (registering students, processing attendance, managing records) and Students (viewing personal attendance logs).
- **Face Detection & Embedding Extraction:** Uses RetinaFace to locate faces in images and DeepFace (Facenet512) to generate facial embeddings.
- **Automated Attendance Logging:** Matches detected faces against registered student embeddings using cosine similarity and exports daily attendance logs to structured CSV files organized by subject and date.
- **Visual Verification:** Annotates processed classroom photos with bounding boxes and confidence scores.
- **Account Management:** Includes SHA-256 password hashing, input validation, and password recovery workflows.

## Tech Stack

- **Frontend / UI:** Streamlit
- **Computer Vision & AI:** OpenCV, RetinaFace, DeepFace (Facenet512)
- **Data Processing:** NumPy, Pandas
- **Storage:** Local Pickle serialization, JSON, and CSV logs

## Local Setup & Installation

1. Clone the repository:
   git clone https://github.com/Bheema-Rishitha/FaceRecognition.git
   cd FaceRecognition

2. Create and activate a virtual environment:
   python -m venv venv
   venv\Scripts\activate

3. Install dependencies:
   pip install -r requirements.txt

4. Run the application:
   streamlit run app.py