# fluffle-ua

Public link-only copy of the Ukrainian Fluffle business one-pager.

- `index.html` — the page. Source of truth is `Fluffle Deck/fluffle-business-one-pager-explainer-ua.html`; this is a published copy with web-optimised assets.
- `robots.txt` — blanket `Disallow: /` plus named AI/scraper agents.
- Contact details are base64-encoded in `data-c` attributes and assembled by an inline script at load, so scrapers that do not execute JavaScript find nothing usable.

## Caveats

- `robots.txt` and `noindex` are advisory. They stop compliant search engines, not determined harvesters. Anything on this page is readable by anyone who fetches the URL.
- `Disallow: /` and the `noindex` meta tag are belt-and-braces: a crawler obeying `robots.txt` never fetches the page and so never sees the meta tag. The page is unlisted, so the practical protection is that nothing links to it.
- The repo is public (required for GitHub Pages on a free account), so this HTML is also browsable on github.com.

## Updating

Re-run the publish transform from the deck folder, then `git commit && git push`. Pages redeploys on push to `main`.
