Air-Canvas: Real-Time Virtual Drawing
Air-Canvas is a computer vision-based application that allows users to draw on a digital screen by moving their hands in the air. By leveraging gesture recognition, the platform tracks hand movements to paint in different colors and manage a virtual canvas without any physical contact.

Project Description
Air-Canvas aims to provide:
•	Touchless Interaction: A seamless way to interact with digital canvases using only hand gestures.
•	Real-Time Processing: High-speed tracking of finger landmarks to ensure zero-lag drawing.
•	Interactive Tools: Easy-to-use virtual buttons for color switching (Blue, Green, Red, Yellow) and a "Clear" function.

System Architecture
The Air-Canvas platform consists of three main technical layers:
Input Layer (Camera): Captures real-time video frames using the webcam via OpenCV.
Processing Layer (Mediapipe): Processes the frames to detect 21 hand landmarks and identifies the specific coordinates of the index finger and thumb.
Output Layer (Canvas): Uses NumPy to create a blank white "Paint" window and overlays the drawing points based on the tracked coordinates.

Technical Stack
Language: Python
OpenCV: Used for image processing, camera access, and drawing lines/shapes.
MediaPipe: Google’s open-source framework used for high-fidelity hand landmark detection.
NumPy: Used to create and manage the virtual white canvas (matrix manipulation).
Deques: Used to store the history of points for each color to maintain smooth, continuous lines.

Features and Functionalities
Hand Tracking: Uses mpHands to detect the user's hand with a minimum detection confidence of 0.7.
Gesture Control:
•	Drawing Mode: Moving the index finger allows the user to draw.
•	Stop/New Line: Bringing the thumb close to the index finger (distance < 30) stops the current line.
Virtual Dashboard: The top of the screen features 5 interactive zones:
•	CLEAR: Resets the entire canvas.
•	BLUE / GREEN / RED / YELLOW: Changes the current drawing ink.
Dual Display: Shows both the live webcam feed with landmark overlays and a separate clean white canvas for the final artwork.

Visual Assets Guide
1. Where to add images
•	You should place your images in the following sections of the README to make it readable:
•	Header: Below the main title (use a GIF of the drawing action).
•	System Architecture: Below the architecture description.
•	Actual Output: At the very end of the Features section to show the final result.

2. How to get these images
•	Webcam Drawing GIF: Use a screen recorder (like OBS or Windows Game Bar) to record yourself drawing a shape. Convert it to a .gif using an online converter.
•	Landmark Diagram: You can find the official Mediapipe Hand Landmark Map on Google's developer site.
•	Final Output: While running your code, press PrtSc (Print Screen) on your keyboard to capture the "Output" and "Paint" windows side-by-side.

Future Enhancements
•	Air Eraser: Adding a specific gesture (like a fist) to erase specific parts of the drawing.
•	Variable Thickness: Changing line thickness based on how close the hand is to the camera.
•	Shape Recognition: Automatically converting messy hand-drawn circles or squares into perfect geometric shapes.
•	Save Feature: Adding a button to export the canvas as a .jpg or .png file.

Conclusion
In conclusion, Air-Canvas demonstrates the power of Computer Vision and Human-Computer Interaction (HCI). By combining OpenCV for image manipulation and MediaPipe for robust hand tracking, the project creates an intuitive, touchless drawing experience. While the current version focuses on basic drawing and color selection, the architecture is designed to be scalable, allowing for future integrations like gesture-based commands or advanced artistic tools.

