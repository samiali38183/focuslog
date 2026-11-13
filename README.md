# FocusLog

A Pomodoro timer that asks what you worked on when a session ends and adds it up by day, week and project. It is one HTML file with no build step, no dependencies and no backend.

Live: [focuslog-ochre.vercel.app](https://focuslog-ochre.vercel.app)

## What it does

The timer has focus, short break and long break modes and a circular progress ring. The defaults are 50, 10 and 30 minutes, with a long break after every 4 focus sessions. All four numbers have sliders in Settings. A beep plays when a session ends. Space starts or pauses the timer and R resets it.

When a focus session ends, a prompt asks what you worked on and, optionally, a project or client name. The note is required, but you can skip the whole prompt and nothing is saved. Each saved session keeps a timestamp and its length.

The dashboard shows focus time and session count for today and for this week (weeks start on Sunday), a day streak, a bar chart of minutes per day, and time and sessions per project for the week. Below that is the full session list, where you can delete single sessions. Export CSV downloads every session with date, time, project, note and minutes.

## Run it

```bash
git clone https://github.com/samiali38183/focuslog.git
cd focuslog
```

Open `index.html` in a browser.

## Where the data lives

Sessions are stored in the browser's `localStorage` under the key `focusSessions`. Nothing is sent to a server. History is per browser and per device, and clearing site data deletes it, so export a CSV if you want a copy.

## Limits

The timer counts one-second ticks with `setInterval`. I have not tested how it behaves in a background tab over a long session, and browsers throttle timers in hidden tabs, so keep the tab visible. There are no tests.

## Stack

Plain HTML, CSS and JavaScript in `index.html`, hosted on Vercel.

## License

MIT. See [LICENSE](LICENSE).
