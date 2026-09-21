# Cadence: typing test

A fast, mobile-friendly typing speed test built with plain HTML, CSS, and JavaScript. No frameworks, no build step, one file.

**Live demo:** https://nishanth-py.github.io/cadence/

## Features

- Three text types: sentences, random words, and code lines
- 15s, 30s, 60s, and 2 minute tests
- Live WPM, accuracy, and countdown
- Results screen with WPM, accuracy, raw speed, consistency, and mistyped keys
- Speed-over-time chart (drawn as SVG) with markers where mistakes happened
- Keyboard heatmap showing which keys you miss or reach slowly
- Progress tab with history, personal bests per mode, and a heatmap across all tests
- Light and dark theme, three text sizes, and a share button
- Works on phones and laptops; results are saved in the browser only

## How it works

- **Accurate timing:** elapsed time is measured from timestamps, not by counting timer ticks, so the clock does not drift. The timer pauses if the keyboard is closed or the tab is hidden.
- **Fast rendering:** on each keystroke only the characters that changed are repainted, so it stays smooth at high speeds.
- **Mobile keyboards:** input is read by comparing the typed text with the previous text (a diff), which works with on-screen keyboards, backspace, and word suggestions.
- **Stats:** WPM counts only correct characters (5 characters = 1 word). Accuracy counts every keystroke, including ones later fixed. Consistency is based on how steady your per-second speed was.
- **Storage:** history and key stats are saved with `localStorage`, with a fallback if storage is blocked.
- **Accessibility:** visible keyboard focus, sufficient contrast in both themes, and reduced-motion support.

## Run locally

Open `index.html` in any modern browser. Fonts load from Google Fonts when online and fall back to system fonts otherwise.

## Deploy with GitHub Pages

1. Push `index.html` to a repository.
2. Go to **Settings > Pages**, choose the `main` branch and the root folder, and save.
3. Your site appears at `https://nishanth-py.github.io/cadence/`.

## Possible next steps

- Convert to React and TypeScript
- Custom text and punctuation options
- Sound and streak tracking
# cadence