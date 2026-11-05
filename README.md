# FocusLog

A Pomodoro timer that logs what you worked on and summarizes it by day, week and project. Single HTML file, no build step, no dependencies, no backend.

Live: [focuslog-ochre.vercel.app](https://focuslog-ochre.vercel.app)

## Features

**Timer**
- Focus, short break and long break modes with a circular progress ring
- Defaults to 50 / 10 / 30 minutes with a long break after 4 focus sessions; all four are adjustable with sliders in Settings
- Audio beep when a session ends
- Keyboard shortcuts: Space starts or pauses, R resets

**Logging**
- When a focus session ends, a prompt asks what you worked on (required) and an optional project or client name; you can skip it
- Sessions are saved with a timestamp and duration

**Dashboard**
- Cards for today's and this week's focus time and session count, plus a day streak
- Bar chart of focus minutes per day for the current week
- Time and session count per project for the week
- Full session list with per-session delete
- Export all sessions to CSV (date, time, project, note, duration in minutes)

## Run it

```bash
git clone https://github.com/samiali38183/focuslog.git
cd focuslog
```

Open `index.html` in a browser.

## Data and privacy

Sessions are stored in the browser's `localStorage` under the key `focusSessions`. Nothing is sent to a server. Clearing site data deletes your history, so use Export CSV if you want a copy. History is per browser and per device.

## Built with

Plain HTML, CSS and JavaScript (one file, `index.html`). Hosted on Vercel.

## License

MIT. See [LICENSE](LICENSE).
