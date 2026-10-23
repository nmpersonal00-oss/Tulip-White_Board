# Tulip Board v5.5 — tested focus drawing mode

This update replaces v5.4. It fixes a JavaScript error left behind when the bottom instruction strip was removed, and makes drawing mode persist until the user taps the small flower restore button or presses Escape.

## Changes
- Completely removed the bottom instruction strip (including stale references in code).
- Removed the extra top Hide button.
- The left-side **Hide** control hides the top and left toolbars together.
- While hidden, the board still accepts drawing strokes; drawing never unhides the toolbars.
- A tiny flower button in the top-left restores all controls.
- If Select or Sticker was active, Hide switches to the pen so drawing works immediately.
- Updated the offline service worker cache version to `tulip-board-offline-v5-5`.

## Update existing GitHub Pages installation
1. Export a Backup of your current editable project from the previous app.
2. Extract this ZIP on your computer or iPad.
3. Upload the extracted `index.html`, `sw.js`, `manifest.webmanifest`, and `icons/` contents into the ROOT of your existing GitHub Pages repository, replacing the older files. Do not upload only the ZIP.
4. Wait for GitHub Pages to deploy. Visit the site in Safari while online, then close and reopen the Home Screen app.
5. Open Help and confirm it says **Tulip Board v5.5**.

If the old app is still cached, close it completely and open the published GitHub Pages site in a fresh Safari private tab to confirm the website has updated. The app saves drawings in the browser/device, not to GitHub; don't erase website data without an editable Backup.

## Browser testing
Tested on Chromium desktop and on an iPad-sized touchscreen emulation, verifying the toolbar is hidden during drawing, a stroke is added, the toolbar remains hidden, and restore works. Apple Pencil hardware was not available for testing.
