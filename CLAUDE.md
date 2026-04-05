# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

TOEFL vocabulary learning and quiz application. A vanilla JavaScript single-page web app with Firebase backend for authentication and cross-device data sync. No build tools, no frameworks, no package manager — static HTML/JS served directly in the browser.

## How to Run

Open `index.html` directly in a browser, or serve with any static file server:
- `python3 -m http.server 8000` then visit `http://localhost:8000`
- Or use VS Code Live Server extension

There are **no npm scripts, no build step, no package.json**.

## Technology Stack

- **Vanilla JavaScript (ES6+)** — all logic embedded in HTML files
- **HTML5 / CSS3** — single-file app with inline styles and scripts
- **Firebase v12.11.0 (CDN)** — loaded via ES module imports from `gstatic.com`
  - Firebase Auth (email/password)
  - Cloud Firestore (user data, quiz progress, wrong words)
- **SUITE Variable Font** — Korean-optimized variable font (`SUITE-Variable-woff2/`)
- **Paperlogy Font** — additional font family (`Paperlogy-1.000/`)

## Project Structure

```
voca/
├── index.html              # Main application (2400+ lines, all HTML/CSS/JS)
├── quiz.html               # Quiz variant page
├── words_data.js           # Complete TOEFL vocabulary dataset (30 days)
├── all_days_data.js         # Consolidated word data by day
├── data_day2_10.js          # Days 2-10 vocabulary
├── data_day11_20.js         # Days 11-20 vocabulary
├── data_day21_30.js         # Days 21-30 vocabulary
├── fulltext.txt             # Source text data
├── SUITE-Variable-woff2/    # SUITE font files
└── Paperlogy-1.000/         # Paperlogy font files
```

## Key Features

- **4 quiz types**: Korean→English, English→Korean, Spelling, Matching
- **User auth**: Email/password signup and login via Firebase Auth
- **Progress tracking**: Per-day quiz completion stored in Firestore
- **Wrong words**: Bookmarking and reviewing incorrect answers
- **Cross-device sync**: All user data persisted in Firestore
- **Auto-logout**: 3 hours of inactivity or tab close

## Firebase Configuration

- Project: `the-toefl-lab`
- Auth domain: `the-toefl-lab.firebaseapp.com`
- Firestore: Used for user profiles, quiz progress, wrong words

## Development Guidelines

### Code Organization
- All application code lives in `index.html` (embedded `<script>` tags)
- Vocabulary data is in separate `.js` files loaded via `<script src>`
- No module bundler — scripts load via standard browser mechanisms

### When Editing
- The main app logic is in `index.html` — it's a large file, read specific sections
- Firebase imports use ES modules via CDN (`https://www.gstatic.com/firebasejs/...`)
- CSS is embedded in `<style>` tags within the HTML files
- Be careful with the embedded JavaScript — no linter or type checker is available

### Security Notes
- Firebase API keys are embedded in the HTML (this is normal for client-side Firebase)
- Firestore security rules should be configured in the Firebase console
- Always sanitize user inputs before rendering (XSS prevention)
- Use `textContent` instead of `innerHTML` when displaying user data
