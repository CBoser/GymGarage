# Boser Garage Gym

A Progressive Web App (PWA) for tracking father & son strength training workouts in the garage gym.

## Features

- **3 Workout Days** - Squat + Bench (A), Hinge + OHP (B), Deadlift + Pull (C)
- **Alternating Set Tracking** - Log weights and completion for both Corey and Son side-by-side
- **Rest Timers** - Per-exercise countdown timers with visual alerts
- **Session Timer** - Global elapsed time for the entire workout
- **Workout History** - All saved sessions stored locally on device
- **Program Reference** - Full exercise details, form cues, and progression rules
- **Offline Support** - Works without internet via Service Worker caching
- **Install as App** - Add to home screen on iOS/iPadOS for a native app experience

## iPad Support

The app includes responsive layouts optimized for iPad and iPad Pro:

- **Portrait** - Wider cards, larger touch targets, more breathing room
- **Landscape** - Two-column exercise grid, side-by-side history cards, three-column program view
- **Safe area insets** - Proper padding for devices with home indicators
- **Both orientations** - Full support for rotating the device during a workout

## Setup

No build step required. Serve the files with any static web server:

```bash
# Using Python
python3 -m http.server 8000

# Using Node.js
npx serve .
```

Then open `http://localhost:8000` in a browser or on your iPad.

### Install on iPad

1. Open the URL in Safari
2. Tap the Share button
3. Select "Add to Home Screen"
4. The app will run in standalone fullscreen mode

## Files

| File | Description |
|------|-------------|
| `index.html` | Complete single-page app (HTML, CSS, JS) |
| `manifest.json` | PWA manifest for app installation |
| `sw.js` | Service Worker for offline caching |

## Data Storage

All workout data is stored in the browser's `localStorage` under the key `bgym_history`. There is no backend server - everything stays on your device.

## Progression Rules

- **Barbell lifts:** +5 lbs when all sets are completed with good form
- **Dumbbell lifts:** +2.5-5 lbs per hand
- **Failed twice?** Drop 10% and rebuild
