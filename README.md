# Hangar

An unofficial, single-file reference tool for the Gundam Card Game. No build step, no server: `index.html` is the whole app.

## What it does

- **Meta Report:** the current top archetypes from tournament results (share of the field and event wins), the banned/restricted rules, and full 50-card decklists with an automatic legality check. Each deck shows its source and date.
- **Card Database:** searchable cards with stats and art, filterable by color, type, and set (booster packs, starter decks, extra booster, promotional).
- **My Collection:** card art tiles with + and - buttons, filter and sort, and a quick "add a card" search.
- **Deck Import:** paste a decklist (IDs or names, `// Main Deck` / `// Resource Deck` headers supported). It shows card art, flags unknown cards, and checks the deck against the ban list and deck rules.
- **Match Log:** win/loss with opponent colors, notable units, mulligan, username, and your deck. Entries can be edited, and you get win rates by opponent color and by deck.
- **New Sets & Backup:** paste a new set's card table when a set releases, add single cards, and download or restore a backup of everything you've entered.

## Hosting on GitHub Pages

1. Create a repository and upload `index.html` and `README.md` (Add file > Upload files).
2. Go to **Settings > Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
3. GitHub gives you a link like `https://yourname.github.io/repo-name/` within a minute or two.

Keep the file named `index.html`. Private repositories need a paid GitHub plan to use Pages.

## How data is stored

This build saves to your browser's `localStorage`:

- Your collection, saved decks, match log, and added cards stay in that browser on that device. Nothing is sent to a server, and there are no accounts.
- Clearing browsing data, switching browsers, or switching devices loses the data. Use **Backup** in the New Sets & Backup tab to move it or keep a copy.

## Card coverage

- **Full data (with effect text):** GD01, GD02, ST01-ST06, Beta, promos.
- **Stats only (no effect text):** ST11-ST14 and GD05.
- **Mostly missing:** GD03, GD04, ST07-ST10, EB01, and GD06 (Stardust Trails, releases Oct 30, 2026). Add them from the New Sets & Backup tab by pasting a card table.
- Cards not in the database still show art when imported by ID, and are marked "NOT IN DB".

## Rules and legality

The legality checker uses the official banned/restricted list as of **Sept 25, 2026**: Anksha banned, Corsica Base limited to 2, Amuro Ray + Mikazuki Augus and Guntank + M1 Astray Shrike banned together, at most one of a group of low-cost vanilla Units, 4 copies per card number, 50-card main deck, 10-card resource deck, and 2 colors maximum. The vanilla Unit group was copied from a summary and may be incomplete. **Always confirm on [gundam-gcg.com](https://www.gundam-gcg.com) before registering a deck.**

## Sources

- Meta ranking and decklists: [ExBurst](https://exburst.dev/gundam/tournaments/meta), a fan-run tournament tracker (200 events, 1,905 decklists, Jul 22 - Oct 20, 2026).
- Early card data: [apitcg/gundam-tcg-data](https://github.com/apitcg/gundam-tcg-data); ST11-ST14 and GD05 stats from public card-list sites.
- Rules and ban list: [gundam-gcg.com](https://www.gundam-gcg.com).

## Disclaimer

Unofficial fan-made tool. Gundam Card Game names, card text, and imagery belong to SOTSU, SUNRISE, and Bandai. Not affiliated with or endorsed by Bandai.
