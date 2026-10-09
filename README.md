# Home Sweet Home 2.0

A static, phone-friendly home organizer. No backend or account required.

## Updating your existing GitHub Pages site

1. **Back up first:** Open your existing app → More → Export backup. Save the JSON in iPhone Files.
2. Unzip this package. Upload the **contents** of `home-sweet-home`, not the containing folder, to the root of your existing GitHub repository. Replace files with the same names, including `sw.js`.
3. Commit to `main`; GitHub Pages publishes the update.
4. Open your existing Home Screen app. If it looks old, close and reopen it, or visit the website in Safari and reload. Offline caches can take a moment to refresh.
5. Existing data is preserved because the app continues using the same `localStorage` key (`home-sweet-home-v1`). Keep the same domain, repository path, and iPhone/browser storage.

## Features
- Today, Week, Calendar, Reset, Meals, More
- Shark floor-care on Thursdays, upstairs carpet vacuuming on Wednesdays
- Monthly maintenance checks, editable dinner plan, grocery checklist, dated calendar notes
- Export/import JSON backups; local-only storage; no push notifications or cross-device sync

## Privacy
GitHub Pages is publicly accessible. Do not put private personal details in source files. Data you type into the app stays in local browser storage on that device, unless you export and share a backup.
