# Search Catalog System

## Components
- Main UI search field in `index.html`.
- BOM data source from `bom-index.js` as `window.BOM_INDEX`.
- Result viewer links to `pdf-highlight-viewer.html` with query params.

## Search modes
1. Motor/table mode:
   - Filters visible rows by motor type/code/serial text.
2. BOM mode:
   - Detects part-number-like input.
   - Falls back to description token scoring.

## Data flow
- User types query.
- UI normalizes text and part format.
- Matching entries are rendered in result panel.
- Clicking a result opens PDF viewer at page + highlighted term.

## Maintenance
- Regenerate/update `bom-index.js` when catalog PDFs or BOM entries change.
- Keep filenames/paths in `downloads/` stable to avoid broken links.
