# Taipei Family Trip Guide — May 2026

Interactive single-file HTML travel guide for a Taipei family trip, built for GitHub Pages deployment.

This project is designed as a lightweight travel web app for a family trip to Taipei from **May 10–17, 2026**. It includes an editable itinerary, restaurants, shopping, apps, trip-prep notes, Google Maps route export links, and a drag-and-drop itinerary builder that works on desktop and mobile.

## Files included

- `index.html` — the full self-contained travel web app
- `README.md` — this project summary and deployment guide

No build step is required. The app can run directly from GitHub Pages because it is a static HTML file.

## Core features

- Responsive web app for desktop and mobile
- Trip itinerary with day summaries, category buckets, and detailed day-by-day planning
- Restaurant guide sorted into useful food categories instead of a catch-all list
- Shopping guide with Taipei 101, Xinyi, stationery, local crafts, character shopping, and souvenir stops
- Apps checklist for Taipei travel logistics
- Trip prep checklist with tappable checklist behavior
- Local browser persistence via `localStorage` for itinerary edits

## Latest itinerary updates

The itinerary reflects the latest family logistics:

- **May 11** is now a more relaxed arrival, shopping, and leisure day because 2 family members arrive later that afternoon.
- **Elephant Mountain + Taipei 101** were moved later so all 10 family members can participate.
- **May 15** functions as the final full day together for the full family group.
- **May 16** accounts for 8 family members flying to Seoul at **12:55 PM**, including checkout and airport-transfer buffer time.
- **May 17** accounts for the remaining 2 travelers flying out at **9:55 AM**.

## Interactive drag-and-drop itinerary builder

The detailed day-by-day itinerary includes a live editing interface.

### What you can do

- Reorder itinerary events by dragging and dropping them.
- Click an itinerary card to select/highlight it.
- Edit activity times, titles, and descriptions directly in the card.
- Move events earlier or later with buttons.
- Duplicate events.
- Remove events.
- Add custom activities manually.
- Reset a day back to the original itinerary.
- Rebalance times automatically.

### Activity side panel

The itinerary editor includes a categorized activity library side panel with places, restaurants, snacks, markets, and activities.

Categories include:

- Iconic sights
- Food & restaurants
- Night markets & snacks
- Shopping & leisure
- Day trips & scenic activities

### Insert-between behavior

The newest interaction update allows activities to be inserted between existing itinerary items.

- Drop lines appear before, between, and after itinerary items while dragging.
- Drag a side-panel place, restaurant, snack, market, or activity onto a line to insert it at that exact position.
- Drag an existing itinerary card onto a line to move it to that exact position.
- Drag a side-panel item onto an existing card to replace that activity while preserving the card's start time.
- Dragging over an insertion line highlights where the new event will be placed.
- Dragging over an existing itinerary card highlights the replacement target.

### Automatic time reflow

The itinerary automatically updates event timing after changes.

- Reordering events recalculates later times.
- Inserting a new event recalculates following events.
- Replacing an activity preserves the replaced slot's start time, then reflows later events.
- Manual time edits become the new anchor point for following events.
- Duplicate/delete/move actions keep the schedule chronologically organized.
- Time spacing uses activity-duration assumptions plus practical between-stop transfer estimates.

## Google Maps routing export

The app intentionally uses a secure Google Maps export model rather than embedding a client-side Google Maps API key.

Each detailed itinerary day includes:

- **Open full Google Maps** route button
- Individual **Map stop** links for activities
- Route order based on the current draggable itinerary sequence
- Built-in between-stop travel estimate cards
- Recommended travel methods such as walking, MRT, taxi, private van, or airport transfer

Because the app does not embed a Google Maps API key, live routing and traffic calculations happen after opening the route in Google Maps.

## Restaurant guide organization

Food and restaurant items are sorted into the existing restaurant guide categories, including:

- Must-eat iconic
- Michelin / Bib-style local food
- Hot pot & groups
- Splurge & farewell
- Night market dishes
- Snacks, tea & sweets
- Taiwanese bars and drinks

Recent additions include items such as **ISLAND Buffet Taipei Hi-Lai Branch**, **Yao Yue Teahouse**, Wang's Broth, A Cheng Goose, Liu Shandong Beef Noodles, Lao Shan Dong, Yongkang Beef Noodles, Tian Jin Scallion Flaky Pancakes, Smoothie House, Xing Fu Tang, Fuzhou Black Pepper Bun, 50 Lan, Bai-Shui Douhua, and other Taipei food stops.

## Mobile optimization

The app includes responsive behavior for smaller screens:

- Activity library stacks above the itinerary on mobile.
- Larger touch targets for itinerary controls, tabs, and buttons.
- Improved card spacing for editable itinerary items.
- Better mobile behavior for transfer cards and route links.
- Scroll-friendly navigation and tab rows.

## GitHub Pages deployment

1. Create a GitHub repository.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Save and wait for GitHub Pages to publish the site.

## Local use

Open `index.html` directly in any modern browser.

Itinerary edits are saved locally in that browser through `localStorage`. To make permanent changes for everyone, edit the source `index.html`, commit it to GitHub, and redeploy through GitHub Pages.

## Security note

This version does **not** expose a Google Maps API key in the HTML file. Routing is handled through outbound Google Maps links and built-in practical estimates, which makes the project safer for public GitHub Pages hosting.
