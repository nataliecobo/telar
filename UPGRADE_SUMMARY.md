---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 0.4.1-beta
- **To:** 0.4.2-beta
- **Date:** 2025-11-11
- **Automated changes:** 4
- **Manual steps:** 2

## Automated Changes Applied

### Layouts (1 file)

- [x] Updated _layouts/index.html: Updated index layout (site description link styling)

### Styles (1 file)

- [x] Updated assets/css/telar.scss: Updated CSS (mobile navbar, font sizes, title wrapping)

### Documentation (1 file)

- [x] Updated README.md: Updated README (version 0.4.2-beta)

### Other (1 file)

- [x] Updated .github/workflows/build.yml: Updated build workflow (smart IIIF detection with caching)

## Manual Steps Required

Please complete these after merging:

1. CRITICAL: The updated build.yml workflow must be merged/committed for IIIF caching to work. If using automated upgrade workflow: Review and MERGE the upgrade pull request - the new build workflow will not take effect until merged. If upgrading locally: COMMIT and PUSH .github/workflows/build.yml - the new workflow is not active until pushed to GitHub. Until the new workflow is active, the IIIF caching protection is not in effect.
2. Test the smart IIIF detection: Make a content-only change (edit a story markdown file), push to GitHub, and verify the build workflow completes faster by skipping IIIF regeneration (optional)

## Resources

- [Full Documentation](https://ampl.clair.ucsb.edu/telar-docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
