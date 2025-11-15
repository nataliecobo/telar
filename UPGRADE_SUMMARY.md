---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 0.4.2-beta
- **To:** 0.4.3-beta
- **Date:** 2025-11-15
- **Automated changes:** 4
- **Manual steps:** 6

## Automated Changes Applied

### Other (4 files)

- [x] success
- [x] changes
- [x] warnings
- [x] errors

## Manual Steps Required

Please complete these after merging:

1. After upgrade completes:
2. 1. Regenerate IIIF tiles to apply EXIF orientation fix:
3.    - If using GitHub Pages: Push this commit to trigger rebuild
4.    - If testing locally: Run `python3 scripts/generate_iiif.py`
5. 2. Portrait photos from phones/cameras will now display correctly
6. 3. iPad users can now navigate stories with swipe gestures

## Resources

- [Full Documentation](https://ampl.clair.ucsb.edu/telar-docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
