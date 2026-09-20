# Ultimate SDE Prep

A complete, self-contained interview-prep toolkit: DSA, Low-Level Design (OOD), and High-Level Design (System Design). No build step, no dependencies, no server — every page is a single HTML file with the data embedded, and progress is saved in your browser via `localStorage`.

## Use it offline (simplest option)

Download or clone this repo, then just double-click **`index.html`**. Everything works with no internet connection after that — the DSA/LLD/HLD sheets link to each other via relative paths.

```bash
git clone <your-repo-url>
cd <repo-folder>
open index.html   # macOS
# or: xdg-open index.html   (Linux)
# or: start index.html      (Windows)
```

## Host it for free with GitHub Pages (readily accessible from any device)

GitHub Pages, not Codespaces, is the right tool for this — Pages serves static files permanently at a stable URL for free; Codespaces is a billed-by-the-hour dev container meant for coding, not for hosting a page you check daily.

1. Push this repo to your own GitHub account (see below).
2. On GitHub: **Settings → Pages → Source → Deploy from a branch → `main` / `(root)` → Save**.
3. Wait ~1 minute. Your hub is live at `https://<your-username>.github.io/<repo-name>/`.
4. Bookmark it or add it to your phone's home screen — updates automatically every time you `git push`.

## Pushing this to your own GitHub

```bash
cd <this-folder>
git remote add origin https://github.com/<your-username>/<repo-name>.git
git branch -M main
git push -u origin main
```

(This repo is already `git init`-ed with an initial commit — you only need to add your remote and push.)

## What's inside

| File | Contents |
|---|---|
| `index.html` | Hub — links to all three sheets |
| `dsa-sheet.html` | 1,720 DSA problems: Striver A2Z + SDE Sheet, company-frequency lists (Uber/Google/Meta/Amazon/Apple/Netflix/Microsoft), CSES (300), Codeforces ladders (1200→1900). 101 patterns with prerequisite chains. |
| `lld-sheet.html` | OOP → SOLID → 22 of the 23 GoF design patterns with prerequisite chains (Interpreter omitted — a compiler/DSL pattern that's essentially never asked in SDE interviews), 38 OOD case-study problems with requirements/UML/multi-language solutions, concurrency fundamentals + 9 problems. |
| `hld-sheet.html` | 31 system-design building blocks with prerequisite chains, 30 case studies (8 fully worked, 22 linked to primary-source architecture write-ups). |
| `ultimate-sde-prep.xlsx` | The same data as a portable, filterable spreadsheet — import into Google Sheets via File → Import. Less interactive than the HTML sheets (no click-to-filter prerequisite chains), but works anywhere a spreadsheet does. |

## Notes on progress tracking

- Each HTML sheet stores checkboxes/stars in your browser's `localStorage`, scoped to wherever the file is served from. If you move from `file://` to GitHub Pages, or switch browsers/devices, progress does **not** carry over automatically.
- Each sheet has an **Export** button (copies a progress JSON to your clipboard) and **Import** button (pastes it back) — use these to move progress between devices or browsers.
- The `.xlsx` version's progress lives in the spreadsheet file itself (the Status column), so it travels naturally with the file — but it's a separate, unsynced copy from the HTML sheets' progress.

## Source data

- DSA: [`TheAlgorithms`-style scrape] of the Striver A2Z sheet (`geckguy/striver-a2z-sheet`) + SDE Sheet (`abhiiishek07/180DSA`) + company lists (`liquidslr/leetcode-company-wise-problems`) + CSES (`ncduy0303/cses-solutions`) + Codeforces ladders (`rishabhdeepsingh/A2OJ-Ladder`).
- LLD: [`ashishps1/awesome-low-level-design`](https://github.com/ashishps1/awesome-low-level-design) (33 problems, requirements, UML, multi-language solutions) + [algomaster.io](https://algomaster.io) (OOP/SOLID/pattern concept pages).
- HLD: [`donnemartin/system-design-primer`](https://github.com/donnemartin/system-design-primer) (building blocks + 8 worked case studies) + primary-source architecture write-ups for the remaining 15 case studies.
