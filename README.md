⚽ World Cup 2026 — Live Tracker
A lightweight, single-file web app to follow the 2026 FIFA World Cup in real time. Built for the office — open it in any browser, no install required.

🇦🇷 All times shown in Argentina time (ART / UTC–3)


🚀 How to use it
👉 Just open gasparduarte.github.io/Worldcup2026 — that's it.

No API key, no setup. The page loads fresh data on its own and keeps refreshing while you have it open (every minute during live matches, every 5 minutes otherwise).

⚙️ How it works
A GitHub Action fetches live data from football-data.org roughly every 5 minutes and commits it to `data.json` in this repo. The page just reads that file — no key needed in the browser.

- The Action keeps itself alive by re-dispatching at the end of each run (GitHub heavily throttles 5-minute cron schedules, so the cron alone is only a safety net).
- It stops automatically when the tournament ends (July 20, 2026).
- Emergency brake: create a file called `STOP` in the repo root and updates halt.
- The API key lives in the repo secret `FOOTBALL_DATA_TOKEN` (Settings → Secrets → Actions).

✨ Features

📅 Full fixture list — all 104 matches with dates, times, and venues
📊 Live standings — official group tables straight from the API
🏆 Knockout bracket — Round of 32 through the Final
👟 Top scorers — live golden boot race
🇦🇷 Argentina tab — dedicated view for La Scaloneta's matches and road to the title
⏱️ Countdown — live timer to the next Argentina match
🔄 Auto-refresh — no reload needed, scores appear on their own
🌙 Dark / light mode — toggle in the top right corner
🎮 Demo mode — preview with fake results, no key needed


ℹ️ Notes

Live data is provided by football-data.org (free tier). Final scores can take a little while to be confirmed there — if a match just ended, give it a few minutes.


Made with ❤️ for the team, World Cup tracker
