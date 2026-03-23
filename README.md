# Gratis LA

A website-first Koreatown research database that works on mobile and desktop under strict rules:

- Tips are not accepted.
- No service fee is imposed.
- Fast food chains are excluded.
- Listings include source citations.

## Project Structure

This project uses a React frontend powered by Vite and a backend powered by Supabase.

- **`src/`**: Contains the React application code. This is where all the UI components, styles, map logic (Leaflet), and state management live.
- **`public/`**: Static assets that don't need processing, like the PWA manifest, service workers, and app icons.
- **`scripts/`**: Automation tools used for gathering, validating, and managing data behind the scenes. This includes scrapers, formatting scripts, and database sync utilities.
- **`supabase/`** *(local only)*: Contains the database schema and seed data to replicate the exact database state locally.
- **`data/`** *(local only)*: Raw output logs from web scrapers and AI agents used to gather new leads and build the database.
- **`docs/`** *(local only)*: Legacy GitHub Pages deployment folder.

*(Note: Data, Supabase credentials, and iOS build artifacts are kept off the public repository for security and cleanliness.)*

## Quick start (no accounts, no data keys)

Run immediately in local mode:

```bash
npm install
npm run dev
```

Local mode behavior:

- Loads bundled demo data automatically.
- No Supabase account needed.
- Uses the same responsive UI on phones and desktops.
- Includes a live interactive map.

## Setting up Full Cloud Mode (optional)

Use this only when you want live shared data, moderation, and scheduled verification updates.

### 1. Configure local env

1. Copy `.env.example` to `.env`.
2. Fill your Supabase variables:

```bash
VITE_SUPABASE_URL=...
VITE_SUPABASE_ANON_KEY=...
```

With valid environment keys, the website switches automatically from demo mode to Supabase-backed live mode when you run `npm run dev`.

## Important note

No free data source can guarantee perfect policy freshness at all times. This app is built for transparency with visible citations.
