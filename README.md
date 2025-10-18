# Gesture-Based Brightness Control

Control your screen brightness using hand gestures! This project uses computer vision to track your hand movements and adjust screen brightness based on the distance between your thumb and index finger.

## Features

- **Real-time hand tracking** using MediaPipe
- **Gesture-based control**: Adjust brightness by pinching thumb and index finger together or apart
- **Visual feedback**: See hand landmarks and distance line on screen
- **Smooth brightness mapping**: Distance range (15-220 pixels) maps to brightness (0-100%)

## How It Works

The system captures video from your webcam, detects your hand using MediaPipe, and measures the distance between your thumb tip (landmark 4) and index finger tip (landmark 8). This distance is then mapped to a brightness value between 0-100%.

## Requirements

```bash
pip install opencv-python mediapipe screen-brightness-control numpy
```

## Installation

1. Clone or download this repository
2. Install the required dependencies:
   ```bash
   pip install opencv-python mediapipe screen-brightness-control numpy
   ```
3. Run the script:
   ```bash
   python brightnesscontrol.py
   ```

## Usage

1. Run the script
2. Position your hand in front of the webcam
3. Pinch your thumb and index finger together to decrease brightness
4. Spread them apart to increase brightness
5. Press **'q'** to exit

## Controls

- **Gesture**: Thumb-Index finger distance controls brightness
- **Quit**: Press 'q' to stop the program

## Technical Details

- **Hand Landmarks Used**: 
  - Landmark 4: Thumb tip
  - Landmark 8: Index finger tip
- **Distance Range**: 15-220 pixels
- **Brightness Range**: 0-100%
- **Framework**: OpenCV for video capture, MediaPipe for hand detection

## Notes

- Works best in well-lit environments
- Ensure your hand is clearly visible to the camera
- The brightness adjustment is system-wide
- Compatible with Windows, macOS, and Linux (depending on screen-brightness-control library support)

## Troubleshooting

- **Camera not opening**: Check if another application is using the webcam
- **Brightness not changing**: Ensure screen-brightness-control supports your system
- **Hand not detected**: Improve lighting or move closer to the camera

## License

Free to use and modify for personal and educational purposes.
