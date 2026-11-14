# howtall

Tap a tree in New Zealand and get its height from LINZ LiDAR. Built for a phone.

- **Tree**: the top of the tree you tapped (highest 1 m cell within 3 m of the tap), the height right at the tap, and the tallest tree tops close by marked on the map.
- **Area**: a circle of 10–50 m radius round the tap (at most ~0.8 ha): tallest tree, five tallest tree tops, cover over 2 m and its mean height.
- **Where I am**: your GPS position; reports the tallest tree within your GPS accuracy (10–50 m).

Height = DSM − DEM from the same LINZ survey, 1 m grid, power lines and pylons left out (same test as inferrd's LiDAR tab). Newest survey first; older surveys covering the spot are buttons under the result.

## Data use

Nothing is read until you tap. The 1:10k sheet tile under the point is worked out from its NZTM coordinates (no survey tile lists are downloaded), a HEAD request per nearby survey says which surveys have it, and only the COG's own 512 × 512 m blocks under the circle are read: about 0.7–0.8 MB a tap for both surfaces. Blocks are kept, so later taps in the same block download nothing. LINZ's catalogue (~65 KB) is cached for a week.

## Running

Single static `index.html`, no build step. Serve the folder (`python -m http.server`) and open it. Deploys as-is to GitHub Pages.

## Sources

LiDAR: Toitū Te Whenua LINZ, [nz-elevation](https://registry.opendata.aws/nz-elevation/), CC BY 4.0. Imagery: Esri World Imagery.
