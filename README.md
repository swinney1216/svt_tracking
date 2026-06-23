# SVT Episode Tracker

A minimal Progressive Web App (PWA) for logging SVT (Supraventricular Tachycardia) episode start and stop times. One tap to start, one tap to stop and save.

## Features

- **One-tap tracking** — big START button, tap again to save the episode
- **Persistent** — active episode survives phone restarts (stored in localStorage)
- **Offline-ready** — works without a network connection after first load
- **Export to CSV** — all episodes with ISO 8601 start/stop times and duration in seconds
- **Install to home screen** — runs as a standalone app (no browser chrome)

## CSV format

```
episode,start,stop,duration_seconds
1,2025-06-23T14:30:00.000Z,2025-06-23T14:47:23.000Z,1043
```

## Hosting on GitHub Pages (free)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set Source to **Deploy from a branch → main → / (root)**
4. Your app will be live at `https://<your-username>.github.io/svt_tracking/`

## Using on iPhone

1. Open the app URL in **Safari** (not Chrome — Safari is required for PWA install)
2. Tap the **Share** button (box with arrow)
3. Tap **"Add to Home Screen"**
4. The app icon will appear on your home screen and opens full-screen like a native app

> **Note:** For a true home-screen widget (showing the button without opening the app), a native Swift app with WidgetKit would be needed. This PWA is the closest web equivalent.

## Icons (optional)

Add `icon-192.png` and `icon-512.png` to the repo root for a custom home-screen icon. Without them the app still works but uses a default browser icon.

A quick way to generate them: use any image editor to create a 512×512 PNG with the design you want, then resize to 192×192 for the smaller size.

## Garmin watch

Garmin Connect IQ apps (written in Monkey C) can be built to log events — this would be a separate project requiring the Connect IQ SDK. The data could sync to the same backend or be exported separately.
