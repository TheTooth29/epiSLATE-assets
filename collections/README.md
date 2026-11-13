# epiSLATE collection artwork

Production artwork uses **WebP**, 1920 × 1080 pixels, quality 90. These are compressed conversions of the exact PNG masters, without cropping, redrawing, or changing title placement. All 30 outputs decode successfully and were checked against a matching master contact sheet.

## Repository organization

- `collections/genres/cover/<slug>.webp`: 18 genre covers, including Music for completeness.
- `collections/decades/cover/<decade>.webp`: eight decade covers.
- `collections/discover/cover/<slug>.webp`: four approved Discover covers, including New Releases with actors and actresses on the red carpet.
- `archive/masters/2026-11-13/<category>/<slug>.png`: byte-for-byte full-size masters used for these conversions.
- `archive/previous-delivery/2026-11-13/`: earlier small WebP covers replaced in this publication.
- `collections/artwork-manifest.json`: source paths, master archive paths, original and delivery checksums, sizes, dimensions, and compression settings.

## Local profile files

The project delivery folder also includes `collections-original.json` (the unchanged app export), `collections-profile-1-optimized.json` (the updated import file), and `url-changes.json` (the exact before/after URL list). Only 29 cover URLs changed; all collection IDs, order, sources, settings, and catalogs are preserved. The other 11 covers already use WebP. These personal profile files are delivered locally; they are not published to GitHub.

## Naming and versioning

Use lowercase descriptive slugs separated by hyphens, existing `scifi` spelling for compatibility, and decade names such as `1950s`. Master archives are dated; serving paths remain stable. The JSON uses a short content checksum in the query string so a revised image is not confused with an older cached copy. Future replacements should update that checksum in the JSON.

Legacy PNG and JPEG serving paths are retained for compatibility with older exports. The optimized profile uses only WebP cover paths. PNG master files retain original quality for future editing. Existing titleless Discover originals remain in the local project under `output/discover/titleless/`.

## Quality and transfer checks

30 optimized covers total 9,062,244 bytes versus 140,909,580 bytes for the source PNGs: **93.6% less image data**. This is a byte reduction, not a measured loading-time improvement on the TV. Each output is 1920 × 1080. All source downloads were verified against their Git blob checksums before conversion; every upload must match its recorded delivery checksum.

Import the updated profile JSON once to use the optimized URLs. No Android build is needed or dispatched.
