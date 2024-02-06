# Rock-Paper-Scissors Game with Hand Gestures

## Overview

This Python script implements a simple Rock-Paper-Scissors game using hand gestures captured from a webcam. The game allows the player to compete against the computer (AI) using hand gestures detected by the OpenCV and CVZone libraries. The game's graphical interface displays the current score and winner, and it continues until one player reaches three points.

## Instructions

1. Ensure you have a webcam connected to your system.
2. Run the Python script.
3. To make a move, use your hand gestures in front of the webcam.
4. The game will display the outcome and update the score accordingly.
5. Press 's' to start or restart the game, and 'q' to quit.

## Code Explanation

### Importing Libraries
- `import random`: Importing the random module for generating AI moves.
- `import cv2`: Importing OpenCV for image processing.
- `import cvzone`: Importing the CVZone library for additional computer vision functionalities.
- `from cvzone.HandTrackingModule import HandDetector`: Importing HandDetector class from the HandTrackingModule for hand gesture detection.
- `import time`: Importing time module for time-related operations.

### Initializing Variables
- `cap`: Creating a VideoCapture object to capture video from the webcam.
- `detector`: Creating an instance of the HandDetector class for hand tracking.
- `timer`: Initializing a variable to keep track of time.
- `stateResult`: Initializing a variable to track if the game's result is being displayed.
- `startGame`: Initializing a variable to track if the game has started.
- `scores`: Initializing a list to store the scores of the AI and the player.
- `imgAI`: Initializing a variable to store the image of the AI's move.

### Main Loop
- The main loop captures frames from the webcam and processes them.
- It resizes the captured frame and extracts the region of interest.
- It detects hand gestures using the HandDetector instance.
- If the game is ongoing (`startGame` is True), it calculates the timer, detects the player's move based on hand gestures, generates a random move for the AI, and determines the winner.
- If a player wins three rounds, it displays the winner and stops the game.
- It updates the graphical interface with the scores, winner text, and instructions.
- It handles keyboard inputs to start or quit the game.

## Conclusion

This script provides a simple implementation of the Rock-Paper-Scissors game using hand gestures. It demonstrates the integration of computer vision techniques for gesture recognition and game development using Python.
