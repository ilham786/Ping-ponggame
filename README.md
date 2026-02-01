# AI PING PONG 🏓🤖

## Description
This is an interactive AI-powered Ping Pong game that utilizes machine learning to control the gameplay. By integrating the **ml5.js PoseNet** model, the game tracks the player's right wrist movement via webcam to control the paddle in real-time.

## Demo & Preview 📸
Open `index.html` in a browser with webcam access.
Press **Play Game**, stand ~3–4 ft from your laptop, and move your right wrist up/down to control the red paddle.

## Files 🔧
- `index.html` — UI and modal instructions
- `main.js` — Game logic, PoseNet integration, scoring
- `style.css` — Styling and layout

## Features ✨
- **Gesture Control:** The left paddle is controlled by moving your right wrist up and down.
- **Real-time Pose Estimation:** Uses the webcam and PoseNet to detect body keypoints.
- **AI Opponent:** Play against a computer-controlled paddle that tracks the ball.
- **Scoreboard:** Tracks scores for both the Player and the Computer.
- **Game Over Condition:** The game ends when the Computer scores 4 points.
- **Audio Feedback:** Sound effects play when the ball hits the paddle or is missed.

## How to Run ▶️
1. **Clone or download** the project.
2. **Open** `index.html` in Chrome/Firefox (allow webcam access).
   - *Note:* For best performance and permission handling, serve via a local server:
     - **VS Code:** Use the Live Server extension.
     - **Python:** Run `python -m http.server 8000` and visit `http://localhost:8000/AI-PING-PONG/index.html`.
3. Click **Play Game**, grant camera permission, and play.

## Controls & Instructions 🕹️
1. **Setup:**
   - Ensure your laptop screen is straight and you are in a well-lit environment.
2. **Positioning:**
   - Stand approximately **3-4 feet away** from the camera.
   - Ensure your upper body is visible.
3. **Controls:**
   - Move your **right wrist** up and down.
   - A red dot will appear on the screen, tracking your wrist's position (when confidence > 0.2).
   - The red paddle (Player) will move according to your wrist.
4. **Gameplay:**
   - Click **"Play Game"** to start.
   - Defend your side! If the ball passes your paddle, the computer gets a point.
   - **Losing condition:** If the computer reaches a score of 4, the game is over.
   - Click **"Restart"** to play again.

## Development Notes / Tips 💡
- **PoseNet Confidence:** The code uses `scoreRightWrist > 0.2` to filter noise.
- **Adjustable Settings (`main.js`):**
  - Ball speed: `ball.dx` / `ball.dy`
  - Game over score: `if(pcscore == 4) { ... }`
- **Audio:** Sounds loaded are `ball_touch_paddel.wav` and `missed.wav`. You can replace these files in the project root.
- **Difficulty:** Improve difficulty by modifying AI paddle behavior or ball speed.

## Troubleshooting ⚠️
- **No camera feed?** Ensure the browser has permission and test on `localhost` or `https`.
- **Wrist not detected?** Improve lighting and move ~3–4 ft away from the camera so your upper body is in frame.

## Technologies Used
- **HTML5 & CSS3** (Bootstrap framework)
- **JavaScript**
- **[p5.js](https://p5js.org/)** - For graphics and game loop.
- **[ml5.js](https://ml5js.org/)** - For PoseNet machine learning model.

## Contributing 🤝
Bug fixes, improvements, and UI enhancements welcome. Please create issues or PRs.

## License 📜
Use/update as you like — consider adding an MIT license if you want to share permissively.

## Credits
- **Developer:** Ilham
- **Original Concept:** Prashant Shukla
