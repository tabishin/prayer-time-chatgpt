# Home Tablet Redesign — v1

## Selected direction
- Android tablet, landscape-first with a portrait fallback.
- Emerald green and warm gold visual theme (`emerald-gold`).
- Five prayer cards have equal visual weight; no prayer is singled out.
- Gregorian and Hijri dates remain visible together.
- Existing Hadith panel retained and restyled.
- Automatic in-app night dimming defaults to 22:00–06:00.

## Files changed
- `index.html`: semantic tablet header; existing JavaScript IDs preserved.
- `styles.css`: appended tablet-first emerald/gold design layer and responsive portrait/mobile rules.
- `script.js`: added automatic night-dim state to the existing live-clock tick.
- `settings.json`: defaults to emerald/gold and enables night dimming.
- Android WebView copies under `android-kiosk/app/src/main/assets/` are synchronized.

## Night dim behaviour
Night dimming affects only the app display using a CSS brightness filter. It does not change Android system brightness and does not change audio or alarm scheduling. Defaults are 22:00 to 06:00; `nightDimEnabled`, `nightDimStart`, and `nightDimEnd` are read from the settings object if supplied.

## Validation status
This is a source-level implementation. It has not been run on a physical tablet or built into a release APK. Validate layout on the target tablet, especially both orientations, and test audio/alarm behaviour separately.
