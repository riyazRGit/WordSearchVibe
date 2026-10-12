# Word Search Vibe

A responsive, accessible word search game that runs in a browser from a single HTML file. No installation, build step, or external dependencies are required.

## Play

Open [`word-search.html`](./word-search.html) in a modern web browser and start a puzzle.

To serve the project locally instead, run:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000/word-search.html>.

## How to play

1. Choose a category: Animals, Food, or Space.
2. Choose a board size: Small (8x8), Medium (10x10), or Large (12x12).
3. Find the words listed beside the letter grid.
4. Drag across a word, or select its first and last letters. Keyboard users can move through the grid with the arrow keys and select endpoints with Enter or Space.
5. Words can be horizontal, vertical, or diagonal, and may read forwards or backwards.
6. Find all listed words to complete the puzzle. Use **New Puzzle** to start over.

## Features

- Randomly generated puzzles with three categories and sizes
- Eight straight-line word directions, including backwards
- Mouse, touch, and keyboard selection
- Found-word highlights, progress counter, and elapsed timer
- Responsive layout with visible focus and screen-reader announcements
- Standalone HTML, CSS, and JavaScript with no third-party dependencies

## Project files

- `word-search.html` — the complete playable game
- `PRD_word_search.md` — product requirements and acceptance criteria
- `README.md` — project overview and instructions

## Technology

The game uses standard HTML, CSS, and JavaScript in a single file. It can be opened directly from disk or served with any static web server.
