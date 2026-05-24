# DELIVERABLE

## FILE 1: index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tetris Game</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <div class="game-wrapper">
            <div class="sidebar">
                <h1>TETRIS</h1>
                <div class="stats">
                    <div class="stat-box">
                        <label>Score</label>
                        <p id="score">0</p>
                    </div>
                    <div class="stat-box">
                        <label>Lines</label>
                        <p id="lines">0</p>
                    </div>
                    <div class="stat-box">
                        <label>Level</label>
                        <p id="level">1</p>
                    </div>
                </div>
                <div class="next-piece">
                    <label>Next</label>
                    <canvas id="nextCanvas" width="100" height="100"></canvas>
                </div>
                <button id="startBtn" class="btn">Start Game</button>
                <button id="pauseBtn" class="btn" disabled>Pause</button>
                <div class="controls">
                    <p><strong>Controls:</strong></p>
                    <p>← → : Move</p>
                    <p>↑ : Rotate</p>
                    <p>↓ : Drop</p>
                </div>
            </div>
            <canvas id="gameCanvas" width="300" height="600" role="img" aria-label="Tetris game board"></canvas>
        </div>
    </div>
    <script src="tetris.js"></script>
</body>
</html>
```

## FILE 2: style.css
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    background: linear-gradient(135deg, #0a0e27 0%, #1a0a3a 100%);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #e0e0e0;
}

.container {
    padding: 20px;
}

.game-wrapper {
    display: flex;
    gap: 30px;
    background: #0f0f23;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 10px 40px rgba(0, 255, 255, 0.1);
}

.sidebar {
    width: 200px;
    display: flex;
    flex-direction: column;
    gap: 20px;
}

h1 {
    color: #00d4ff;
    text-align: center;
    font-size: 28px;
    text-shadow: 0 0 15px #00d4ff;
}

.stats {
    display: grid;
    grid-template-columns: 1fr;
    gap: 10px;
}

.stat-box {
    background: #1a1540;
    padding: 15px;
    border-radius: 5px;
    border-left: 4px solid #ff006e;
}

.stat-box label {
    display: block;
    font-size: 12px;
    color: #888;
    text-transform: uppercase;
    margin-bottom: 5px;
}

.stat-box p {
    font-size: 24px;
    color: #00d4ff;
    font-weight: bold;
}

.next-piece {
    background: #1a1540;
    padding: 15px;
    border-radius: 5px;
    text-align: center;
}

.next-piece label {
    display: block;
    font-size: 12px;
    color: #888;
    text-transform: uppercase;
    margin-bottom: 10px;
}

#nextCanvas {
    background: #0d0d1f;
    border-radius: 3px;
    display: block;
    margin: 0 auto;
    border: 1px solid #00d4ff;
}

.btn {
    padding: 12px 20px;
    background: linear-gradient(135deg, #00d4ff 0%, #ff006e 100%);
    color: #0f0f23;
    border: none;
    border-radius: 5px;
    font-weight: bold;
    cursor: pointer;
    transition: all 0.3s;
    font-size: 14px;
}

.btn:hover:not(:disabled) {
    box-shadow: 0 0 15px #00d4ff, 0 0 10px #ff006e;
    transform: translateY(-2px);
}

.btn:disabled {
    opacity: 0.5;
    cursor: not-allowed;
}

.controls {
    background: #1a1540;
    padding: 15px;
    border-radius: 5px;
    font-size: 12px;
    border-left: 3px solid #00d4ff;
}

.controls p {
    margin: 5px 0;
    color: #aaa;
}

#gameCanvas {
    background: #000;
    border: 3px solid #00d4ff;
    border-radius: 5px;
    image-rendering: pixelated;
    box-shadow: 0 0 20px #00d4ff, 0 0 40px rgba(255, 0, 110, 0.3);
}

@media (max-width: 768px) {
    .game-wrapper {
        flex-direction: column;
        align-items: center;
    }
    
    .sidebar {
        width: 100%;
    }
}
```

---

**Changes Applied:**
- **Primary Color:** Cyan (#00d4ff) replaces neon green for improved eye comfort and modern aesthetics
- **Accent Color:** Magenta (#ff006e) introduces visual hierarchy and accent highlights
- **Background:** Deepened dark navy gradient (#0a0e27 to #1a0a3a) for reduced eye strain during extended play
- **Contrast Ratio:** Cyan-on-dark meets WCAG AA standards; magenta accents enhance UI differentiation
- **Button States:** Gradient background with enhanced glow effects on hover for better affordance
- **Box Shadow:** Layered cyan/magenta glows maintain cyberpunk aesthetic while improving visual feedback