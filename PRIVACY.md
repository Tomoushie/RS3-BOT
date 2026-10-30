# Privacy Policy — RS3Bot

_Last updated: 30 October 2026_

RS3Bot is a **local-first** Windows application. This document explains exactly what is stored and what is never sent anywhere.

## What RS3Bot stores locally

On your computer only (`%APPDATA%\RS3Bot\` and the WebView local storage):

- Grand Exchange cache (`cache.json`), price history, item metadata;
- Favourites, trade journal, bank, alerts, comparator slots, map preferences;
- Interface preferences (language, theme, notifications, cursor, window size);
- Local profile names and salted PIN hashes (profiles are an optional local convenience);
- Premium license token and a random device identifier (if you activate a license);
- Debug logs you explicitly export from the Internal build.

Nothing in this list is uploaded to us or to any third party.

## What RS3Bot sends over the network

Only **read-only requests to public data sources**:

- `secure.runescape.com` (Jagex itemdb) — official GE prices and metadata;
- `api.weirdgloop.org` — community prices, volumes and history;
- `runescape.wiki` — item/quest/NPC/map data and news;
- `maps.runescape.wiki` — map tiles (premium map only).

These requests contain no personal information. We do not operate a data-collection server, and the app has **no telemetry or analytics**.

## Premium licensing

Premium licenses are **offline**: the app verifies the signed license locally with an embedded public key. The license token and a random device ID are stored locally. If you contact us to request a license, your email address is processed solely to send the key and provide support.

## Data sharing

We do **not** sell, rent, share or transfer your data. We cannot access your local journal, bank or favourites.

## Data deletion

Delete `%APPDATA%\RS3Bot\` and the app's local storage to erase every trace. Uninstalling the app removes the installation but may leave `%APPDATA%\RS3Bot\`; you can delete it manually.

## Children

RS3Bot is not directed at children under 13. Do not send us personal data if you are under 13.

## Changes

Any change to this policy will be published in this file and in the release notes.

## Contact

nowaktombe@protonmail.com
