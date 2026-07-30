# Karipap Pusing NH website and wholesale operations concept

Responsive static website, product catalogue, cart, bulk order form, Billplz-ready checkout architecture, operational solution page and dashboard demo.

## Preview pages

- `index.html`: customer storefront
- `solution.html`: proposal for wholesale and manufacturing operations
- `dashboard.html`: owner dashboard demo, all numbers are sample data
- `payment-status.html`: payment return page

## Payment status

The public preview runs in `demo` mode because a real Billplz merchant account, collection ID, API key and X Signature key were not provided. No real charge is created in demo mode.

For live Billplz:

1. Create and verify the merchant organization.
2. Create a Collection in Billplz.
3. Deploy the Cloudflare Worker under `/worker`.
4. Store `BILLPLZ_API_KEY` and `BILLPLZ_X_SIGNATURE_KEY` as Worker secrets.
5. Set the collection ID, site URL and Worker URL in `wrangler.toml`.
6. Change `config.js` to:

```js
window.NH_CONFIG = {
  paymentMode: "billplz",
  apiEndpoint: "https://YOUR-WORKER.workers.dev",
  whatsapp: "60198591963",
  currency: "MYR",
  siteName: "Karipap Pusing NH"
};
```

The backend calculates prices server-side. Never place the Billplz API key in `config.js` or any GitHub Pages file.

## Product prices

Prices shown are reference values gathered from public third-party listings and are not confirmed direct factory prices. Confirm all prices, product names, pack sizes, delivery fees and availability with the owner before switching the site from demo to live.

## GitHub Pages

A Pages workflow is included at `.github/workflows/pages.yml`. If the workflow reports that Pages is not configured, open repository Settings, Pages, then choose GitHub Actions as the publishing source and rerun the workflow.

## Content checks before launch

- Confirm registered company or organization name.
- Confirm Halal certification and only display a Halal claim or logo after verification.
- Confirm exact pickup address, opening hours and delivery zones.
- Confirm allergen statement, storage temperature, cooking instructions and shelf life.
- Replace reference prices with approved retail, agent and stockist tiers.
- Obtain permission for every product image used in the final commercial site.
