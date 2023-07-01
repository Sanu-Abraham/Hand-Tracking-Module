# Hand Tracking Module using Mediapipe

This module provides a Python implementation of hand tracking using the Mediapipe library and OpenCV. It enables the detection and tracking of hand landmarks in images or video streams, allowing for applications that involve hand gesture recognition, augmented reality, and more.

## Dependencies

The following dependencies are required to use the module:

- OpenCV
- Mediapipe

You can install these dependencies using pip:

```shell
pip install opencv-python mediapipe
```

## Usage

To use the Hand Tracking module, import it in your Python code:

```python
from hand_tracking import HandTracker
```

Then, create an instance of the `HandTracker` class with your desired configuration:

```python
tracker = HandTracker(mode=False, maxHands=2, modelComplexity=1, detectConf=0.5, trackConf=0.5)
```

You can adjust the parameters according to your specific requirements. Once the `HandTracker` object is created, you can call its methods to track hands in images or video frames.

For example, to track hands in a single image:

```python
import cv2

image = cv2.imread("image.jpg")
tracked_image = tracker.trackHands(image)
hand_landmarks = tracker.getPosition(image)
# Process the tracked image and hand landmarks as needed
```

Refer to the script for more details and examples on how to use the `HandTracker` class.

## Acknowledgements

The hand tracking functionality in this module is based on the Mediapipe library, which provides the hand tracking model used for detecting and tracking hand landmarks.
