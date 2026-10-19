# Question of the Day — Jas & Lan

A tiny daily ritual: one coin flip, one wheel spin, one question — every day, between two people.

## How it works

1. **Coin toss.** The app alternates each day whose turn it is to call it — Jas one day, Lan the next. Tap Heads or Tails and watch the coin flip.
2. **Winner spins.** Whoever called the coin correctly (or the other person, if they didn't) gets to spin a 1,000-slice color wheel.
3. **Question revealed.** The wheel lands on a question — a Would You Rather, a True or False fact (with the answer underneath), or a Guess the Outcome brain-teaser — pulled from a pool of 1,000, never repeated.
4. **Counter.** The top of the page always shows how many of the 1,000 have been used so far.

## Tech notes

This is a single self-contained `index.html` — no build step, no server, no dependencies. All 1,000 questions are embedded directly in the page.

**Progress is stored in your browser's `localStorage`**, on whichever device you open it on. That means:
- It's zero-setup and free to host anywhere static files are served.
- Progress does **not** sync between devices — if Jas and Lan each open it on their own phone, they'll see different coin flips/questions. It works best opened together on one shared device (or on a laptop you both use), or revisit later if you want real cross-device sync (e.g. via Firebase) and ask for it to be added.
- Clearing browser data / using a different browser / incognito mode will reset progress. There's a "reset all progress" link at the bottom of the page if you ever want to start over on purpose.

## Hosting on GitHub Pages

This repo is set up to deploy automatically via GitHub Actions on every push to `main`. Once the first push lands:

1. Go to the repo's **Settings → Pages**.
2. Under **Build and deployment → Source**, select **GitHub Actions** (if it isn't already).
3. Your site will be live at:
   `https://sheepdogfan2019.github.io/dailyquestion/`

(First deploy can take a minute or two after the workflow run finishes.)

## Local preview

Just open `index.html` directly in a browser — no server needed.
