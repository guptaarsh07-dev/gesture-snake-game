# Gesture-Controlled Nokia Snake Game

A modern take on the classic Nokia Snake game — but controlled entirely through **hand gestures** using your webcam.  
The snake responds to swipe gestures for movement and pinch gestures for speed boosts. The game is built using **Pygame**, **OpenCV**, and **MediaPipe**.

---

## 🎮 Features

- **Gesture-based controls**  
  - Swipe **Up / Down / Left / Right** to move the snake  
  - **Pinch** (thumb + index) to activate a speed boost  
- **Retro Nokia-style visuals**
- **Smooth camera-based gesture detection**
- **Particle effects** when the snake eats food
- **Game restart** using an UP gesture after Game Over
- Dual-window system:
  - Pygame game window  
  - OpenCV webcam preview with landmarks & gesture labels

---

## 📁 Project Structure

.
├── main.py # Main entry point, camera + threads + game loop
├── snake_game.py # Game logic, rendering, collisions, particles
├── gesture_controller.py # Hand tracking & gesture detection (MediaPipe)
├── setup.py # Helper script for installing dependencies
└── README.md

yaml
Copy code

---

## 🛠️ Installation

Install dependencies manually:

```bash
pip install pygame mediapipe opencv-python numpy
Or run the included setup script:

bash
Copy code
python setup.py
Ensure your system has a functioning webcam.

▶️ Running the Game
Run the main script:

bash
Copy code
python main.py
Two windows will appear:

