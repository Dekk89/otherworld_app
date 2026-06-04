# Otherworld 2026 — My Planner

A tiny, **offline-first personal schedule planner** for the Otherworld 2026 festival.
One self-contained HTML file. No install, no account, no server. Star the events you
care about and build your weekend — your picks stay private on your own phone.

> Unofficial & community-made. Not affiliated with Kindle Arts Society or Otherworld.

## What it does

- **Browse** all 1,000+ events — filter by type (🏕️ Camps · 🔊 Sound Stages · 🎨 Art · 🚐 Mutant Vehicles)
  and by day (Thu → Mon), or search across titles, camps and descriptions.
- **⭐ Star** anything to add it to **My Schedule** — grouped by day, sorted by time,
  with a gentle ⚠︎ warning when two of your picks overlap.
- **Works fully offline.** It pulls the live community schedule once while you have
  signal, caches it on your device, and runs dark all weekend.
- **`✓ Verified`** pill shows events whose camp owners maintain their own listing.

## Use it on your phone

1. Open **`index.html`** on your phone (email it to yourself, AirDrop it, or host it — see below).
2. While you still have signal, tap **⟳** to download the schedule.
3. **Add to Home Screen** (Share → Add to Home Screen on iOS; menu → Install on Android)
   so it opens like a real app — offline.

That's it. Your favourites are saved in the browser's local storage on that device.
Use **Settings → Export favourites** to back them up or move them to another phone.

## Where the data comes from

The schedule is the canonical community feed, fetched live from:

```
https://raw.githubusercontent.com/Isaiiaas/OtherworldWWW/master/events.json
```

That file is CORS-open, so the app can read it directly from any device with no proxy.
It's reconciled from a shared Google Sheet roughly hourly, so a quick **⟳ Refresh**
before you head out gets you the latest.

**No signal and need to load it?** Grab the raw `events.json`, then in
**Settings → Paste data** paste its contents to load the schedule manually.

## Files

| File | What it is |
|------|------------|
| `index.html` | The entire app — HTML, CSS and JS in one file. This is all you need. |
| `events.json` | A snapshot of the schedule (handy as an offline import; the app fetches live by default). |
| `README.md` | This file. |

## Hosting (optional)

Drop `index.html` on any static host (GitHub Pages, Netlify, a USB stick…). Because the
data feed is CORS-open, the live fetch keeps working from anywhere.

## Privacy

Everything is local. Your favourites never leave your device — there's no backend and
no analytics. The only network call is fetching the public schedule feed.
