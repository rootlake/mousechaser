# Mouse Chaser Game

A simple, interactive browser-based game where players must avoid a chaser that follows their mouse cursor. The game increases in difficulty over time as the chaser's speed gradually increases.

## 🎮 Game Overview

Mouse Chaser is a survival-style game built with vanilla HTML, CSS, and JavaScript. The objective is simple: keep your mouse cursor away from the red chaser for as long as possible. The longer you survive, the faster the chaser becomes, making the game progressively more challenging.

## ✨ Features

- **Real-time mouse tracking**: The chaser follows your cursor position in real-time
- **Progressive difficulty**: Speed increases over time (multiplier increases every 10 seconds)
- **Live timer**: Displays elapsed time during gameplay
- **Speed indicator**: Shows current speed multiplier
- **Collision detection**: Game ends when chaser catches the cursor
- **Game over screen**: Displays final survival time
- **Restart functionality**: Play again without page reload
- **Responsive design**: Works on different screen sizes
- **Smooth animations**: Uses `requestAnimationFrame` for fluid movement

## 🎯 How to Play

1. Open `index.html` in a web browser
2. Move your mouse cursor around the screen
3. Avoid the red chaser circle
4. Try to survive as long as possible
5. When caught, view your final time and click "Play Again" to restart

## 🛠️ Technical Details

### Technologies Used
- **HTML5**: Structure and semantic markup
- **CSS3**: Styling, gradients, animations, and responsive design
- **Vanilla JavaScript**: Game logic, event handling, and animations

### Key Implementation Details

- **Movement Algorithm**: Uses vector mathematics to calculate direction and distance between chaser and cursor
- **Speed Calculation**: Base speed of 0.5 pixels per frame, multiplied by time-based factor
- **Collision Detection**: Euclidean distance calculation between circle centers
- **Animation Loop**: `requestAnimationFrame` for smooth 60fps updates
- **Event Handling**: Mouse move events tracked on the game container

### Code Structure

```javascript
// Core game loop
updateChaser()     // Updates chaser position each frame
updateTimer()      // Updates timer and speed multiplier
checkCollision()   // Detects when chaser catches cursor
endGame()          // Handles game over state
restartGame()      // Resets game to initial state
```

## 🚀 Getting Started

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/rootlake/mousechaser.git
cd mousechaser
```

2. Open `index.html` in your web browser:
   - Simply double-click the file, or
   - Use a local server: `python -m http.server` or `npx serve`

### GitHub Pages

The game is automatically deployed to GitHub Pages:
**https://rootlake.github.io/mousechaser/**

## 📁 Project Structure

```
mousechaser/
├── index.html              # Main game file (HTML, CSS, JS)
├── README.md              # Project documentation
├── LICENSE                # MIT License
└── .github/
    └── workflows/
        └── deploy.yml     # GitHub Pages deployment workflow
```

## 🎨 Design Features

- **Gradient background**: Purple gradient for visual appeal
- **Glowing effects**: Box shadows on game elements for depth
- **Custom cursor**: Hidden default cursor, replaced with green indicator
- **Smooth transitions**: CSS transitions for polished feel
- **Modern UI**: Clean, minimalist interface with clear typography

## 🔧 Customization

You can easily customize the game by modifying variables in the JavaScript:

- `baseSpeed`: Initial speed of the chaser (default: 0.5)
- Speed increase rate: Modify `speedMultiplier = 1.0 + (elapsed / 10)` to change difficulty curve
- Chaser size: Adjust `width` and `height` in CSS `#chaser`
- Collision distance: Change `distance < 30` threshold in `checkCollision()`

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

Josh Lake

## 🙏 Acknowledgments

- Built as a simple, fun browser game demonstration
- Uses modern web APIs and best practices
- No external dependencies required

