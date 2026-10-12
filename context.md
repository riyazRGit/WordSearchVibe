# Repository Context

## What this project does
This repository contains self-contained browser games built with plain HTML, CSS, and JavaScript. The games can be opened directly in a browser without a build pipeline or external dependencies.

The Memory Game lets a player:
- flip cards to reveal symbols
- match pairs to clear the board
- track moves and elapsed time
- rate performance with a star system
- switch between 4x4 and 6x6 layouts
- keep local high scores in browser storage
- use keyboard controls for accessibility

The Word Search game generates a letter grid for a chosen category and size. Players find hidden words by dragging across letters or selecting the first and last letters, with keyboard navigation also supported.

## Project structure
- `memory-game.html` — the full game implementation, styling, and logic in one file
- `word-search.html` — the standalone Word Search implementation, styling, and logic
- `PRD_word_search.md` — requirements and acceptance criteria for Word Search
- `README.md` — user-facing overview and quick-start instructions
- `context.md` — this file, summarizing the project purpose and repo context

## How the games work
The Memory Game creates a shuffled deck of emoji pairs, renders the cards in a grid, and tracks player turns. When two cards match, they remain face-up and are marked as matched. Once all pairs are found, the app records the player's result and displays a win modal and score summary.

The Word Search game places selected category words into a generated grid in straight horizontal, vertical, or diagonal directions, then fills the remaining cells with random letters. It tracks found words and elapsed time until the player completes the puzzle.

## What the repo name means
The project name is `memory-game-GHCP`. The `memory-game` portion is clear and descriptive: it is a memory matching game. The `GHCP` suffix is not defined in the codebase or README, so it appears to be a repository or environment label rather than an acronym with business logic behind it. In practical terms, this repo is simply a small front-end game project named with a label suffix.

## Best way to use it
Open either `memory-game.html` or `word-search.html` in a browser, or serve the folder locally with a simple HTTP server if preferred.

Example:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/memory-game.html` or `http://localhost:8000/word-search.html`.

## Summary
This repo is a collection of lightweight, self-contained browser games for learning, fun, and front-end prototyping. It demonstrates interactive games using core web technologies, without frameworks or package installation.
