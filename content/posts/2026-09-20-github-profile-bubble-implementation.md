# GitHub Profile Upgrade — Bubble Implementation for Rajethakur2

**Date:** 2026-09-20
**Source:** github.com/LHRUN/bubble — Bubble Awesome Profile (510 stars, MIT)
**Profile:** github.com/Rajethakur2

## LinkedIn Version

Your GitHub profile is your CV for developers.

I just rebuilt mine using Bubble — an open-source collection of 35+ ready-to-use README components.

No code from scratch. Just copy, paste, and customise.

What I used:
- Capsule Render for the waving header
- Readme Typing SVG for the animated intro
- GitHub Readme Stats + Streak Stats + Trophy
- Activity Graph for contribution history
- Platane/snk for the contribution snake animation

How it works: Every widget is an image URL that renders live from your GitHub data. Change your username in the URL and it is yours.

My profile was empty last week. Now it tells my story in 5 seconds: Fintech, TravelTech, Bubble.io, Claude and Gemini.

If your profile still looks empty, Bubble is the fastest way to fix it.

Link in comments. What component would you add first?

---

## Facebook Version

Fixed my empty GitHub profile in one afternoon.

Used Bubble — github.com/LHRUN/bubble — a free collection of awesome profiles and README components you can copy.

No building from zero. Just pick your widgets and paste your username.

I added a waving header, animated typing intro, stats cards, streak, trophies, activity graph and the snake.

If you are on GitHub, have a look. Which widget do you like most?

---

## Files Delivered

1. `2026-09-20-github-profile-bubble-readme.md` — Complete README.md to paste into Rajethakur2/Rajethakur2
2. `2026-09-20-github-profile-bubble-snk.yml` — GitHub Action to generate the snake animation

Both files are mirrored to `content-growth-machine/content/posts/` and saved to Desktop.

## How to Publish (2 minutes)

### Option A — GitHub Website (easiest)
1. Go to github.com/Rajethakur2/Rajethakur2 — if the repo does not exist, create it: New repository → Name: `Rajethakur2` → Public → Check "Add a README" → Create
2. Click the pencil icon to edit README.md → delete old content → paste entire content of `2026-09-20-github-profile-bubble-readme.md` → Commit
3. Create folder `.github/workflows` → New file → name it `snk.yml` → paste content of `2026-09-20-github-profile-bubble-snk.yml` → Commit
4. Go to Actions tab → enable workflows if asked → Run workflow once manually → Wait 1 minute → Snake will appear

### Option B — Git Push (if you have local clone)
```bash
git clone https://github.com/Rajethakur2/Rajethakur2.git
cp "C:/Users/GEMTECH 1/Desktop/My Content Posts/2026-09-20-github-profile-bubble-readme.md" Rajethakur2/README.md
mkdir -p Rajethakur2/.github/workflows
cp "C:/Users/GEMTECH 1/Desktop/My Content Posts/2026-09-20-github-profile-bubble-snk.yml" Rajethakur2/.github/workflows/snk.yml
cd Rajethakur2
git add .
git commit -m "feat: upgrade profile with Bubble components"
git push
```

## Components Used (all from Bubble)

- capsule-render → header/footer wave
- readme-typing-svg → animated lines
- github-readme-stats → stats + top langs
- github-readme-streak-stats → streak
- github-profile-trophy → trophies
- github-readme-activity-graph → activity
- Platane/snk → snake

## Customisation Next

Change `theme=tokyonight` to `theme=radical` or `theme=dark` for different colours. Change badge colours in shields.io URLs. Add `github-profile-views-counter` or `leetcode-stats` if needed.

## Proof

Verified Bubble repo live 2026-09-20, demo at bubble-awesome-profile.vercel.app. All components are MIT and free.
