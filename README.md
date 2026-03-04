# Part Catalog (Honda) - GitHub Pages

Static catalog website with:
- Category tables (Cub, Matic, Sport)
- Client-side search/filter
- BOM index lookup (part number + description)
- PDF highlight viewer for parts references

## Copyright / License
This repository is **not open source**.
See `WARNING.txt` for all-rights-reserved notice.

## Repository Structure
- `index.html` - Main catalog app
- `bom-index.js` - Search index for part/BOM lookup
- `pdf-highlight-viewer.html` - Viewer used by search results
- `downloads/` - PDF catalog assets by category
  - `downloads/cub/`
  - `downloads/matic/`
  - `downloads/sport/`
- `docs/` - Operational docs

## GitHub Pages Deployment
Use either method:
1. Branch deploy: `main` + `/(root)` in Pages settings.
2. Or GitHub Actions (custom) if you want CI-based deploy.

The published URL is typically:
`https://<username>.github.io/<repo>/`

## Search Catalog System
Search runs fully client-side in browser:
- Motor table filtering by keyword
- BOM part lookup from `window.BOM_INDEX.parts`
- PDF viewer deep-link generation per match

See `docs/SEARCH_SYSTEM.md` for implementation notes.

## Important Security Note
`.gitignore` helps prevent future accidental commits,
but it does **not** protect files already committed or already public.
For sensitive/private data:
- Keep repository private, or
- Remove sensitive history before publishing.
