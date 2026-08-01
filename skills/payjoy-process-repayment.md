---
name: Process a customer repayment
description: Look up repayment options for a financed device, create a payment reference, and pay it.
api: openapi/payjoy-partner-api-openapi.yml
operations: [getPaymentOptions, createPaymentReference, payReference]
---

# Process a customer repayment (PayJoy Partner API V2)

Use this flow when a merchant collects an in-store repayment against a customer's financed device.

## Auth
Send your API key in the `X-PayJoy-ApiKey` header on every request. Keys are generated in the
Partner Console (https://app.payjoy.com/admin-console/login → API). Base URL (sandbox):
`https://partner-integration.sandbox.payjoy.com/partner-api`.

## Steps
1. **List repayment options** — `GET /v2/payments/options` (`getPaymentOptions`). Supply at least one
   of `deviceTag`, `phoneNumber`, or `imei`. Returns `minimumPaymentAmount`, `fullPayoffAmount`, and a
   `paymentOptions[]` list. If `flexibleAmountEnabled` is true, any amount between the minimum and full
   payoff is allowed.
2. **Create a payment reference** — `POST /v2/payments/references` (`createPaymentReference`) with
   `deviceTag`, `amount`, `currency` (ISO 4217), `merchantId`, `salesClerkId`. Returns
   `paymentReference` and `paymentReferenceExpiration` — collect payment before it expires.
3. **Pay the reference** — `POST /v2/payments` (`payReference`) with `paymentReference`, `amount`,
   `currency`, `merchantId`, `salesClerkId`. Returns `transactionId` and `transactionCreatedAt`.

## Rules
- Amounts are numbers with two decimals; `currency` must match `^[A-Z]{3}$`.
- Idempotency: paying an already-paid reference returns **409 / PAYMENT_REFERENCE_ALREADY_PAID**;
  an expired one returns **PAYMENT_REFERENCE_EXPIRED**. Do not blindly retry a 409.
- Errors use `{ error: { code, message, details }, meta: { requestId } }`. Log `X-Request-ID`.
- Test in sandbox with deviceTag `DTSTBBB` (success); see sandbox/payjoy-sandbox.yml for failure cases.
