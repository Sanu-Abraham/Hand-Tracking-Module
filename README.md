# Hand Tracking using Mediapipe

This project implements a hand tracking system using the Mediapipe library and OpenCV in Python. It detects and tracks hand landmarks in an image or video stream, providing the positions of specific landmarks on each hand.

## Dependencies

The following dependencies are required to run the script:

- OpenCV
- Mediapipe

You can install these dependencies using pip:
pip install opencv-python mediapipe

## Usage

To use the `HandTracker` class in your own code, you can import it as follows:

```python
from hand_tracker import HandTracker
```
Then, create an instance of the HandTracker class with your desired configuration:
```python
tracker = HandTracker(mode=False, maxHands=2, modelComplexity=1, detectConf=0.5, trackConf=0.5)
```
You can adjust the parameters based on your requirements. After creating the HandTracker object, you can call its methods to track hands in images or videos.

For example, to track hands in a single image:
```python
import cv2

image = cv2.imread("image.jpg")
tracked_image = tracker.trackHands(image)
landmark_positions = tracker.getPosition(image, handNo=0)
# Process the tracked image and landmark positions as needed
```
Refer to the script for more details and examples on how to use the HandTracker class.
