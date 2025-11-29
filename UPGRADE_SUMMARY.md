---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 0.6.0-beta
- **To:** 0.6.1-beta
- **Date:** 2025-11-29
- **Automated changes:** 5
- **Manual steps:** 2

## Automated Changes Applied

### Configuration (1 file)

- [x] Updated _config.yml: version 0.6.1-beta (2025-11-29)

### Scripts (2 files)

- [x] Updated scripts/generate_iiif.py - IIIF generation script (EXIF orientation fix)
- [x] Updated scripts/migrations/v050_to_v060.py - v0.5.0→v0.6.0 migration script (template pollution fix)

### Documentation (1 file)

- [x] Updated README.md - README (bilingual version)

### Other (1 file)

- [x] Updated CHANGELOG.md - CHANGELOG (v0.6.1 release notes)

## Manual Steps Required

Please complete these after merging:

1. **If you use GitHub Pages:**

No further actions needed. GitHub Actions will automatically regenerate IIIF tiles with the EXIF orientation fix when your site rebuilds.
2. **If you work with your site locally:**

If you have self-hosted images with EXIF orientation metadata (most smartphone photos taken in portrait mode), regenerate IIIF tiles to fix thumbnail orientation:

`python3 scripts/generate_iiif.py --base-url YOUR_SITE_URL`

(Replace YOUR_SITE_URL with your site's URL)

You will see "Saving rotated image for IIIF processing" in the console output for affected images.

## Resources

- [Full Documentation](https://telar.org/docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
