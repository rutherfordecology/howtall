# Changelog

## 0.8.0 — 2026-11-15

- The LiDAR credit names each survey's own licensor (often a council or a councils' group: BOPLASS for Bay of Plenty, Environment Canterbury for Canterbury), under the result and on the map, as CC BY 4.0 asks. Before, everything was credited to LINZ, which publishes the surveys but often isn't their licensor. howtall reads the licensor from the last 8 KB of the survey's collection.json, once per survey, and remembers it.
- Licence: code under PolyForm Strict 1.0.0, howtall's own words and images under CC BY-NC-ND 4.0 (LICENSE, as in WhatDatBird). Before, the repo had no licence.
- About and README list the sources and licences.

## 0.7.0 — 2026-11-15

- Topo map as a third option beside Aerial and Ground: OpenTopoMap (the same topo layer as occurd.), with the tree heights coloured on top, a little more see-through than on the aerial so the contours and tracks show. It has detail to zoom 17; closer in it's enlarged. The choice is remembered.
- On a phone the Aerial/Ground/Topo buttons sit under the ? button so the header fits the screen.

## 0.6.0 — 2026-11-15

- One dot per tree, not a cluster per crown. Two tops count as separate trees only if the canopy dips between them by at least 2 m, or a quarter of the shorter tree's height (whichever is more), and rises again; tops closer than 2 m are always one tree. A dense 50 m forest circle went from 135 dots to 51.
- The tallest tree is now the tallest real tree top in the circle. Before, it was the circle's highest point, which could be the side of a bigger tree just outside the circle (a Hamilton park showed 42.9 m for a crown flank; now 30.4 m, the tallest top inside).
- The five labelled tops are the five tallest trees, at least 6 m apart.

## 0.5.1 — 2026-11-15

- The menu's inferrd. link goes to its new address, inferrd.rutherfordecology.co.nz.

## 0.5.0 — 2026-11-15

- Every tree top over 5 m in the circle now has a small dot (tops at least 3 m apart, so one broad crown counts once). Tap a dot to see that tree's height; tapping a dot doesn't start a new circle, and the dots have a wide tap area for fingers.

## 0.4.0 — 2026-11-15

- Where I am is now a small target button on the map, above the zoom buttons, instead of a full-width bar.
- Says clearly when the phone's Location (GPS) is off: an error from the phone now says to turn Location on, and if the phone gives no answer at all, a hint appears after 7 seconds (it gives up after 15).
- A tap on the map while waiting for a location cancels the wait.

## 0.3.1 — 2026-11-15

- New address: howtall.rutherfordecology.co.nz (the github.io address redirects).
- Apps menu links Rightree and Soundabouts at their new rutherfordecology.co.nz addresses.

## 0.3.0 — 2026-11-15

- Rutherford Ecology branding: "by Rutherford ecology" under the app name opens a menu with the Rutherford Ecology website and links to the other apps.
- Buy me a coffee link at the bottom of the panel, and in the menu and About.
- Icons from the shared Rutherford Ecology line set (occurd's icons.js), with new tree, mountain, shell and tail icons drawn in the same style.
- Home-screen icon redrawn in the style of the other small apps.

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
