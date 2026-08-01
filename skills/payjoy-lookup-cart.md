---
name: Look up a PayJoy cart / sale
description: Retrieve a cart's sale, approval, financing and (where permitted) customer details.
api: openapi/payjoy-partner-api-openapi.yml
operations: [getCartByTag]
---

# Look up a PayJoy cart / sale (Partner API V2)

## Auth
`X-PayJoy-ApiKey` header on every request.

## Steps
1. **Get cart** — `GET /v2/carts/{cartTag}` (`getCartByTag`). Returns amounts (`purchaseAmount`,
   `financeAmount`, `downPaymentAmount`), status flags (`isCustomerApproved`, `isContractSigned`,
   `isFinanceCreated`), plus `merchant`, `clerk`, and `device`.
2. **Expand as needed** — pass `expand` with any of `customer`, `offer`, `downpayment`, `voucher`.
   `customer` returns PII and is only available in countries that require it for the sale; `offer`,
   `downpayment`, and `voucher` are feature-gated per merchant.

## Rules
- Poll `isContractSigned` / `isFinanceCreated` to know when a sale is complete before fulfilment.
- Unknown cartTag returns **404**. Log `X-Request-ID`.
