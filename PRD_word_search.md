# Product Requirements Document: Word Search

## 1. Overview

Create a self-contained Word Search game as a new HTML file in this repository. Players find a list of hidden words in a letter grid by selecting each word from its first letter to its last. The game must run directly in a modern browser without a server, framework, external library, or build step.

## 2. Goals

- Deliver a complete, playable word search in one HTML file with embedded CSS and JavaScript.
- Make new puzzles from built-in word categories and three board sizes.
- Support mouse, touch, and keyboard input.
- Clearly communicate found words, progress, elapsed time, and completion.
- Keep the existing Memory Game and its files unchanged.

## 3. Users

Casual players, including children and families, who want a simple word-finding game that opens and plays in a browser.

## 4. User stories

- As a player, I can choose a word category and puzzle size so I can play a puzzle that suits me.
- As a player, I can find words horizontally, vertically, and diagonally, in either direction.
- As a player, I can select a word by dragging across its letters or by choosing its start and end letters.
- As a player, I can see which words I have found and how many remain.
- As a player, I can start another puzzle without reloading the page.
- As a keyboard or assistive-technology user, I can navigate the grid, select word endpoints, and hear game status updates.

## 5. Functional requirements

### FR1: Puzzle setup

- Provide category choices for at least Animals, Food, and Space.
- Provide Small (8x8), Medium (10x10), and Large (12x12) puzzle sizes.
- A new puzzle is generated on page load, when a setting changes, and when the player selects New Puzzle.
- Each puzzle contains a word list sized to its difficulty and a matching letter grid.

### FR2: Word placement

- Place every listed word in a straight line horizontally, vertically, or diagonally.
- Words may run forward or backward.
- Fill all unoccupied cells with random uppercase letters.
- Do not silently show an incomplete puzzle: if generation fails, display an explicit error and allow retry.

### FR3: Selection and matching

- Support pointer dragging over a straight line of letters, including touch.
- Also support selecting a start cell and then an end cell, so selection does not rely on dragging.
- Accept only exact listed words, in either direction.
- Reject non-straight selections and words not in the current list.
- Keep found words selectable when cells overlap other hidden words.

### FR4: Progress and completion

- Show found/total word count and mark found words in both the grid and word list.
- Start the timer on the first selection and stop it when all words have been found.
- Show a clear completion state and elapsed time when the puzzle is solved.
- Let the player start a fresh puzzle at any time.

### FR5: Accessibility and responsive behavior

- Make grid cells keyboard-focusable using a roving focus pattern; arrow keys move focus and Enter/Space select endpoints.
- Provide visible keyboard focus and sufficient text/background contrast.
- Use an accessible label for each cell and a polite live region for status/progress announcements.
- Keep controls and the grid usable on narrow screens and touch devices.

## 6. Non-functional requirements

- Use only standard HTML, CSS, and JavaScript; no external network requests or dependencies.
- Keep puzzle generation and selection responsive for all supported board sizes.
- Do not modify the existing Memory Game behavior or its score data.
- Handle invalid word selections and puzzle-generation failures with clear player-facing messages.

## 7. Out of scope

- Online multiplayer, accounts, or server-side features.
- Downloadable/shareable puzzles, custom word entry, or external word APIs.
- Persistent player profiles or leaderboards.
- Sound effects or a hint/solver system.

## 8. Proposed interface

The page has a title and short instructions, category and size selectors, a New Puzzle button, elapsed time and progress, a word bank, a responsive letter grid, and an announced completion message. Players may drag a straight line or click/tap/keyboard-select its two endpoints.

## 9. Acceptance criteria

1. Opening the HTML file directly in a browser creates a playable puzzle without network access.
2. All configured words are present in the generated grid, and the grid is fully populated.
3. Selection accepts words in all eight straight-line directions and their reversals.
4. Drag, touch, click/tap endpoint, and keyboard endpoint selection work.
5. Incorrect selections do not mark words as found or increment progress.
6. Found words are visibly marked; overlapping cells remain usable for other words.
7. Category, size, and New Puzzle controls each create a fresh puzzle and reset progress and timer.
8. The timer starts on the first selection and completion is announced after the last word.
9. Grid navigation has visible focus, cell labels, and live status announcements.
10. Existing Memory Game files and behavior remain unchanged.

## 10. Validation plan

- Open the HTML file locally and verify a puzzle appears with a non-empty word list.
- Test each board size and category, and verify New Puzzle resets progress and time.
- Find words using drag and endpoint selection, including reversed and diagonal words.
- Try an invalid line and a non-listed word; confirm neither is counted.
- Verify completion and timer behavior, keyboard arrows/Enter/Space, screen-reader labels, and mobile-width layout.
- Confirm the existing Memory Game still opens and plays independently.

## 11. Definition of done

The standalone HTML file meets the acceptance criteria, has no external dependencies, does not replace the existing game, and is ready for the player to open and test.
