# House Hunt Dashboard — Bicester & Deddington (+15 mi)

A self-contained, single-page dashboard tracking 4-bed detached houses ≤ £600,000
around Bicester, Deddington and villages within 15 miles.

**Live site:** enable GitHub Pages (Settings → Pages → Deploy from branch → `main` / root)
and it will be served at `https://<your-username>.github.io/house-hunt-dashboard/`

## What's in it
- One card per property, **deduplicated across Rightmove, Zoopla and OnTheMarket**
- Photo, description, floorplan link, links to every portal advert
- Current advertised price + **recommended opening offer** based on HM Land Registry
  sold prices (last 2 years, detached, per postcode district), time-on-market and
  price-reduction signals
- Filters by area and match score; sortable by price / negotiation room

## Search criteria
4-bed detached · ≤ £600k · utility room · open-plan kitchen/diner · WC on every floor ·
ensuite master · garage convertible to office (or already converted) · nice area within
15 miles of Bicester / Deddington.

## Updating
The dashboard is refreshed weekly (Fridays) by a Claude Cowork scheduled task, which
regenerates `index.html`. To publish an update:

```bash
cp <new-index.html> index.html
git add index.html && git commit -m "Weekly refresh $(date +%F)" && git push
```

*Offer prices are research guidance, not a formal valuation. Data © respective portals
and HM Land Registry; images served from the agents' own listings.*
