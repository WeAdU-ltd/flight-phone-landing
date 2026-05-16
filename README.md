# flight-phone-landing

Small **static** mobile-first landing for **Google Ads** call campaigns in the **U.S. flight booking** vertical.

## Why this is a separate repository

It is **not** a Git submodule of `WeAdU-ltd/.github`. Keeping the site in its own repo makes **Netlify**, **Cloudflare Pages**, or similar hosts straightforward (one root, one `index.html`, isolated lifecycle).

## Publish

1. Edit `index.html` and replace every `REPLACE_*` placeholder and the example phone `+15551234567` in **all** places: visible text, `href="tel:…"`, and JSON-LD `telephone`.
2. Set the `<link rel="canonical" href="…">` to the final **HTTPS** URL of this page (same host you use as the Google Ads final URL).
3. Deploy the **repository root** so `index.html` is served at `/` on your domain.

The checklist at the top of `index.html` (HTML comment) summarizes Google Ads–oriented checks before you send traffic.

## Policies

Google updates advertising policies over time. Re-read the relevant **Google Ads Policy Help** articles (destination requirements, insufficient original content, misrepresentation, dishonest pricing practices, call ad requirements, unverified phone number, destination experience, trademarks) before launch and after major campaign changes.
