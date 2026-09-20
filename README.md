# 🚩 Astha's Journey — UPSC Prep Dashboard

A single-file, dark-themed, fully offline-capable dashboard for tracking daily UPSC preparation, consistency, and revision — built with vanilla HTML/CSS/JS, Tailwind (via CDN), and Lucide icons. All data is saved locally in your browser via `localStorage` — no backend, no login, no tracking.

## ✨ Features

- **Live Prelims 2027 Countdown** — days / hours / minutes, editable target date.
- **Consistency-adjusted countdown** — shows your real "effective study days" left based on your actual punch-in rate, not just the calendar.
- **The Guilt Engine** — rotating reminders of the competitive and opportunity cost of a wasted day.
- **Weekly Punch Card** — Monday–Sunday grid; click a day to log what you studied and punch in. Tracks your current streak.
- **Micro Planner (Weekly Targets)** & **Macro Planner (Monthly Strategy)** — add, check off, delete.
- **Answer-Writing Counter** — daily tally with an editable weekly goal and progress bar.
- **Syllabus Tracker** — collapsible GS1–GS4, CSAT, and Optional sections with pre-filled UPSC topics, checkboxes, per-subject and overall progress bars, plus support for adding custom topics.
- **Automated Spaced Revision Scheduler** — enter a completed topic, get auto-generated Day 1 / 3 / 7 / 30 revision dates with a done/overdue/pending status.
- **Weekly Review** — a Sunday reflection prompt (what went well / what didn't / plan for next week), with history.
- **Browser Notifications** — optional reminders when a revision is due today, and an evening nudge if you haven't punched in yet (works only while the site is open in a browser tab — see limitations below).
- **Export / Import** — download your entire dashboard as a JSON backup and restore it anytime, on any device/browser.

## 🚀 Deploying on GitHub Pages

1. Push this repo to GitHub (public or private both work).
2. Go to **Settings → Pages** in the repo.
3. Under "Build and deployment," set **Source** to **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
4. Wait about a minute — your site will be live at:
   `https://<your-username>.github.io/<repo-name>/`

That's it. No build step, no dependencies to install — it's a single static `index.html` file.

## 🗂️ Repo structure

```
.
├── index.html   ← the entire app (HTML + CSS + JS in one file)
└── README.md    ← this file
```

## ⚠️ Good to know

- **Data is per-browser, per-origin.** Once you deploy to GitHub Pages, your saved data will start fresh at that URL — it does not carry over automatically from a previous preview link or a different device. Use the **Export** button before switching, then **Import** on the new URL to bring your data with you.
- **Notifications require the tab to be open somewhere** in your browser (it can be in the background). There's no service worker or push server here, so notifications won't fire if the browser itself is fully closed.
- **Back up regularly.** Since everything lives in `localStorage`, clearing your browser data/cache will wipe your dashboard. Use Export weekly (or after big updates) to keep a safe copy.
- Updating `index.html` and pushing new commits does **not** affect your saved data, as long as the site's URL (origin) stays the same.

## 🛠️ Tech stack

- Vanilla HTML, CSS, and JavaScript (no build tools, no frameworks)
- [Tailwind CSS](https://tailwindcss.com/) via CDN (play-CDN script)
- [Lucide Icons](https://lucide.dev/) via CDN
- Browser `localStorage` for persistence
- Browser `Notification` API for reminders

---

🚩 Jai Hanuman — built for discipline, one day at a time.
