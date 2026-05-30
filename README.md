# City Atlas

A single-file map for tracking the cities you have visited and the ones still on your list, with a rough budget for clearing the list.

Pin where you have been, tier the places you still want to go (cheap / mid / splurge), and the app tells you how many are left, the total to clear the list, and the average cost per remaining city.

**Live demo:** https://rizabalci.github.io/city-atlas/

## Features

- Interactive world map (Leaflet + CARTO dark tiles)
- Add cities by search, or click anywhere on the map to drop a pin
- Visited cities get a pearl pin with a check; wishlist cities are colour-coded by cost tier (green / amber / red)
- Live stats: visited count, remaining count, total to clear, average cost per city
- Editable cost tiers so the budget reflects your real numbers
- Saves automatically in the browser (localStorage)
- Export and import your atlas as JSON for backup or moving between devices

## Run locally

It is one file with no build step. Either:

- Double-click `index.html` to open it in your browser, or
- Serve it for a cleaner setup:

```bash
cd ~/Desktop/city-atlas
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy to GitHub Pages

1. Push this repo to GitHub (see below).
2. In the repo: **Settings -> Pages**.
3. Under **Build and deployment**, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, then Save.
4. After a minute it goes live at `https://rizabalci.github.io/city-atlas/`.

## Notes

- City search and map-click lookups use the free OpenStreetMap Nominatim API, so they need an internet connection.
- Default cost tiers (€400 / €900 / €2,000) are placeholders for flights plus a stay from Vienna. Set your own under "Cost tiers" and everything recalculates.
- Your data lives only in your browser. Use Export regularly if you want a backup.

## Tech

Plain HTML, CSS, and JavaScript. No framework, no build. Leaflet for the map, Nominatim for geocoding, Google Fonts (Fraunces + Archivo).

## License

MIT. See [LICENSE](LICENSE).
