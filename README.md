# Task Corkboard

A single-file task board styled like a corkboard with sticky notes. No build step, no dependencies — open `index.html` in a browser and it works.

<img width="1235" height="597" alt="image" src="https://github.com/user-attachments/assets/f89b7852-6f15-4503-9a60-ba3f5f4a3f98" />

## Features

- Add, edit, delete, and drag-to-reorder tasks ("notes")
- Subtasks per task with a cyclable status (To do → In progress → Done → Canceled) and a progress bar
- Data is saved automatically to the browser's `localStorage`, so it survives page reloads
- Export the board to CSV and re-import it later (also useful as a manual backup)

## Usage

Just open `index.html` in any modern browser. No server or install required.

- **+ New Task** — add a note to the board
- **Load CSV** — replace the current board with one from a CSV file
- **Export CSV** — download the current board as a CSV file
- Click a note's title or a subtask's text to edit it; click the status pill to cycle its status
- Drag a note to reorder the board

## Current limitations

- Data is stored in `localStorage`, which is local to one browser on one device — it does not sync across devices or browsers, and clearing browser data will erase it. Use CSV export as a backup.
- Single-user only; there is no concept of accounts. If this is deployed to a shared URL, everyone who visits gets their own independent board (scoped to their own browser's `localStorage` for that domain) — boards are not shared or synced between visitors.

## Deploying to Cloudflare Pages

This is a static site, so no build step is required.

1. Push this repo to GitHub (already done if you're reading this from the repo).
2. In the [Cloudflare dashboard](https://dash.cloudflare.com/), go to **Workers & Pages → Create → Pages → Connect to Git**.
3. Select this repository and authorize Cloudflare's GitHub App if prompted.
4. Framework preset: **None**. Build command: leave blank. Build output directory: `/` (repo root).
5. Click **Save and Deploy**. Cloudflare will give you a `*.pages.dev` URL — every push to `main` redeploys automatically.

## Roadmap

Real accounts and a shared/synced backend (so a person's board follows them across devices) are not implemented — the current deployment relies on each visitor's own browser storage.
