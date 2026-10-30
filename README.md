# migration

Website: https://move.datubu.com

This is a separate website configuration and GitHub Pages deployment repository in the Datubu network. All original content is read from **human-journeys**; shared website code is read from **journeys**.

## Local build

Place this repository beside human-journeys and journeys. Install dependencies in journeys with `npm ci`, then run `npm run build` here. Output is written to dist/. For a connected nine-site local preview, run `npm run build:all` and `npm run preview` in journeys.

## Upload and Pages

GitHub repository: https://github.com/datubu/migration. Select GitHub Actions as the Pages source. The workflow reads the shared repositories under the same owner. CONTENT_REF and ENGINE_REF repository variables may pin a branch, tag or commit; build-info.json records resolved commits. CUSTOM_DOMAINS_ACTIVE defaults to false: cross-site links use GitHub Pages project URLs until the domain is configured.

Bind move.datubu.com in Pages settings after the matching DNS record is ready, then set CUSTOM_DOMAINS_ACTIVE=true for all website repositories and rebuild. The generated CNAME file documents the intended domain; Actions-based publication still requires the Pages setting.

## Features

Chinese/English, light/dark themes, mobile bottom navigation and a static app-shell cache are shared with all destinations. Cached text can be read offline; map tiles require a network connection. No account server or cross-domain saved-data synchronization is provided.
