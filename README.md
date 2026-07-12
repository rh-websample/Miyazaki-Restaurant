# Miyazaki — Restaurant Website

A single-page static website concept for **Miyazaki**, a Japanese restaurant
in Molito Complex, Alabang (Muntinlupa City) — built referencing the public
description and tone of its
[Facebook page](https://www.facebook.com/miyazakiph/), and using six
restaurant-supplied photos (dining room, yakiniku table, and four dishes) as
the actual imagery on the page. Everything else — the ensō brush-circle
mark, wave dividers, line icons — is original, hand-coded SVG built to match
a refined, modern-traditional Japanese dining aesthetic: ink, warm washi
paper, deep indigo, antique gold, and a muted brick-red accent that echoes
the restaurant's red lacquer trays.

## Structure

```
miyazaki-restaurant/
├── index.html            # all page content/sections
├── css/style.css          # design tokens, layout, animation
├── js/script.js           # mobile nav, footer year
├── assets/favicon.svg     # site icon (ensō mark)
├── assets/gallery/        # restaurant photos used on the page
│   ├── tatami-room.jpg      — hero background + Tatami Rooms card
│   ├── yakiniku-table.jpg   — Yakiniku Rooms card
│   ├── kani-salad.jpg       — Kani Salad dish card
│   ├── beef-hotpot.jpg      — Beef Hot Pot dish card
│   ├── tuna-tataki.jpg      — Tuna Tataki dish card
│   └── shrimp-fried-rice.jpg — Shrimp Fried Rice dish card
└── README.md
```

No build step, no dependencies — plain HTML/CSS/JS. Google Fonts
(Shippori Mincho, Noto Sans JP) load via CDN link tags.

## Run locally

Just open `index.html` in a browser, or serve it locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `miyazaki-restaurant`).
2. Push these files to the repo:
   ```bash
   git init
   git add .
   git commit -m "Miyazaki restaurant website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/miyazaki-restaurant.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`.
5. Save — GitHub will publish the site at
   `https://<your-username>.github.io/miyazaki-restaurant/` within a minute
   or two.

## Customizing

- **Colors / fonts**: edit the CSS custom properties at the top of
  `css/style.css` (`:root { --gold, --vermilion, --indigo, --washi, ... }`).
- **Menu, hours, address**: edit directly in `index.html` (`#menu`,
  `#hours` sections) — prices and hours here are drawn from public listings
  and should be double-checked against the current Facebook page or the
  restaurant directly before publishing.
- **Photos**: swap files in `assets/gallery/` to update any photo — filenames
  are referenced directly in `index.html`, so keep the same filename or
  update the `src` attribute if you rename one.

## Notes

This is an unofficial, fan-made demo — not affiliated with or endorsed by
Miyazaki. Replace placeholder details (menu prices, hours, contact info)
with verified current info before treating this as a real business site.
