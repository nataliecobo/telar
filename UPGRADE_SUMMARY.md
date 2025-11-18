---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 0.4.3-beta
- **To:** 0.5.0-beta
- **Date:** 2025-11-18
- **Automated changes:** 36
- **Manual steps:** 6

## Automated Changes Applied

### Configuration (1 file)

- [x] Updated _config.yml: version 0.5.0-beta (2025-11-18)

### Layouts (3 files)

- [x] Updated _layouts/story.html: Embed mode support, share button
- [x] Updated _layouts/index.html: Share button in navbar
- [x] Updated _layouts/default.html: Share panel modal

### Includes (4 files)

- [x] Updated _includes/share-button.html: Share button component
- [x] Updated _includes/share-panel.html: Share/embed modal
- [x] Updated _includes/header.html: Navbar share button
- [x] Updated _includes/panels.html: Mobile image width fix

### Styles (1 file)

- [x] Updated assets/css/telar.scss: Embed mode, share UI, carousel, mobile fixes

### Scripts (7 files)

- [x] Removed unused file: assets/js/scrollama.min.js
- [x] Removed unused file: assets/js/openseadragon.min.js
- [x] Updated scripts/csv_to_json.py: CSV-driven processing, flattened paths
- [x] Updated scripts/generate_iiif.py: Extended format support, case-insensitive
- [x] Updated assets/js/embed.js: Embed mode detection and banner
- [x] Updated assets/js/share-panel.js: Share/embed functionality
- [x] Updated assets/js/story.js: Embed navigation, panel fixes

### Documentation (7 files)

- [x] Removed deprecated directory: docs/google_sheets_integration
- [x] Updated README.md: v0.5.0 documentation
- [x] Updated components/README.md: Updated directory structure
- [x] Updated components/images/README.md: Flattened structure documentation
- [x] Updated components/pdfs/README.md: Future v0.6.0 placeholder
- [x] Updated components/audio/README.md: Future v0.7.0 placeholder
- [x] Updated components/3d-models/README.md: Future v0.8.0 placeholder

### Other (13 files)

- [x] Discovered 0 CSV-referenced images
- [x] Found 0 image references in .md files
- [x] Removed empty directory: components/images/objects
- [x] Removed empty directory: components/images/additional
- [x] Migrated 8 images to flat structure
- [x] No image path updates needed
- [x] Updated objects.csv: Renamed 'iiif_manifest' column to 'source_url'
- [x] Created directory: components/pdfs
- [x] Created directory: components/audio
- [x] Created directory: components/3d-models
- [x] Updated _data/languages/en.yml: Share/embed strings, updated error messages
- [x] Updated _data/languages/es.yml: Spanish translations
- [x] Updated CHANGELOG.md: v0.5.0 changelog

## Manual Steps Required

Please complete these after merging:

1. ⚠️ **CRITICAL: Update Your GitHub Actions Workflows** ⚠️

**Without this step, images will NOT display on your published site.**

The upgrade changed where images are stored, but your GitHub Actions workflows still point to the old location. You must update two files: `build.yml` and `upgrade.yml`.

---

**Option 1: Using the GitHub Website**

1. Go to the Telar repository workflows: https://github.com/UCSB-AMPLab/telar/tree/main/.github/workflows
2. Click on `build.yml`, then click the "Raw" button, and copy all the text
3. In **your** repository on GitHub, go to `.github/workflows/build.yml`
4. Click the pencil icon (✏️) to edit, delete everything, and paste the new content
5. Click "Commit changes" at the bottom
6. Repeat steps 2-5 for `upgrade.yml`

---

**Option 2: Using the Command Line** (if you've been syncing your repository to your machine and are comfortable with git)

Run these commands in your repository:

```bash
# Download the updated workflows
curl -o .github/workflows/build.yml https://raw.githubusercontent.com/UCSB-AMPLab/telar/main/.github/workflows/build.yml
curl -o .github/workflows/upgrade.yml https://raw.githubusercontent.com/UCSB-AMPLab/telar/main/.github/workflows/upgrade.yml

# Commit the changes
git add .github/workflows/
git commit -m "Update workflows for v0.5.0 image structure"
git push
```

**That's it!** Your next build will use the correct image locations. ([guide](https://github.com/UCSB-AMPLab/telar/tree/main/.github/workflows))
2. Regenerate IIIF tiles to ensure images work with new structure: python3 scripts/generate_iiif.py
3. Test your site build: bundle exec jekyll build
4. Test embed mode: Add ?embed=true to any story URL to see the embed mode UI with navigation banner
5. Explore new share/embed UI: Click the share button (icon with arrow) on stories or homepage to access share links and embed code
6. Optional: Install pillow-heif for HEIC/HEIF support (iPhone photos). Run: pip install pillow-heif. The framework gracefully degrades if not installed, converting HEIC to standard formats.

## Resources

- [Full Documentation](https://ampl.clair.ucsb.edu/telar-docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
