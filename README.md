# Browser Mini Games

This repository contains lightweight, responsive browser games built with plain HTML, CSS, and JavaScript. Each game is self-contained and can be opened directly in a browser.

## Games

### Memory Game

A Memory (Concentration) card game. See [memory-game.html](./memory-game.html).

Features:

- 4x4 and 6x6 grid options
- Smooth card flip animations
- Timer and moves counter
- Star rating system
- Local storage for best scores
- Keyboard controls for accessibility
- Responsive design for all devices
- No external dependencies

### Word Search

A word-finding puzzle with a generated letter grid. See [word-search.html](./word-search.html).

Features:

- Animals, Food, and Space word categories
- Small (8x8), Medium (10x10), and Large (12x12) boards
- Find words horizontally, vertically, and diagonally, forwards or backwards
- Select words by dragging or choosing their first and last letters
- Keyboard navigation, elapsed timer, and live progress announcements
- No external dependencies

## How to Play the Memory Game

1. Open `memory-game.html` in a web browser
2. Click or use keyboard (Tab + Enter/Space) to flip cards
3. Find matching pairs to win
4. Try to complete the game with as few moves as possible
5. Switch between 4x4 and 6x6 grids using the buttons

## How to Play Word Search

1. Open `word-search.html` in a web browser
2. Choose a word category and board size
3. Find each word listed beside the grid
4. Drag across a word, or select its first and last letters with a click, tap, or keyboard
5. Words may run in any straight direction, including backwards and diagonally
6. Find every word to complete the puzzle; choose **New Puzzle** to play again

## Technical Details

- Each game is implemented as a standalone HTML file with embedded CSS and JavaScript
- No external libraries or dependencies
- Responsive layouts using CSS Grid
- Accessibility features including keyboard controls and assistive-technology announcements
- The Memory Game uses local storage for persistent high scores

## Development

1. Clone the repository
2. Open either `memory-game.html` or `word-search.html` in a web browser
3. Or serve using a local HTTP server:
   ```bash
   python3 -m http.server 8000
   ```
4. Visit `http://localhost:8000/memory-game.html` or `http://localhost:8000/word-search.html`