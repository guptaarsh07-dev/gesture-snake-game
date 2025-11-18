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

bash
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


Snake Game – the playable Pygame window

Gesture Window – webcam preview with MediaPipe landmarks

Press ESC to quit the game window.
Press Q inside the webcam preview window to exit gesture view.

✋ Gesture Controls
Swipe Left/Right/Up/Down
→ Move the snake

Pinch Gesture (thumb touching index)
→ Speed boost activated

Show UP gesture when dead
→ Restart game

ESC Key
→ Quit the game

🧩 How It Works
1. Gesture Detection
gesture_controller.py uses MediaPipe Hand Landmarks to detect wrist movement and finger distance, determining direction and pinch status.

2. Game Logic
snake_game.py maintains:

Snake position

Fruit spawning

Collision detection

Score tracking

Speed boost logic

Rendering & particle effects

3. Integration
main.py links gesture input to snake movement, manages threaded gesture detection, updates the game, and renders both windows.

🐞 Troubleshooting
Gesture not detected?
Improve lighting or adjust camera angle.

Laggy performance?
Reduce particle effects in snake_game.py.

Webcam not opening?
Ensure no other application is using the camera, or change the camera index in main.py.

🚀 Future Improvements
Add keyboard fallback controls

Add settings panel (gesture threshold, sensitivity, grid size)

Add sound effects

Create an executable release

Improve gesture accuracy with smoothing filters

⚠️ Note
Some changes are required and pending for the project's improvement.

