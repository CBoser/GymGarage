# Boser Garage Gym

A Progressive Web App (PWA) for tracking strength training workouts in the garage gym.

**Use it now:** [https://cboser.github.io/GymGarage](https://cboser.github.io/GymGarage)

## Install on Your Phone or iPad

1. Open the link above in **Safari**
2. Tap the **Share button** (square with arrow)
3. Tap **"Add to Home Screen"**
4. It runs full-screen like a native app, works offline

## Features

- **3 Workout Days** - Squat + Bench (A), Hinge + OHP (B), Deadlift + Pull (C)
- **Exercise Swaps** - Tap any exercise name to swap it for an alternative (e.g. Rack Pull to Conventional Deadlift)
- **Warmup Section** - Custom description and timer at the start of each workout
- **Rest Timers** - Per-exercise countdown timers with visual alerts
- **Session Timer** - Global elapsed time for the entire workout
- **Workout History** - All saved sessions stored locally on device
- **Program Reference** - Full exercise details, form cues, and progression rules
- **Sync Between Devices** - Export/import workout data between phone and iPad
- **Offline Support** - Works without internet via Service Worker caching

## Cross-Platform Support

Works on iPhone, iPad, and any modern browser. Responsive layouts adapt to your screen:

- **Phone** - Compact single-column layout with touch-optimized controls
- **iPad Portrait** - Wider cards, larger touch targets
- **iPad Landscape** - Two-column exercise grid, side-by-side history cards, three-column program view
- **Safe area insets** - Proper padding for notched devices

## Syncing Data Between Devices

Each device stores workout data locally. To transfer between your phone and iPad:

1. On the source device: go to **Sync** tab, tap **"Copy Data"** (or **"Download Backup"**)
2. On the other device: go to **Sync** tab, paste and tap **"Paste & Import"** (or **"Import File"**)
3. Choose **Merge** to combine data from both devices without duplicates

## Files

| File | Description |
|------|-------------|
| `index.html` | Complete single-page app (HTML, CSS, JS) |
| `manifest.json` | PWA manifest for app installation |
| `sw.js` | Service Worker for offline caching |
| `icon-*.png` | App icons (180, 192, 512px) |

## Data Storage

All workout data is stored in the browser's `localStorage` under the key `bgym_history`. There is no backend server - everything stays on your device.

## Progression Rules

- **Barbell lifts:** +5 lbs when all sets are completed with good form
- **Dumbbell lifts:** +2.5-5 lbs per hand
- **Failed twice?** Drop 10% and rebuild
