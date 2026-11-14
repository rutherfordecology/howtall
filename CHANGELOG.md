# Changelog

## 0.1.0 — 2026-11-15

- First version, split out of inferrd's LiDAR tab as a phone app.
- Tree mode: tap a crown, get the highest point within 3 m, plus nearby tree tops labelled on the map.
- Area mode: circle of 10–50 m radius with tallest tree, five tallest tops, cover over 2 m and its mean height.
- Where I am: GPS position, tallest tree within the GPS accuracy.
- Reads only the LiDAR blocks under the spot (~0.7–0.8 MB a tap), keeps them for later taps nearby; survey found from the tile name, no tile lists downloaded.
- Heights drawn in viridis over the imagery, resampled to lon/lat so the 1 m cells line up.
- Older surveys covering the spot can be picked from buttons under the result.
- Installable to a phone home screen (manifest and icons).
