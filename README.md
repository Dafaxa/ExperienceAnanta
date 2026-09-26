# Ananta Property Experience — prototype

A clickable prototype of the Ananta interactive 3D walkthrough, sales console, CMS and analytics. `index.html` is the Platform Hub, which links to every app.

It's a static site, so there's no build step. Deploy the repository root as-is (Vercel, Netlify, Cloudflare Pages or GitHub Pages), or run it locally:

```sh
npx serve .
```

Always open the pages through a server. Opening a file by double-clicking it breaks the page imports.

- The `.dc.html` pages load React from unpkg.com, so they need internet access. Fonts come from Google Fonts.
- Sync between the sales console, the CMS and the customer screen only works between tabs in the same browser.
- Keep `support.js`, `image-slot.js`, `deck-stage.js`, `CMSSidebar.dc.html` and `img/`. The pages depend on them.
- `src/` and `uploads/` hold the original renders. No page uses them directly.
- `design-handoff/` holds the Claude Design export notes and chat transcript.
