# Face Detection and Analysis

This is a real-time face detection and analysis application that uses Haar cascades to detect faces and a Convolutional Neural Network (CNN) to predict whether the detected regions are human faces. The application displays the number of faces detected along with their confidence levels in a webcam feed.

## Features

- **Real-Time Face Detection**: Detects and highlights faces in a live webcam feed using Haar cascades.
- **CNN-Based Face Verification**: Uses a pre-trained CNN model to verify and display confidence levels for detected faces.
- **Bounding Boxes and Labels**: Displays bounding boxes and labels for each detected face with unique identifiers.
- **Face Count Display**: Shows the total number of faces detected on the screen.
- **User-Friendly Interface**: Provides live video feedback with easy-to-interpret results.

## How It Works

### 1. Detection Process
- **Face Detection**: Haar cascades identify regions in the frame likely to contain faces.
- **Preprocessing**: Detected regions are resized and normalized before being passed to the CNN.

### 2. Prediction Process
- The CNN processes the preprocessed images and predicts whether each region contains a human face.
- The model outputs a confidence score (ranging from 0 to 1) for each prediction.

### 3. Result Display
- Bounding boxes are drawn around detected faces, each labeled with an ID and confidence score.
- The total number of detected faces is displayed in real-time on the video feed.

## Why Haar Cascades and CNN?

- **Haar Cascades**: Provide efficient face detection with minimal computational overhead.
- **CNN**: Enhances detection by verifying detected regions and improving accuracy through a confidence metric.

## Installation and Setup

### 1. Clone the Repository
```
git clone https://github.com/<your-username>/face-detection-analysis.git
cd face-detection-analysis 
```
## 2. Install Dependencies

Ensure you have Python installed, then install the required packages:

```
pip install -r requirements.txt
```

## 3. Run the Application
Start the application by running the following command:

```
python face_detection.py 
```

The application will open a real-time webcam feed for face detection.

## File Structure
- **face_detection.py**: Main script for real-time face detection and analysis.
- **haarcascade_frontalface_default.xml**: Haar cascade XML file for detecting faces.
- **models/**: Directory containing the pre-trained CNN model for face verification.

## Future Improvements
- Add emotion recognition for detected faces.
- Implement GPU acceleration for faster CNN inference.
- Extend functionality for image or video file processing.
