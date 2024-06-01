# Drowsiness Detection with YOLOv8

This project uses the YOLOv8 model to detect drowsiness in real-time from a video feed. When drowsiness is detected for a specified duration, an audio alert is played to wake up the person.

## Features

- Real-time drowsiness detection using the YOLOv8 model.
- Audio alerts played when drowsiness is detected.
- Modular design with classes for better organization and maintainability.

## Requirements

- Python 3.x
- `opencv-python`
- `ultralytics`
- `pygame`

## Installation

1. Clone the repository or download the code.
2. Install the required dependencies:

    ```sh
    pip install opencv-python ultralytics pygame
    ```

## Usage

1. Place your audio files (`a.mp3`, `b.mp3`, `c.mp3`, `d.mp3`, `e.mp3`) in the same directory as the script.
2. Ensure that the YOLOv8 model file (`best.pt`) is in the same directory or provide the correct path.
3. Run the script:

    ```sh
    python3 code.py
    ```

## Code Overview

### `AudioPlayer` Class

Handles loading and playing audio files. It also supports asynchronous playback to avoid blocking the main thread.

### `DrowsinessDetector` Class

Processes video frames to detect drowsiness using the YOLOv8 model. It triggers the audio alert if drowsiness is detected for a specified duration.

### `VideoCapture` Class

Manages the video capture from the webcam and integrates with the `DrowsinessDetector` to process each frame.

## Customization

- **Audio Files**: Modify the `audio_files` list in the `AudioPlayer` class to use different audio files.
- **Drowsiness Duration**: Change the `drowsiness_duration` parameter in the `DrowsinessDetector` class to adjust the duration required to trigger the audio alert.

## Acknowledgements

- The YOLOv8 model is provided by [Ultralytics](https://github.com/ultralytics/yolov8).
- Special thanks to the open-source community for the tools and libraries used in this project.
