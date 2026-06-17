# SafeBite allergen database

`allergens.json` is the over-the-air allergen dictionary SafeBite checks on launch.
The app bundles a copy of this file and downloads this hosted copy when its
`version` is strictly newer (numeric `YYYY.MM[.patch]` compare), swapping it in
atomically. The app stays fully functional offline on its last-good copy.

## How to update (same-day fix, no App Store release)
1. Edit `allergens.json`: add/adjust the alias under the right canonical allergen.
2. Bump `version` (e.g. `2026.07` -> `2026.07.1` for a patch, `2026.08` for a month).
3. Commit + push. GitHub Pages serves it within ~1 minute.
4. Installed apps pick it up on their next launch over Wi-Fi.
5. Periodically fold the same change into the app's bundled `allergens.json` so
   fresh installs get it offline too, and ship with the next binary.

## Sources
US FDA (FALCPA + FASTER Act), EU/UK FIC Annex II, Health Canada priority allergens;
derivative/hidden names from FARE and FARRP references. Screening aid only, not
clinically certified; cross-contact is often unprinted and undetectable.

## History
- 2026.07 — first sourced build: 16 canonical allergens, 406 alias terms,
  16 precautionary phrases. US 9 + EU/UK 14 + Health Canada + Coconot(US optional).
