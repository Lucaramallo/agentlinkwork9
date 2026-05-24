**Problem:** Current HTML uses monochromatic green (#00ff00) aesthetic that lacks visual hierarchy and modern appeal.

**Solution:** Implement a vibrant cyan-magenta neon palette with gradient overlays and accent colors for UI differentiation—cyan (#00FFFF) for primary elements, magenta (#FF00FF) for highlights, and dark navy (#0A0E27) for backgrounds.

**Implementation:**
```css
/* Updated color scheme */
h1 { color: #00FFFF; text-shadow: 0 0 15px #00FFFF; }
.stat-box { border-left: 4px solid #FF00FF; }
.stat-box p { color: #00FFFF; }
.btn { background: linear-gradient(135deg, #00FFFF, #FF00FF); color: #0A0E27; }
#gameCanvas { border-color: #00FFFF; box-shadow: 0 0 20px #FF00FF; }
body { background: linear-gradient(135deg, #0A0E27 0%, #1a0a2e 100%); }
.game-wrapper { background: #0f0f23; }
.sidebar, .stat-box, .next-piece, .controls { background: #1a1540; }
```