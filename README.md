# howtall

Tap a tree in New Zealand and get its height from LINZ LiDAR. Built for a phone.

- **Tap**: reads a circle round the spot (slider, 10–100 m radius): tallest tree, the tree you tapped (highest cell within 3 m), five tallest tops, cover over 2 m and its mean height.
- **Where I am**: the same circle round your GPS position, widened to at least the GPS accuracy.
- **Aerial | Ground**: heights coloured over the photo, or the bare-earth hillshade from the LiDAR ground model with no photo or trees.

Height = DSM − DEM from the same LINZ survey, 1 m grid, power lines and pylons left out (same test as inferrd's LiDAR tab). Newest survey first; older surveys covering the spot are buttons under the result.

## Data use

Nothing is read until you tap. The 1:10k sheet tile under the point is worked out from its NZTM coordinates (no survey tile lists are downloaded), a HEAD request per nearby survey says which surveys have it, and only the COG's own 512 × 512 m blocks under the circle are read: about 0.75 MB a tap for a small circle, about 2.5 MB for a 200 m circle, more where it straddles block edges. Blocks are kept, so later taps in the same block download nothing. LINZ's catalogue (~65 KB) is cached for a week.

## Running

Single static `index.html`, no build step. Serve the folder (`python -m http.server`) and open it. Deploys as-is to GitHub Pages.

## Sources

LiDAR: 1 m surface and ground models from [nz-elevation](https://registry.opendata.aws/nz-elevation/), published by Toitū Te Whenua LINZ, CC BY 4.0. Each survey has its own licensor (often a regional council or a councils' group, such as BOPLASS or Environment Canterbury); howtall reads it from the end of the survey's collection.json (the last 8 KB, once per survey) and credits it on the map and under the result. Maps: Esri World Imagery and World Hillshade; OpenTopoMap (CC-BY-SA).

## Licence

Code: [PolyForm Strict 1.0.0](LICENSE) — free to use for non-commercial purposes; redistributing or modifying it is not permitted. Written content and original images: [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/). Third-party data, map tiles and libraries keep their own licences. For commercial use, contact Rutherford Ecology.
