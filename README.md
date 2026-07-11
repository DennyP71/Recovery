# Recovery Equipment Checkout

A single-page kiosk app for checking recovery/compression equipment in and out at the front desk. Members type their name, tap a device, and the app tracks who has what — including a waiver step and a wait queue for equipment that's at capacity.

## Features

- **Name-based checkout** — enter a name to check equipment in or out; tapping the same name again returns it.
- **Waiver modal** — first-time checkout of a device shows a liability waiver that must be accepted before checkout completes.
- **Compression equipment capacity limit** — the 6 compression devices (Normatec x4, Arms, Hips) share a checkout limit (`COMPRESSION_LIMIT` in `index.html`, currently 4). Once the limit is reached, additional members are offered a spot in the queue instead of being blocked outright.
- **Queue** — members can queue for compression equipment that's at capacity; they're shown their position and automatically removed from the queue once they check the equipment out.
- **`Clearall` command** — typing "Clearall" as a name resets all checked-out equipment and clears the queue (used for end-of-day resets).

## Equipment tracked

Normatec (x3), Normatec (Small), Arms, Hips, Hyperice massage guns (x3), Vyper foam rollers (x2), Inversion Table, Hypersphere (x2), Venom.

## Usage

This is a static HTML/CSS/JS app with no build step or dependencies. Open `index.html` in a browser, or serve the folder with any static file server:

```bash
python3 -m http.server
```

Intended for a kiosk/tablet display at the front desk.

## Project structure

- `index.html` — the entire app (markup, styles, and logic)
- `Assets/` — equipment images
