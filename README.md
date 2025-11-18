# Gesture-Controlled Nokia Snake Game

A modern take on the classic Nokia Snake game — but controlled entirely through **hand gestures** using your webcam.  
The snake responds to swipe gestures for movement and pinch gestures for speed boosts. The game is built using **Pygame**, **OpenCV**, and **MediaPipe**.

---
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
```
▶️ Running the Game
Run the main script:

css
Copy code
python main.py
Two windows will appear:

Snake Game – the playable Pygame window

Gesture Window – webcam preview with MediaPipe landmarks

Press ESC to quit the game window.
Press Q inside the webcam preview window to exit gesture view.

✋ Gesture Controls
Swipe Left/Right/Up/Down → Move the snake

Pinch gesture → Speed boost

UP gesture on Game Over → Restart

ESC → Quit game

🧩 How It Works
Gesture Detection
gesture_controller.py tracks hand landmarks and detects:

wrist movement for direction

pinch distance for boost

Game Logic
snake_game.py handles:

snake movement

fruit spawning

collisions

particle effects

game restart state

Integration
main.py connects gesture input to game actions and manages both windows.

🐞 Troubleshooting
Gesture not detected?
Improve lighting or adjust camera angle.

Laggy performance?
Reduce particle settings in snake_game.py.

Webcam not opening?
Ensure no other app is using the camera or change camera index in main.py.

🚀 Future Improvements
Keyboard fallback controls

Adjustable gesture sensitivity

Better smoothing for gesture detection

Executable release

Sound effects

⚠️ Note
Some changes are required and pending for the project's improvement.
