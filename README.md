# Gesture-Controlled-Virtual-Painter

## Project Description

Gesture Controlled Virtual Painter is a computer vision based drawing application that allows users to paint on the screen using hand gestures instead of a mouse or stylus. The application uses a webcam to track hand movements and converts finger motion into drawing actions.

By moving the index finger, the user controls a virtual brush. Pushing the finger forward toward the camera activates drawing, while lifting it stops drawing. Users can change colors using a gesture-based menu and erase drawings using a virtual eraser tool.

The program integrates real-time hand tracking, gesture recognition, and interactive graphics to create a touchless digital painting experience.

## Objective

The objective of this project is to demonstrate how machine learning based hand tracking can be used to build gesture-controlled creative applications. It showcases how computer vision can replace traditional input devices like a mouse or touchscreen.

## Features

* Real-time hand tracking using webcam
* Gesture-controlled drawing system
* Virtual brush with dynamic thickness
* Color selection using dwell-based gesture menu
* Eraser tool for removing drawings
* Gesture-based canvas clearing using fist detection
* Z-axis push detection to activate drawing
* Smooth cursor movement with interpolation
* Transparent drawing canvas overlay
* Real-time brush preview
* Interactive gesture menu interface

## Technologies and Libraries Used

Python 3

Libraries:

* OpenCV (cv2) – Used for webcam video capture and image processing
* MediaPipe – Used for machine learning based hand landmark detection
* Pygame – Used for creating the graphical interface and rendering drawings
* NumPy – Used for mathematical calculations and gesture detection
* Time – Used for dwell-time based interactions
* OS – Used for locating the hand tracking model file

## Machine Learning Model

The application uses the MediaPipe Hand Landmarker model to detect and track hand landmarks in real time.

Model file required:
hand_landmarker.task

This file must be placed in the same directory as the Python script.

## How the Program Works

1. The webcam captures live video frames.
2. MediaPipe processes each frame to detect hand landmarks.
3. The index finger tip acts as the cursor controlling the brush.
4. The distance between the thumb and index finger dynamically adjusts brush thickness.
5. The system checks the Z-axis position of the finger to determine whether the user is "pushing" to draw.
6. When pushing forward, the program draws lines on a transparent canvas.
7. When the hand moves into the top menu area, a color selection interface appears.
8. Holding the finger over a color for a few seconds selects that color.
9. Selecting the eraser tool allows the user to erase parts of the drawing.
10. Making a fist gesture clears the entire canvas.

## Gesture Controls

Index Finger Movement
Moves the cursor across the screen.

Push Gesture
Move the finger toward the camera to start drawing.

Release Gesture
Pull the finger back to stop drawing.

Color Selection
Move the cursor to the top menu and hold over a color button for a few seconds.

Eraser Tool
Select the eraser from the menu to remove parts of the drawing.

Fist Gesture
Closing all fingers into a fist clears the entire canvas.

## How to Run the Program

Step 1: Install required Python libraries

pip install opencv-python mediapipe pygame numpy

Step 2: Download the MediaPipe hand tracking model

hand_landmarker.task

Step 3: Place the model file in the same directory as the Python script.

Step 4: Run the program

python virtual_painter.py

Step 5: Allow access to your webcam.

The drawing interface will open and begin tracking your hand.

## System Requirements

* Python 3.8 or later
* Webcam
* Basic GPU/CPU capable of real-time video processing
* Screen resolution recommended: 1280×720 or higher

## Possible Improvements / Future Work

* Add more brush types (spray, marker, pencil)
* Add shape drawing tools (circle, rectangle, line)
* Implement undo and redo functionality
* Add save and export options for artwork
* Support multi-hand gesture controls
* Add gesture-based color palette expansion
* Improve gesture recognition accuracy
* Add background templates for drawing

## Conclusion

This project demonstrates how computer vision and machine learning can be used to create innovative touchless creative tools. By combining MediaPipe hand tracking with Pygame graphics rendering, the application transforms hand gestures into a powerful digital painting interface.
