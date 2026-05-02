# Taipei Family Trip Guide — May 2026

Interactive single-page Taipei family itinerary web app.

## Latest update: Explore tab link hardening

This version updates the Explore tab to use Google Maps-first outbound links for places, activities, day trips, neighborhoods, and practical stops. This avoids stale tourism pages, blank pages, or 404 errors for items like Elephant Mountain.

### Included behavior

- Explore card title links open a Google Maps search for the exact place/activity.
- Explore **Open map** buttons now always point directly to Google Maps.
- Elephant Mountain now resolves to Xiangshan Trail / Elephant Mountain in Taipei rather than a potentially stale tourism-page URL.
- The broader app remains in secure Google Maps export-only mode, with no embedded Google Maps API key.
- Drag-and-drop itinerary behavior, insert-between drop lines, replacement behavior, automatic time reflow, and mobile-optimized layout remain intact.

## Deployment

Upload the contents of this ZIP to GitHub, Firebase Hosting, Netlify, Vercel, or another static host. The root file must remain named `index.html`.
