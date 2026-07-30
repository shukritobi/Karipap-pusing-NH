# Karipap Pusing NH website and wholesale operations concept

Responsive customer storefront, six-flavour product catalogue, shopping cart, bulk-order form, wholesale operations proposal, owner-dashboard concept and Billplz-ready payment architecture.

## Website pages

The deploy workflow reconstructs the website from the versioned files under `bundle/` and publishes these pages:

- `index.html`: customer storefront and cart
- `solution.html`: wholesale and manufacturing operations proposal
- `dashboard.html`: owner dashboard demo, all figures are sample data
- `payment-status.html`: payment return page

To inspect the complete source locally:

```bash
mkdir -p site-source
cat bundle/part-* | base64 --decode | tar -xz -C site-source
```

## Payment status

The public preview runs in `demo` mode because a real Billplz merchant account, Collection ID, API key and X Signature key were not provided. No real charge is created in demo mode.

For live Billplz:

1. Create and verify the merchant organization.
2. Create a Collection in Billplz.
3. Deploy the Cloudflare Worker included under `/worker` in the extracted source.
4. Store `BILLPLZ_API_KEY` and `BILLPLZ_X_SIGNATURE_KEY` as Worker secrets.
5. Set the Collection ID, site URL and Worker URL in `wrangler.toml`.
6. Change the extracted `config.js` to:

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

## Product prices and assets

Prices shown are reference values gathered from public third-party listings and are not confirmed direct factory prices. Confirm all prices, product names, pack sizes, delivery fees and availability with the owner before switching the site from demo to live.

The preview uses public product-image URLs found during research. Obtain the owner's written permission and replace them with approved original assets before commercial launch.

## GitHub Pages

The workflow at `.github/workflows/pages.yml` automatically deploys the bundled site. GitHub requires the repository publishing source to be set to **GitHub Actions** before the first Pages deployment:

1. Open repository **Settings**.
2. Select **Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Open **Actions** and rerun **Deploy Karipap Pusing NH website** if necessary.

Expected project-site address after deployment:

`https://shukritobi.github.io/Karipap-pusing-NH/`

## Content checks before launch

- Confirm the registered company or organization name.
- Confirm Halal certification before displaying any Halal claim or logo.
- Confirm the exact pickup address, opening hours and delivery zones.
- Confirm allergen statements, storage temperature, cooking instructions and shelf life.
- Replace reference prices with approved retail, agent and stockist tiers.
- Confirm deposit, cancellation, refund and delivery policies.
