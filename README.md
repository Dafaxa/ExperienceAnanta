# Ananta Property Experience — prototype

A clickable prototype of the Ananta interactive 3D walkthrough, sales console, CMS and analytics. `index.html` is the Platform Hub, which links to every app.

It's a static site, so there's no build step. Deploy the repository root as-is (Vercel, Netlify, Cloudflare Pages or GitHub Pages), or run it locally:

```sh
npx serve .
```

Always open the pages through a server. Opening a file by double-clicking it breaks the page imports.

- React is served from `vendor/` (same files and integrity hashes as unpkg), so the pages run without a CDN; unpkg.com is only a fallback. Fonts still come from Google Fonts.
- Prices, promos and the headline published from the CMS are stored in the browser. Use **Reset demo data** in the Hub footer before each client meeting.
- Sync between the sales console, the CMS and the customer screen only works between tabs in the same browser.
- Keep `support.js`, `image-slot.js`, `deck-stage.js`, `CMSSidebar.dc.html`, `vendor/` and `img/`. The pages depend on them.
- `src/` and `uploads/` hold the original renders. No page uses them directly.
- `design-handoff/` holds the Claude Design export notes and chat transcript.
