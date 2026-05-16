# flight-phone-landing

Small **static** mobile-first landing for **Google Ads** call campaigns in the **U.S. flight booking** vertical.

## Why this is a separate repository

It is **not** a Git submodule of `WeAdU-ltd/.github`. Keeping the site in its own repo makes **Netlify**, **Cloudflare Pages**, or similar hosts straightforward (one root, one `index.html`, isolated lifecycle).

## Marketcall research (optional)

Affiliate-offer snapshot, benchmark notes, and a small script to refresh exports from the Marketcall API live in this repo (they are **not** required to deploy the static landing):

| Path | Role |
|------|------|
| `docs/marketcall_offers_active_snapshot_2026-05-15.csv` | CSV snapshot (`GET /api/v1/affiliate/offers`) |
| `docs/marketcall_offers_benchmark_2026-05-15.md` | Analysis / Google Ads–aligned framing |
| `scripts/marketcall_fetch_offers.py` | Paginated JSON export; needs env `MC_KEY` (see script header) |

## Google Ads — planning docs (WEA-189–WEA-194)

Operational artifacts for the same **US flight / call** vertical (negatives, FAQ, go-live checklist, tracking, QA, extensions). Versioned next to the landing:

| Path | Linear |
|------|--------|
| `docs/google-ads/us-flight-call-negative-keywords.csv` | WEA-189 |
| `docs/google-ads/us-flight-call-landing-faq.md` | WEA-190 |
| `docs/checklists/google-ads-landing-campaign-go-live.md` | WEA-191 |
| `docs/google-ads/google-ads-marketcall-call-tracking-plan.md` | WEA-192 |
| `docs/qa/us-flight-call-qa-monitoring.md` | WEA-193 |
| `docs/google-ads/us-flight-call-ad-extensions-copy.md` | WEA-194 |

## Publish

1. Edit `index.html` and replace every `REPLACE_*` placeholder and the example phone `+15551234567` in **all** places: visible text, `href="tel:…"`, and JSON-LD `telephone`.
2. Set the `<link rel="canonical" href="…">` to the final **HTTPS** URL of this page (same host you use as the Google Ads final URL).
3. Deploy the **repository root** so `index.html` is served at `/` on your domain.

The checklist at the top of `index.html` (HTML comment) summarizes Google Ads–oriented checks before you send traffic.

## Policies

Google updates advertising policies over time. Re-read the relevant **Google Ads Policy Help** articles (destination requirements, insufficient original content, misrepresentation, dishonest pricing practices, call ad requirements, unverified phone number, destination experience, trademarks) before launch and after major campaign changes.
