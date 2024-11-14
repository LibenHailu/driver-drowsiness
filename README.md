# Driver Drowsiness Detection

## Overview
The Driver Drowsiness Detection project utilizes computer vision techniques to monitor the driver's alertness by analyzing facial landmarks. The program captures video from the webcam and calculates the eye and mouth aspect ratios to determine if the driver is drowsy. If drowsiness is detected, a warning is displayed on the screen.

## Code Explanation
The main components of the `DriverDrowsiness.py` script are as follows:

1. **Library Imports**:
   - The script imports necessary libraries such as `numpy`, `dlib`, and `cv2` for numerical operations, facial landmark detection, and image processing, respectively.

2. **Video Capture**:
   - The script initializes video capture from the webcam using OpenCV.

3. **Facial Landmark Detection**:
   - Dlib's frontal face detector and shape predictor are used to identify facial landmarks, which are crucial for calculating eye and mouth aspect ratios.

4. **Aspect Ratio Calculations**:
   - The `eye_aspect_ratio` and `mouth_aspect_ratio` functions compute the respective ratios based on the positions of facial landmarks. These ratios help in assessing the driver's alertness.

5. **Real-time Monitoring**:
   - The script continuously captures frames from the webcam, processes them to detect faces, and calculates the eye and mouth aspect ratios.
   - If the calculated ratios indicate drowsiness (based on predefined thresholds), a warning is displayed on the screen.

6. **User Feedback**:
   - The program provides visual feedback by drawing rectangles around detected faces and displaying the alert status (either "Sleepy" or "Alert").

## Features
- Real-time detection of drowsiness using facial landmarks.
- Visual alerts for the driver when drowsiness is detected.
- Easy integration with any webcam.

## Requirements
- Python 3.x
- OpenCV
- Dlib
- NumPy

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/DriverDrowsinessDetection.git
   cd DriverDrowsinessDetection
   ```

2. Install the required libraries:
   ```bash
   pip install opencv-python dlib numpy
   ```

3. Download the Dlib shape predictor model:
   - Download the `shape_predictor_68_face_landmarks.dat` file from [Dlib's model repository](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2) and place it in the project directory.

## Usage
Run the script using:
```bash
python DriverDrowsiness.py
```
Ensure your webcam is connected and accessible. The program will open a window displaying the video feed. If the driver is detected to be drowsy, a "Sleepy" warning will appear on the screen.

## Notes
- The thresholds for eye and mouth aspect ratios can be adjusted based on testing and requirements.
- Ensure proper lighting conditions for better detection accuracy.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- [Dlib](http://dlib.net/) for the facial landmark detection.
- [OpenCV](https://opencv.org/) for computer vision functionalities.