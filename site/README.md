# PropNet sales site

A standalone landing page for PropNet. It lives in its own folder so the app (the files at the repo root) is never touched.

- Live address once pushed: https://adrianstandage-ai.github.io/Standageadrian-/site/
- Files: `index.html`, `img/` (real app screenshots with sample data, logo), `fonts/` (self-hosted Manrope and Fraunces, so no Google Fonts request).
- No cookies, no trackers, no build step.

## Links the page uses

All set in the small script at the bottom of `index.html`:

- `CHECKOUT`: the live Lemon Squeezy checkout (same link as `LS_CHECKOUT` in the app).
- `APP`: `../` (the app, one folder up). Terms and privacy links are `../terms.html` and `../privacy.html` in the HTML.
- `DEMO`: the YouTube video id. The video only loads from youtube-nocookie.com when someone presses play.

If the site moves to its own domain (for example the websites team hosts it), change `APP` to the app's full address and update the terms, privacy and footer links to full addresses too.

## Visitor counting

Off by default. To switch on cookieless counting, create a GoatCounter site and uncomment the script line in the `<head>`. Every buy, demo and app button already has a `data-goatcounter-click` name, so clicks are counted without more code.

## The app's service worker

`sw.js` at the root also covers this folder for people who have the app installed. It is network-first, so the page always loads fresh when online. No change to `sw.js` is needed.
