# Home Sweet Home — private, iPhone-friendly home organizer

A small progressive web app (PWA) built with plain HTML, CSS, and JavaScript. No npm, API keys, subscription, or database required.

## What's included
- Today's automatically selected cleaning checklist, keyed to the local date
- Weekly routine and three laundry loads, keyed to the Monday of each week
- Four room-recovery projects with lasting checkmarks
- Monthly maintenance checklist, editable seven-day dinner plan, grocery notes
- Add a custom recurring task to a day of the week
- JSON backup export/import
- Mobile layout, app icon, and offline cache after first successful online load

## Quick preview on a computer
1. Extract the ZIP.
2. In a terminal, enter the `home-sweet-home` folder.
3. Run `python3 -m http.server 8000`.
4. Open `http://localhost:8000` in a browser.

## Put it on your iPhone Home Screen (free hosting with GitHub Pages)
1. Create a free GitHub account if needed, then create a **new repository** named `home-sweet-home`.
2. Upload the **contents** of the `home-sweet-home` folder to the repository root (index.html, app.js, styles.css, etc.).
3. Open repository **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, `main`, `/ (root)`, then Save.
4. Wait for GitHub to publish your site. It will usually appear at `https://YOUR-USERNAME.github.io/home-sweet-home/`.
5. On iPhone, open the site in **Safari**, tap **Share**, then **Add to Home Screen** (or use the Share menu's More options). Name it `Home Sweet Home`.
6. Open the new Home Screen icon. Once loaded, the app can work offline in that browser installation.

**Privacy warning:** GitHub Pages sites from public repositories are publicly accessible. The *app code* and its built-in example tasks are public. Your entered checkmarks, notes, and meal changes stay in local browser storage and are not sent to GitHub by this code. Do not put private information directly in the source files or public repository.

## Important limitations
- Data is saved with `localStorage` on that device/browser only. It will **not sync** between iPhone, laptop, or separate app/browser storage contexts.
- Removing the Home Screen app, clearing website data, or switching devices can erase local data. Use **More → Export backup** regularly, and import on the new device.
- No push notifications or automatic reminders are implemented. Use iPhone Reminders separately for filter changes or trash night.
- Service worker offline support requires HTTPS (GitHub Pages provides it) or localhost. Double-clicking index.html is not the recommended setup.
- After editing source files, change `CACHE` in `sw.js` (e.g., v2) to force offline cache refresh; you may also need to reload the installed app.

## Customize
- Edit `ROUTINE`, `PROJECTS`, `MAINT`, and `DEFAULT_MEALS` in `app.js`.
- Edit colors in `styles.css`.
- Change the house icon in `icon.svg`.
- Existing saved meal plans and project checkmarks are not overwritten by source edits. To fully reset, use More → Erase all app data (export a backup first).

## File map
- `index.html`: app shell
- `styles.css`: design
- `app.js`: screens, task data, storage, interactions
- `manifest.webmanifest`: install metadata
- `sw.js`: offline cache
- `icon.svg`: app icon
