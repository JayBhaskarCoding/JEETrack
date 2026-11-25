# JEETrack

JEETrack is a static JEE Main 2027 study planner with two browser layouts:

- **Full dashboard:** the main progress, syllabus, reminders, sync, and backup experience at [`index.html`](./index.html).
- **Compact layout:** a phone-focused daily plan, checklist, timer, and reminders at [`app.html`](./app.html).

Both pages use the same local storage and Firebase sync room. They can be installed separately so the compact layout opens directly on a phone. If cloud sync is unavailable, progress is saved on the current device.

## Publish

The GitHub Pages workflow in [`.github/workflows/static.yml`](./.github/workflows/static.yml) publishes the repository from the `main` branch. The dashboard opens at the site root; the compact layout is at `app.html`.

The service worker caches the page shell for offline opening. Cloud sync and remote visual libraries still need a network connection.
