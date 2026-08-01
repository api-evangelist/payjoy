---
name: Redeem or cancel a PayJoy voucher
description: Redeem a voucher code at point of sale, or cancel one that was issued in error.
api: openapi/payjoy-partner-api-openapi.yml
operations: [redeemVoucher, cancelVoucher]
---

# Redeem or cancel a PayJoy voucher (Partner API V2)

## Auth
`X-PayJoy-ApiKey` header on every request.

## Steps
1. **Redeem** — `PUT /v2/vouchers/{voucherCode}/redeem` (`redeemVoucher`) with body `amount`,
   `currency` (ISO 4217), and optional `metadata`. Returns `authorizationCode` and `redeemedAt`.
2. **Cancel** (only if issued/redeemed in error) — `PUT /v2/vouchers/{voucherCode}/cancel`
   (`cancelVoucher`) with `amount`, `currency`. Returns `cancellationCode` and `cancelledAt`.

## Rules
- A missing/invalid voucher returns **404 Not Found**.
- `amount` is a two-decimal number; `currency` must match `^[A-Z]{3}$`.
- Persist the `authorizationCode` / `cancellationCode` for audit and reconciliation.
