# Changelog

## 0.2.0 — 2026-11-15

- Tree and Area modes replaced by one: every tap reads a circle and reports the tallest tree in it, the tree you tapped (highest point within 3 m), the five tallest tops, cover over 2 m and its mean height.
- Circle radius up to 100 m (about 3 ha, at most about 3 MB a tap), was 50 m.
- New Ground view (Aerial | Ground, top right): no photo and no trees, just the bare earth from the LiDAR ground model at 1 m, hillshaded from the north-west with ×2 vertical exaggeration, over Esri's world hillshade outside the circle.
- Heights image drawn about 100× faster (corners projected, the rest interpolated), so big circles stay quick on a phone.
- The map now moves to fit the whole circle above the results panel.
- Tree-top labels that would overlap are left off (dot only) until you zoom in.
- Zoom buttons moved to bottom right.

## 0.1.0 — 2026-11-15

- First version, split out of inferrd's LiDAR tab as a phone app.
- Tree mode: tap a crown, get the highest point within 3 m, plus nearby tree tops labelled on the map.
- Area mode: circle of 10–50 m radius with tallest tree, five tallest tops, cover over 2 m and its mean height.
- Where I am: GPS position, tallest tree within the GPS accuracy.
- Reads only the LiDAR blocks under the spot (~0.7–0.8 MB a tap), keeps them for later taps nearby; survey found from the tile name, no tile lists downloaded.
- Heights drawn in viridis over the imagery, resampled to lon/lat so the 1 m cells line up.
- Older surveys covering the spot can be picked from buttons under the result.
- Installable to a phone home screen (manifest and icons).
