---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 0.5.0-beta
- **To:** 0.6.0-beta
- **Date:** 2025-11-29
- **Automated changes:** 66
- **Manual steps:** 3

## Automated Changes Applied

### Configuration (2 files)

- [x] Updated _data/navigation.yml: Bilingual navigation menu configuration (NEW)
- [x] Updated _config.yml: version 0.6.0-beta (2025-11-29)

### Layouts (6 files)

- [x] Updated _layouts/story.html: Credit prefix exposure, byline markdown support
- [x] Updated _layouts/default.html: Multilingual support
- [x] Updated _layouts/user-page.html: Custom pages layout (NEW)
- [x] Updated _layouts/objects-index.html: Object ordering bug fix
- [x] Updated _layouts/index.html: Logo display removed
- [x] Updated _layouts/glossary.html: Demo badge text fix

### Includes (2 files)

- [x] Updated _includes/header.html: Data-driven navigation, logo CSS
- [x] Updated _includes/viewer.html: Object credits badge HTML/CSS

### Styles (1 file)

- [x] Updated assets/css/telar.scss: Logo, panel freeze, tab widget, glossary, credits badge

### Scripts (8 files)

- [x] Updated scripts/csv_to_json.py: Demo content processing, bilingual CSV support, story_id
- [x] Updated scripts/fetch_demo_content.py: Demo content bundle fetcher (NEW)
- [x] Updated scripts/generate_collections.py: Custom pages support, demo glossary
- [x] Updated scripts/fetch_google_sheets.py: Bilingual tab support, story_id support
- [x] Updated scripts/discover_sheet_gids.py: Story_id support
- [x] Updated scripts/generate_iiif.py: Version header update
- [x] Updated assets/js/story.js: Panel freeze system, credits badge, viewer scroll isolation
- [x] Updated assets/js/telar.js: Glossary link handling, click-outside-to-close

### Documentation (1 file)

- [x] Updated README.md: v0.6.0 documentation

### Other (46 files)

- [x] Created directory: components/texts/pages/
- [x] Created directory: components/texts/stories/your-story/
- [x] Created directory: components/texts/stories/tu-historia/
- [x] Moved pages/about.md → components/texts/pages/about.md
- [x] Added generated JSON patterns to .gitignore
- [x] Added _jekyll-files/ to .gitignore
- [x] Added demo glossary pattern to .gitignore
- [x] Removed _jekyll-files/ from git tracking
- [x] Removed 5 generated file(s) from git tracking
- [x] Removed v0.5.0 example file: components/images/ampl-logo.png
- [x] ℹ️  Kept 2 v0.5.0 example files (still referenced in Google Sheet)
- [x]   • components/structures/story-1.csv
- [x]   • components/structures/story-2.csv
- [x] ✓ Removed 1 v0.5.0 example files (not in use)
- [x] ℹ️  Your custom content is preserved
- [x] Updated _data/languages/en.yml: Credit prefix, updated strings
- [x] Updated _data/languages/es.yml: Spanish translations, credit prefix
- [x] Updated CHANGELOG.md: v0.6.0 changelog
- [x] Updated .gitignore: Generated files gitignored
- [x] Updated components/texts/stories/your-story/about-coordinates.md: Coordinate system explanation
- [x] Updated components/texts/stories/your-story/guiding-attention.md: Question/Answer/Invitation pattern
- [x] Updated components/texts/stories/your-story/building-argument.md: Coordinate sequences as argument
- [x] Updated components/texts/stories/your-story/visual-rhetoric.md: Visual contrast analysis
- [x] Updated components/texts/stories/your-story/the-reveal.md: Full view synthesis
- [x] Updated components/texts/stories/your-story/progressive-disclosure.md: Layer 2 panel explanation
- [x] Updated components/texts/stories/your-story/ruler-place.md: Charles III marginalized position
- [x] Updated components/texts/stories/your-story/multiple-images.md: IIIF vs self-hosted comparison
- [x] Updated components/texts/stories/your-story/whats-next.md: Template overview
- [x] Updated components/texts/stories/tu-historia/acerca-de-coordenadas.md: Sistema de coordenadas
- [x] Updated components/texts/stories/tu-historia/guiar-atencion.md: Patrón Pregunta/Respuesta/Invitación
- [x] Updated components/texts/stories/tu-historia/construir-argumento.md: Secuencias como argumento
- [x] Updated components/texts/stories/tu-historia/retorica-visual.md: Análisis de contraste visual
- [x] Updated components/texts/stories/tu-historia/la-revelacion.md: Síntesis de vista completa
- [x] ⚠️  Warning: Could not fetch components/texts/stories/tu-historia/divulgacion-progresiva.md from GitHub
- [x] Updated components/texts/stories/tu-historia/lugar-gobernante.md: Posición marginalizada
- [x] Updated components/texts/stories/tu-historia/multiples-imagenes.md: Comparación IIIF vs autoalojadas
- [x] Updated components/texts/stories/tu-historia/que-sigue.md: Resumen de plantilla
- [x] Updated components/texts/glossary/story.md: Story glossary entry
- [x] Updated components/texts/glossary/step.md: Step glossary entry
- [x] Updated components/texts/glossary/viewer.md: Viewer glossary entry
- [x] Updated components/texts/glossary/panel.md: Panel glossary entry
- [x] Updated components/texts/glossary/historia.md: Historia glossary entry
- [x] Updated components/texts/glossary/paso.md: Paso glossary entry
- [x] Updated components/texts/glossary/visor.md: Visor glossary entry
- [x] Updated components/texts/glossary/panel-es.md: Panel-es glossary entry
- [x] ⚠️  Warning: Could not fetch components/images/leviathan.jpg from GitHub

## Manual Steps Required

Please complete these after merging:

1. **If you use GitHub Pages:**

No further actions needed. GitHub Actions will automatically rebuild your site with the upgraded framework.
2. **If you work with your site locally:**

1. Regenerate data files: `python3 scripts/csv_to_json.py && python3 scripts/generate_collections.py`
2. Test your site build: `bundle exec jekyll build`
3. **Optional (all users):**

Enable demo content by setting `include_demo_content: true` in `_config.yml` under `story_interface`. Demo content will be automatically fetched during the build process.

## Resources

- [Full Documentation](https://telar.org/docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
