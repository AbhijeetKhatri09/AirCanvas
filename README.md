# Air-Canvas: Real-Time Virtual Drawing

Air-Canvas is a computer vision-based application that allows users to draw on a digital screen by moving their hands in the air. By leveraging gesture recognition, the platform tracks hand movements to paint in different colors and manage a virtual canvas without any physical contact.

<img width="1594" height="636" alt="image" src="https://github.com/user-attachments/assets/057b8065-1dc5-4e97-a2e2-418be9c4bb78" />


---

## Project Description
Air-Canvas aims to provide:

* **Touchless Interaction:** A seamless way to interact with digital canvases using only hand gestures.
* **Real-Time Processing:** High-speed tracking of finger landmarks to ensure zero-lag drawing.
* **Interactive Tools:** Easy-to-use virtual buttons for color switching (Blue, Green, Red, Yellow) and a "Clear" function.

---

## System Architecture
The Air-Canvas platform consists of three main technical layers:

* **Input Layer (Camera):** Captures real-time video frames using the webcam via OpenCV.
* **Processing Layer (Mediapipe):** Processes the frames to detect 21 hand landmarks and identifies the specific coordinates of the index finger and thumb.
* **Output Layer (Canvas):** Uses NumPy to create a blank white "Paint" window and overlays the drawing points based on the tracked coordinates.
  
  <img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/85b1a645-20b7-4d60-8f53-e0640af1687e" />


---

## Technical Stack
* **Language:** Python
* **OpenCV:** Used for image processing, camera access, and drawing lines/shapes.
* **MediaPipe:** Google’s open-source framework used for high-fidelity hand landmark detection.
* **NumPy:** Used to create and manage the virtual white canvas (matrix manipulation).
* **Deques:** Used to store the history of points for each color to maintain smooth, continuous lines.

---

## Features and Functionalities
* **Hand Tracking:** Uses `mpHands` to detect the user's hand with a minimum detection confidence of 0.7.
* **Gesture Control:**
    * **Drawing Mode:** Moving the index finger allows the user to draw.
    * **Stop/New Line:** Bringing the thumb close to the index finger (distance < 30) stops the current line.
* **Virtual Dashboard:** The top of the screen features 5 interactive zones: **CLEAR**, **BLUE**, **GREEN**, **RED**, and **YELLOW**.
  
  <img width="1597" height="635" alt="image" src="https://github.com/user-attachments/assets/a619a318-9e23-4d0b-bf2f-94b7edce2bd1" />


---

## Conclusion
In conclusion, Air-Canvas demonstrates the power of Computer Vision and Human-Computer Interaction (HCI). By combining OpenCV for image manipulation and MediaPipe for robust hand tracking, the project creates an intuitive, touchless drawing experience.
