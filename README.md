# CalSwipes — website

The marketing, support, and privacy site for **[CalSwipes](https://apps.apple.com/us/app/calswipes/id6815878177)**, a free iPhone app that helps UC Berkeley students turn Berkeley Dining menus into meals that fit their calorie and nutrition goals.

**[Download on the App Store →](https://apps.apple.com/us/app/calswipes/id6815878177)**

## Pages

| Page | Path | Purpose |
|---|---|---|
| Home | `dist/index.html` | Product overview and App Store link |
| Support | `dist/support/index.html` | Contact and help |
| Privacy Policy | `dist/privacy/index.html` | Linked from App Store Connect |

## Design principles

- **Zero dependencies:** plain HTML and CSS, with no frameworks, client JavaScript, or build step
- **Private by default:** no tracking, analytics, cookies, or external fonts
- **Fast:** the whole site is a few static files in `dist/`

## Run locally

```sh
node serve.mjs
```

Then open http://127.0.0.1:4173.

## Deploy

All published files live in `dist/`. There is no build step, so any static host works:

- **GitHub Pages:** handled by `.github/workflows/pages.yml` on every push to `main`
- **Vercel:** Framework preset *Other*, no build command, output directory `dist`

## Editing

- Shared styles are in `dist/styles.css`.
- The support email (`support.calswipes@gmail.com`) appears in `dist/support/` and `dist/privacy/`. Update both if it changes.
- Keep the privacy policy aligned with the app's actual behavior, and update its "Last updated" date after edits.

## Team

Built by **Ashkon Chaghajerdi** and **Dylan Brown** at UC Berkeley.

*CalSwipes is an independent app and is not affiliated with, endorsed by, or sponsored by the University of California, Berkeley.*
