# FaceKey: Secure Biometric Authentication System

FaceKey is a secure, Python-based facial recognition login system that allows users to authenticate using their webcam. It combines **Flask** for the backend API with **DeepFace** for state-of-the-art face verification AI.

## Key Features

*   **Biometric Login**: Authenticate securely using facial recognition instead of passwords.
*   **Liveness Detection**: Includes a "blink detection" mechanism (via MediaPipe) to prevent spoofing with static photos.
*   **Real-time Processing**: Captures and verifies images instantly using client-side JS and server-side analysis.
*   **Privacy-First**: Operates locally without sending biometric data to external cloud APIs.

## Tech Stack

*   **Backend**: Python, Flask
*   **AI/ML**: DeepFace (for recognition), MediaPipe (for face mesh/liveness)
*   **Frontend**: HTML5 Video API, JavaScript
*   **Computer Vision**: OpenCV

## Prerequisites

*   Python 3.8+
*   Webcam

## Installation & Setup

1.  **Clone the repository** (or download the ZIP):
    ```bash
    git clone https://github.com/chidanandgowda/FaceKey.git
    cd FaceKey
    ```

2.  **Create the necessary directories**:
    The system requires folders for storing uploads and known user images.
    ```bash
    mkdir -p static/uploads
    mkdir -p static/user_images
    ```

3.  **Add User Images**:
    *   Add clear photos of authorized users into the `static/user_images` directory.
    *   The filename (e.g., `john_doe.jpg`) will be used as the username.

4.  **Install Dependencies**:
    ```bash
    pip install mediapipe opencv-python flask deepface numpy
    ```

5.  **Run the Application**:
    ```bash
    python app.py
    ```

6.  **Access the Login Page**:
    *   Open your browser and navigate to `http://localhost:5000` (or the link printed in your terminal).
    *   Allow camera access when prompted.
    *   Blink your eyes to trigger the login process!

