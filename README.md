# Tic-Tac-Toe Web Application — Task 03 (Prodigy InfoTech Web Dev Internship)

This is my submission for Task 03 of the Prodigy InfoTech web development internship. The brief was to build a Tic-Tac-Toe game where users can play against each other or against an AI opponent.

## What it does

- **2 Player mode** — X and O take turns on the same device.
- **Vs AI mode** — you play X, the computer plays O and responds automatically after a short "thinking" delay.
- Detects wins across all 8 possible patterns (rows, columns, diagonals) and highlights the winning cells.
- Detects a draw when the board fills up with no winner.
- Reset button clears the board and starts a fresh round in whichever mode is currently selected.

## Tech used

- **HTML** for the board and mode/status controls
- **CSS** (internal, inside a `<style>` tag) for the grid layout and styling
- **JavaScript** (internal, inside a `<script>` tag) for game logic, win detection, and the AI

Everything lives in one file — no external `.css` or `.js` links, so it's fully self-contained and runs by just opening `index.html`.

## How it's built

The board is just a 9-element array (`null`, `'X'`, or `'O'`), and after every move it's checked against 8 hardcoded win patterns — three in a row, column, or diagonal — plus a draw check if the board is full with no winner.

The AI isn't random — it uses the **minimax algorithm**, which plays out every possible sequence of remaining moves recursively and scores each outcome (win for O = positive, win for X = negative, draw = 0), preferring wins that happen sooner and losses that happen later. This makes it effectively unbeatable — the best a human can force is a draw.

## Files
HTML + internal CSS + internal JS, all in one file
