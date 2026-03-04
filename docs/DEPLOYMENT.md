# GitHub Pages Deployment

## Quick setup
1. Create a public GitHub repository (empty).
2. Push local `main` branch.
3. In GitHub: Settings > Pages.
4. Source: Deploy from a branch.
5. Branch: `main`, Folder: `/(root)`.
6. Wait 1-3 minutes and open published URL.

## Validate after publish
- `index.html` loads successfully.
- `bom-index.js` loads (no 404 in browser console).
- `pdf-highlight-viewer.html` opens from search results.
- PDFs open from `downloads/...` links.
