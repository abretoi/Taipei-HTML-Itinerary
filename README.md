# Taipei Family Trip Guide — May 2026

An interactive, single-file HTML travel guide for a family trip to Taipei, Taiwan from **May 10–17, 2026**. The guide is designed for a group of 10 travelers staying at **Park Taipei Hotel**, with itinerary planning, restaurants, shopping, apps, and trip-prep details organized into a mobile-friendly web app.

## Project Overview

This repository is intended to host a static GitHub Pages site using `index.html` as the main entry point. The guide is built as a self-contained HTML web app with embedded CSS and JavaScript, so it does not require a build process, package manager, backend, database, or external framework.

The app includes:

- A day-by-day Taipei itinerary
- Flexible scheduling for staggered arrivals and departures
- Restaurant and food recommendations
- Shopping, souvenirs, character goods, stationery, luxury malls, and local craft stops
- Must-download travel apps
- Trip-prep checklist and packing guidance
- Live or search-safe external links for maps, official websites, and app downloads

## Latest Itinerary Logic

The itinerary has been updated to account for two important scheduling changes:

1. **Two family members arrive later on May 11**  
   Because 2 travelers will not arrive until the afternoon of May 11, the original Taipei 101 and Elephant Mountain activities were moved later so all 10 travelers can participate together.

2. **Split departures on May 16 and May 17**  
   - 8 family members leave for **Seoul, South Korea on May 16 at 12:55 PM**.
   - The schedule now includes checkout and airport-transfer time for that group.
   - 2 remaining travelers depart Taipei on **May 17 at 9:55 AM**.
   - May 16 afternoon/evening is now optimized as a lighter final Taipei window for the remaining 2 travelers.

## Key Content Updates

Recent updates include:

- May 11 changed into a more relaxed Xinyi shopping, leisure, and arrival-friendly day.
- Elephant Mountain and Taipei 101 moved to a later shared day so the full group can join.
- May 15 positioned as the final full day together for all 10 travelers.
- May 16 updated for the Seoul departure group and the remaining 2 travelers.
- May 17 added as the final departure morning for the remaining 2 travelers.
- Added **ISLAND Buffet Taipei Hi-Lai Branch** to the restaurant guide.
- Added **Yao Yue Teahouse** to Snacks, Tea & Sweets.
- Updated character-shopping links to avoid broken pages or 404 errors by using official links or search-safe fallbacks.

## File Structure

```text
.
├── index.html      # Main single-file Taipei travel guide web app
└── README.md       # Project summary and GitHub Pages instructions
```

## How to Deploy on GitHub Pages

1. Create a new GitHub repository.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Go to the repository's **Settings** tab.
4. Select **Pages** from the left-side menu.
5. Under **Build and deployment**, choose:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
6. Save the settings.
7. GitHub will generate a public GitHub Pages URL after deployment.

## Local Preview

You can preview the guide locally by opening `index.html` directly in a browser.

For a local server preview, run:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Notes for Future Updates

When updating the guide:

- Keep `index.html` at the root of the repository.
- Avoid adding broken direct links for shops or character-goods stores; use official websites, Google Maps search links, or Google Search fallbacks when a reliable page is unavailable.
- For itinerary changes, update both the day summary and detailed day-by-day sections so the app remains consistent.
- For restaurant additions, place each recommendation in the most relevant tab based on dining type, price point, or occasion.

## Intended Use

This app is meant to be shared with family members before and during the trip. It works especially well on mobile devices and can be uploaded to GitHub Pages, Netlify, Vercel, or any static website host.
