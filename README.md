# Hand Tracking and Gesture Control

This project utilizes OpenCV and MediaPipe to track hand movements and implement basic gesture-based controls. The script detects hand landmarks, calculates the distance between the index finger tip and thumb tip, and simulates mouse movements and clicks based on the detected gestures.

## Features
- Tracks hand movements using MediaPipe
- Displays real-time FPS on the video feed
- Moves the mouse cursor based on index finger position
- Simulates a mouse click when index finger and thumb come close

## Prerequisites
Make sure you have the following dependencies installed before running the script:

```sh
pip install opencv-python mediapipe pyautogui
```

## How to Run
1. Clone the repository:
   ```sh
   git clone <your-git-repo-link>
   ```
2. Navigate to the project directory:
   ```sh
   cd <project-folder>
   ```
3. Run the script:
   ```sh
   python hand_tracking.py
   ```
4. To exit the application, press `q`.

## Explanation of Key Components
- **Hand Tracking:** Uses MediaPipe's Hand module to detect hand landmarks.
- **FPS Display:** Calculates frames per second and displays on the video feed.
- **Mouse Movement:** Moves the cursor to the detected index finger position.
- **Click Detection:** Calculates the distance between index finger tip and thumb tip. If it falls within a set range, a mouse click is triggered.

## Notes
- Ensure that your webcam is connected and accessible.
- Adjust the threshold values (`threshold_min` and `threshold_max`) if needed to improve click detection accuracy.
- The cursor movement is scaled (`idx_x * 2.5`, `idx_y * 2.5`) to better map hand motion to screen movement. Adjust this scaling factor based on your screen size and hand movements.

## License
This project is for educational and personal use. Modify and use it as needed.

