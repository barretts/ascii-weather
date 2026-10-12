# ascii-weather

A compact weather app drawn as one ascii screen. Enter a US ZIP code (default 78750, Austin) and it shows the
current weather, the next eight hours, and animated halftone scenes and graphics for the conditions.

Live: https://barretts.github.io/ascii-weather/ (deployed from `main` by `.github/workflows/pages.yml`).

Built with [Astro](https://astro.build) and the [ascii.rest](https://github.com/bas3line/ascii) animation library.

```sh
npm install
npm run dev      # http://localhost:4321
npm run build    # static site in dist/
```

## How it works

- `src/pages/index.astro` is the whole app: the character grid, the layout, the hourly graphics and the data loading.
- The hero scene comes from ascii.rest pieces (`storm-plains`, `alpine-dawn`, `misty-forest`, `night-coast`, `ocean-sunset`),
  drawn on a canvas over the grid. The hourly graphics are drawn in the page itself in the same halftone style.
- ZIP to place: [zippopotam.us](https://zippopotam.us). Weather: [Open-Meteo](https://open-meteo.com).

## Before you publish

- **Open-Meteo** is free for non-commercial use and asks for attribution; ads, subscriptions or in-app purchases need
  a paid plan. Check their current terms.
- **zippopotam.us** is a free service with no stated guarantees. Replace it with a service you control for production.
- **Licenses:** keep `THIRD_PARTY_NOTICES.md` and `public/fonts/OFL.txt` with any build you distribute.
- **iOS:** wrapping a web page in a WebView can be rejected under App Store guideline 4.2 (minimum functionality).
