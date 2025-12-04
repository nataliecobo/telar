---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 0.6.1-beta
- **To:** 0.6.2-beta
- **Date:** 2025-12-04
- **Automated changes:** 18
- **Manual steps:** 2

## Automated Changes Applied

### Configuration (3 files)

- [x] Renamed config section: testing-features → development-features
- [x] Updated _layouts/story.html - Story layout (viewer preloading config)
- [x] Updated _config.yml: version 0.6.2-beta (2025-12-04)

### Layouts (2 files)

- [x] Updated _layouts/index.html - Index layout (hover prefetch, hide flags)
- [x] Updated _layouts/objects-index.html - Objects index (hide_collections flag)

### Includes (3 files)

- [x] Updated _includes/viewer.html - Viewer include (removed inline transition styles)
- [x] Updated _includes/header.html - Header (hide_collections nav flag)
- [x] Updated _includes/panels.html - Panels (h5→h1 semantic fix)

### Styles (1 file)

- [x] Updated assets/css/telar.scss - Stylesheet (image overflow, h1 spacing, fade transitions)

### Scripts (5 files)

- [x] Updated assets/js/story.js - Story JS (viewer preloading overhaul)
- [x] Updated assets/js/telar.js - Telar JS (glossary-to-glossary linking)
- [x] Updated scripts/csv_to_json.py - CSV converter (case-insensitive matching)
- [x] Updated scripts/generate_collections.py - Collections generator (glossary links, hide flags)
- [x] Updated scripts/build_local_site.py - NEW: All-in-one local build script

### Documentation (1 file)

- [x] Updated README.md - README (version update)

### Other (3 files)

- [x] Updated CHANGELOG.md - CHANGELOG (v0.6.2 release notes)
- [x] Removed deprecated: components/texts/glossary/iiif-manifest.md
- [x] Removed deprecated: components/texts/glossary/markdown.md

## Manual Steps Required

Please complete these after merging:

1. **If you use GitHub Pages:**

No further actions needed. Your site will automatically use the improved viewer preloading when it rebuilds.
2. **If you work with your site locally:**

A new all-in-one build script is now available:

`python3 scripts/build_local_site.py`

This runs all build steps (CSV conversion, collections, IIIF, Jekyll) with a single command. Use `--skip-iiif` for faster rebuilds when images haven't changed.

## Resources

- [Full Documentation](https://telar.org/docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
