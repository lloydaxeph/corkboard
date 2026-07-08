# Task Corkboard

A single-file task board styled like a corkboard with sticky notes. No build step, no dependencies — open `task-corkboard.html` in a browser and it works.

## Features

- Add, edit, delete, and drag-to-reorder tasks ("notes")
- Subtasks per task with a cyclable status (To do → In progress → Done → Canceled) and a progress bar
- Data is saved automatically to the browser's `localStorage`, so it survives page reloads
- Export the board to CSV and re-import it later (also useful as a manual backup)

## Usage

Just open `task-corkboard.html` in any modern browser. No server or install required.

- **+ New Task** — add a note to the board
- **Load CSV** — replace the current board with one from a CSV file
- **Export CSV** — download the current board as a CSV file
- Click a note's title or a subtask's text to edit it; click the status pill to cycle its status
- Drag a note to reorder the board

## Current limitations

- Data is stored in `localStorage`, which is local to one browser on one device — it does not sync across devices or browsers, and clearing browser data will erase it. Use CSV export as a backup.
- Single-user only; there is no concept of accounts or sharing a board with others yet.

## Roadmap

Deploying this online for multiple people (each with their own private board) is planned but not yet implemented — it will require adding a real backend and accounts, since `localStorage` can't follow a person across devices.
