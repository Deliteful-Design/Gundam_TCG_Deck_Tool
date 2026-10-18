# GCG Field Manual

A single-file, no-build reference tool for the Gundam Card Game: current meta report with verified decklists, a searchable card database, a collection tracker, a deck importer (paste text → matched card art), and a win/loss match log with per-deck breakdowns.

Data snapshot: July 2026. Each verified decklist in the Meta Report shows its source (official Bandai deck guide where possible, community tracker otherwise).

## Hosting on GitHub Pages

1. Push this repo to GitHub (public or private both work for Pages on a free account, though private repos need GitHub Pro for Pages).
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Save. GitHub will give you a URL like `https://yourusername.github.io/repo-name/` within a minute or two.

That's it — `index.html` is the entire app, no build step, no dependencies to install.

## How data storage works here

This build uses the browser's `localStorage` API instead of Claude's built-in storage (which only works inside Claude's own interface). That means:

- **Each visitor's collection, saved decks, and match log live only in their own browser**, tied to that specific browser on that specific device.
- Nothing is sent to a server — there isn't one. This is a fully static site.
- If a visitor clears their browsing data, switches browsers, or switches devices, their data won't carry over. There's no login and no sync.
- This is actually the right tradeoff for a public, shared tool: nobody's personal collection or match history is exposed to or mixed with anyone else's.

If you want real cross-device sync down the line, the natural upgrade path is swapping the storage layer for a small backend (e.g. Supabase or Firebase) behind a login — a bigger step, not something to take on before a tournament.

## Backup, restore, and new cards

The **Backup & Custom** tab lets visitors:

- Download a backup file (collection, saved decks, match log, custom cards) and restore it later, in Replace or Merge mode. If downloads are blocked, "Show as text" gives copyable text instead.
- Add cards from new sets themselves, one at a time or in bulk (`ID | Name | Color | Type | Level | Cost | AP | HP | Effect`). Card art loads automatically from the card ID.

Because storage is per-browser, the backup file is also how a visitor moves their data between devices.

## What's real vs. what to verify

The card and deck data embedded in `index.html` is sourced, not invented. Coverage is incomplete, though:

- Card database covers GD01, GD02, ST01–ST06, Beta, and Promos in full, ST11–ST14 and GD05 (stats only, no effect text), plus a handful of individually-verified GD03/GD04 cards. GD03, GD04, ST07–ST10 and EB01 are mostly missing; add them from the Backup & Custom tab.
- The banned/restricted list and legality checker reflect the official list as of Sept 25, 2026. Always verify at gundam-gcg.com before registering a deck.
- 4 of the current top-10 meta archetypes have fully verified 50-card decklists; the rest link out to live trackers.
- Anything without a green "VERIFIED" tag should be treated as a lead to check, not gospel.

## Disclaimer

This is an unofficial fan-made reference tool. All Gundam Card Game names, card text, and imagery belong to SOTSU, SUNRISE, and Bandai. Not affiliated with or endorsed by Bandai.

## Credits / sources

- Card data: [apitcg/gundam-tcg-data](https://github.com/apitcg/gundam-tcg-data) (open source)
- Meta tracking: [gundamtcg.one](https://www.gundamtcg.one), [gundambay.com](https://gundambay.com)
- Official decklists: [gundam-gcg.com](https://www.gundam-gcg.com)
- Community decklists: [exburst.dev](https://exburst.dev)
