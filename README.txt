GROUNDWORKS CALCULATOR — PWA STARTER
=====================================

Contents
- index.html: calculator UI and logic
- manifest.json: installable app metadata
- sw.js: service worker for offline caching
- icon.svg, icon-192.png, icon-512.png: app icons

Features
- Volume and estimated tonnes
- Material catalogue with editable densities
- Custom materials
- Saved calculation history in browser local storage
- Export/import JSON backup
- Decimal point and comma input support
- Copy calculation summary

IMPORTANT LIMITS
- Density values are example estimates; verify with your supplier.
- Data is stored locally in the browser on this device. Clearing browser/site data can remove it.
- Export a backup regularly. This first version does not sync data between devices.
- For dependable offline use, host on HTTPS, open it once while online, and allow the service worker to finish caching.
- A PWA cannot be installed reliably by opening index.html directly from a file manager. It must be served from HTTPS (or localhost during development).

EASY HOSTING OPTION: GITHUB PAGES
1. Sign in to GitHub and create a new public repository, e.g. groundworks-calculator.
2. Upload all four files from this folder to the repository root (index.html, manifest.json, sw.js, icon.svg).
3. In repository Settings > Pages, enable deployment from the main branch and root folder.
4. Wait for GitHub Pages to publish the site. Open the HTTPS address on your Samsung in Chrome.
5. While online, open the app and wait a few seconds.
6. In Chrome menu (three dots), tap "Install app" or "Add to Home screen" (wording can vary).
7. Launch the installed app once, then test Airplane mode. If it opens and calculates, offline caching is working.

UPDATING
When files change, increase CACHE_NAME in sw.js (e.g. v1 to v2), upload the updated files, then open the app online once to update the cache.

This package is a starter PWA, not a Play Store APK.
