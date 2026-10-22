# Changelog

Keep this file in the repo. Commit after every update so GitHub's history lets you go back to any earlier version.

## Latest
- Added GD03, EB01, ST07-ST10 and GD06 (pre-release) with full effect text from TCGCSV files. Added credits to the app footer and a SOURCES.md file.
- Added all Phantom Aria (GD04) cards (stats only). Card list now loads 60 at a time with a Show more button, which fixes scroll lag.
- Removed the game counts from the Match Log and New Sets & Backup tabs.
- Fixed the 2-color rule wrongly flagging two-color decks (some cards stored colors as "white" instead of "White", and "-" counted as a color). The color filter now includes those cards too.
- Meta Report now uses ExBurst tournament data (Jul 22 - Oct 20, 2026) with one verified Aile Strike + Strike Freedom list.
- Collection shows art tiles with + / - controls, filtering, sorting, and quick add.
- Card Database can be filtered by set; new sets can be pasted in under New Sets & Backup.
- Match Log entries can be edited; added a deck dropdown, mulligan, and opponent username.
- Legality checker follows the Sept 25, 2026 ban list.
- Renamed the app to Hangar.

## Must keep working (check these after every update)
1. Collection, saved decks, match log, and added cards survive a page reload.
2. Backup > Download / Show as text > Restore works.
3. Deck Import handles `// Main Deck` headers, `4x ID` lines, and flags unknown cards.
4. Legality check flags banned cards, banned pairs, and the vanilla-unit group, but not legal two-color decks.
5. Card Database set, color, type, and search filters all work together.
