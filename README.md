# Link: 
# FIA Act 1974 — Case File Preparation

A self-contained, single-file quiz website for preparing for exams based on the **Federal Investigation Agency Act, 1974** (Pakistan). Styled as an official case-file dossier, it covers all sections of the Act with randomized multiple-choice questions.

## Contents

- `fia-act-quiz.html` — the entire app (HTML, CSS, and JavaScript in one file). No build step, no server, no dependencies to install.

## Features

- **50 MCQs** covering the Act end-to-end: short title & extent, definitions, constitution of the Agency, superintendence & administration, powers of members, Public Prosecutors (Sec. 15A), amendment of the Schedule, delegation of powers, indemnity, rule-making, and repeal/transfer provisions.
- **Choose your dossier length** — quick 10-question drills, or the full 50.
- **Randomized every session** — question order and answer-option order are reshuffled each time you start, so you can't just memorize positions.
- **Instant feedback** — correct/incorrect marked immediately after each answer, with a running score and progress bar.
- **Results summary** — a pass/fail stamp, your final percentage, and a review list of every question you got wrong with the correct answer shown.
- **No accounts, no tracking, no backend** — everything runs client-side in the browser; nothing is saved or sent anywhere.

## How to use

1. Download `fia-act-quiz.html`.
2. Open it in any modern web browser (double-click it, or right-click → Open With → your browser).
3. Choose how many questions you want, click **"Open the case file"**, and start answering.
4. At the end, review anything you missed and click **"Reopen Case File"** to try again with a fresh shuffle.

## Updating the questions

All question data lives in a single JavaScript array near the top of the `<script>` section, named `QUESTIONS`. Each entry looks like this:

```js
{ s: "Sec. 3", q: "Question text here?", o: ["Option A", "Option B", "Option C", "Option D"], a: 1 }
```

- `s` — the section label shown as a tag above the question.
- `q` — the question text.
- `o` — an array of exactly 4 answer options.
- `a` — the index (0–3) of the correct option in `o`.

To add, remove, or edit questions, just edit this array directly — no other code needs to change. The quiz engine automatically picks up the new count for shuffling and length options.

## Notes

- Content is sourced from the Federal Investigation Agency Act, 1974, for self-study purposes only and is not a substitute for reading the official Act text.
- Works offline once downloaded — the only external resources are Google Fonts (loaded via CDN for the letterhead/typewriter typography); the quiz logic itself needs no internet connection.
