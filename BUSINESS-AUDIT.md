# Karipap Pusing NH, public-source business audit

Research date: 30 July 2026

This audit uses public information only. Product claims, prices, certification, capacity and operational details must be confirmed directly with Karipap Pusing NH before commercial launch.

## Confirmed public footprint

- Karipap Pusing NH sells and distributes fried and frozen karipap from Ukay Perdana, Ampang. The public Linktree lists daily operating hours of 8:00 AM to 6:00 PM, a shop location, an agent list and an agent application link.
- Public reseller listings show six frozen flavours in 10-piece packs: ayam, daging, kambing, kentang, sardin and telur.
- Third-party listings describe the frozen product as half-cooked and suitable for air-frying or deep-frying.
- The brand is available through reseller channels including Khayr Frozen and Shopee. Public Shopee search data shows more than 1,000 units sold through one distributor listing, which indicates market traction but does not represent direct factory sales.
- Karipap Pusing NH already has a website at `karipappusing.com`, but its indexed menu still contains unrelated burger and pizza template content. Its public payment page instructs customers to transfer money manually and report payment through WhatsApp.

## Main digital gaps

1. **Unfinished existing website**
   Unrelated demo content reduces trust and can confuse customers searching for products, prices and delivery information.

2. **Manual payment reconciliation**
   Bank transfer plus WhatsApp proof requires staff to match names, amounts and orders manually. It also makes payment status difficult to track across retail, corporate and wholesale orders.

3. **Retail and bulk enquiries share the same channel**
   A normal consumer order, a 1,000-piece corporate order and a stockist reorder require different pricing, approval and delivery flows.

4. **No visible production planning layer**
   Orders need to be converted into flavour quantities, pack counts, production dates, cold-storage allocation and dispatch schedules.

5. **Agent network needs structured management**
   Agent applications, zones, price tiers, order history, marketing materials and repeat orders should be managed from one system.

## Recommended solution

### Customer storefront

- Six-flavour catalogue with approved product photos and confirmed prices.
- Frozen or fried selection.
- Pickup and delivery options.
- Cart, checkout, payment status and automatic WhatsApp confirmation.
- SEO landing pages for frozen karipap, office catering, kenduri and stockist enquiries.

### Wholesale portal

- Separate enquiry form for corporate, event, cafe, agent, stockist and OEM requests.
- MOQ and price tiers controlled by customer type.
- Quotation approval followed by online deposit, then balance-payment link.
- Purchase-order upload and recurring reorder links.

### Production and cold-chain dashboard

- Daily production queue grouped by flavour and required date.
- Batch or lot number, production date, expiry date and storage status.
- Raw-material forecast based on confirmed orders.
- Packing, freezer and dispatch status board.
- Delivery manifest and proof of delivery.

### Agent CRM

- Agent profile, territory, tier and approved price list.
- Order history, outstanding balance and sales performance.
- Downloadable posters, product photos and campaign links.
- Automated reorder reminders and inactive-agent follow-up.

### Management reporting

- Retail versus wholesale revenue.
- Best-selling flavours and channels.
- Paid, deposit, balance-due and cancelled orders.
- Production demand for the next 7 and 30 days.
- Agent and stockist performance.

## Payment recommendation

Billplz is suitable for a Malaysian pilot because it supports FPX, payment links and API-based Bills. The integration should be handled by a server-side function or Worker. Secret keys must never be stored in the public GitHub Pages frontend.

The website remains in demo mode until Karipap Pusing NH provides and approves:

- registered organization name and registration number
- organization bank account
- TIN and business details required by Billplz
- Billplz Collection ID, Secret Key and X Signature key
- confirmed pricing, delivery fees, refund terms and deposit policy

## Suggested rollout

1. **Phase 1, sales foundation:** approved content, catalogue, checkout, Billplz FPX and order database.
2. **Phase 2, bulk operations:** quotations, deposits, production queue and delivery board.
3. **Phase 3, distribution:** agent CRM, stockist price tiers, recurring reorders and analytics.

## Public sources reviewed

- https://linktr.ee/karipappusingnh
- https://karipappusing.com/
- https://karipappusing.com/pembayaran/
- https://karipappusing.com/our-menu/
- https://khayrfrozen.com.my/product-category/%F0%9F%A5%9Fkaripap-pusing-buncit-nurul-hasanah/
- https://shopee.com.my/shop/43658388
- https://main.billplz.com/pricing
- https://support.billplz.com/guide/add-a-new-account
- https://support.billplz.com/guide/settlement-schedule-by-payment-method
- https://support.billplz.com/api
