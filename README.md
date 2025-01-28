# Face Recognition Attendance System

A modern attendance tracking system that uses facial recognition to log employee/student check-ins and check-outs. The system consists of a FastAPI backend for face recognition processing and a React frontend for user interaction.

## Features

- Face Recognition-based login/logout
- New user registration
- Attendance log generation and export
- Real-time face detection and matching
- Cross-Origin Resource Sharing (CORS) enabled
- CSV-based attendance logging with timestamps
- Downloadable attendance reports

## Tech Stack

### Backend
- Python 3.10
- FastAPI
- OpenCV
- face_recognition
- uvicorn
- starlette

### Frontend
- React.js
- npm

## Prerequisites

Before running the application, ensure you have the following installed:
- Python 3.x
- Node.js and npm
- Required Python packages:
  ```
    opencv-python-headless
    fastapi
    face-recognition
    cmake
    python-multipart
    uvicorn
  ```


## Installation and Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <project-directory>
   ```

2. Backend Setup:
   ```bash
   # Create and activate virtual environment (optional but recommended)
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   
   # Install required packages
   pip install fastapi python-multipart uvicorn opencv-python face_recognition
   ```

3. Frontend Setup:
   ```bash
   cd face-attendance-web-app-front
   npm install
   ```

## Running the Application

1. Start the Backend Server:
   ```bash
   # From the backend directory
   uvicorn main:app
   ```
   The server will start at `http://localhost:8000`

2. Start the Frontend Development Server:
   ```bash
   # From the frontend directory
   npm start
   ```
   The application will open in your default browser at `http://localhost:3000`

## API Endpoints

### POST `/login`
- Handles user login through face recognition
- Requires an image file upload
- Returns user identification and match status

### POST `/logout`
- Handles user logout through face recognition
- Requires an image file upload
- Returns user identification and match status

### POST `/register_new_user`
- Registers a new user in the system
- Requires an image file and user name
- Stores face embeddings in the database

### GET `/get_attendance_logs`
- Downloads attendance logs as a ZIP file
- Contains CSV files with attendance records


## Acknowledgments

- face_recognition library
- FastAPI framework
- OpenCV contributors